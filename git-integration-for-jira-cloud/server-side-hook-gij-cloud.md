---
title: Server-side Hook
description: Configure server-side hooks to enforce Jira ticket policies on git pushes.
taxonomy:
    category: git-integration-for-jira-cloud
---

Server-side hooks enforce project policies by running scripts before and after pushes. Use these hooks to require valid Jira ticket references in commit messages.

**On this page:**
- [Understand server-side hooks](#understand-server-side-hooks)
- [Install the pre-receive hook](#install-the-pre-receive-hook)
- [Configure the script](#configure-the-script)
- [Sample script](#sample-script)

&nbsp;
* * *
&nbsp;

## Understand Server-side Hooks

The server runs these scripts when handling pushes from clients:

- **pre-receive**: Runs before accepting any commits. Rejects the push if commits don't have proper Jira issue tags.
- **post-receive**: Runs after the push completes.

Server-side hooks require Python on the server. On Linux and macOS, hook scripts must have executable permissions.

For more information:
- [Customizing Git – Hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks)
- [githooks.com](http://githooks.com/)

&nbsp;

## Install the Pre-receive Hook

1. Download the sample [pre-receive file](https://bigbrassband.com/files/pre-receive.zip).

2. Copy the file to your Git server repository: `hooks/pre-receive`

3. Set executable permissions (Linux/macOS):
   ```bash
   chmod +x hooks/pre-receive
   ```

4. Configure the required settings in the script.

&nbsp;

## Configure the Script

Edit these settings in the pre-receive file:

| Setting | Description | Example |
|---------|-------------|---------|
| `JIRA_XMLRPC` | Path to your Jira instance | `https://jira.example.com/rpc/xmlrpc` |
| `JIRA_USER` | Jira username with issue lookup permissions | `service-account` |
| `JIRA_PASSWORD` | Password for the Jira user | `password123` |
| `PROJECT_KEYS` | Array of project keys (used when Jira is unavailable) | `['PROJ1', 'PROJ2']` |

### How PROJECT_KEYS works

The `PROJECT_KEYS` setting defines project keys that are compared against ticket keys in commit messages. This setting is used only when Jira is unavailable. When Jira is available, the hook validates tickets directly against Jira.

**Pattern example:** `(PROJECT_KEY1|PROJECT_KEY2|...)-\d+`

If the `PROJECT_KEYS` array is empty and Jira is unavailable, the hook performs no checks.

&nbsp;

## Sample Script

```py
#!/usr/bin/python
import sys
import os
import xmlrpclib
import subprocess
import sys
import re

JIRA_XMLRPC = 'https://jira.example.com/rpc/xmlrpc'
JIRA_USER = 'user'
JIRA_PASSWORD = 'password'

PROJECT_KEYS = ['EXAMPLE', 'EXAMPLE']

NO_JIRA_TICKET_MESSAGE = \
'No Jira ticket present in the commit message. \
Please include the Jira ticket key.'
INVALID_JIRA_TICKET_MESSAGE = \
'Proper Jira ticket syntax was found, but none were valid tickets. \
Please check the tickets and try again.'
INVALID_ISSUE_TYPE_MESSAGE = \
'You may not commit against subtasks or task-splits. \
Please commit against the parent ticket.'

FAULT_MSG_ISSUE_NOT_FOUND = 'com.atlassian.jira.rpc.exception.RemotePermissionException'

proxy = xmlrpclib.ServerProxy(JIRA_XMLRPC)

def git(args, **kwargs):
    environ = os.environ.copy()
    if 'repo' in kwargs:
        environ['GIT_DIR'] = kwargs['repo']
    if 'work' in kwargs:
        environ['GIT_WORK_TREE'] = kwargs['work']
    proc = subprocess.Popen(args, stdout=subprocess.PIPE, env=environ)
    return proc.communicate()

def get_log(a, b, **kw):
    entries = {}
    (results, code) = git(('git', 'log', '--pretty=oneline', "%s..%s" % (a, b)), **kw)
    lines = results.splitlines()
    for line in lines:
        (commit, msg)=line.split(' ', 1)
        entries[commit] = msg

    return entries

def check_message(auth, message, ticket_re_pattern):
    tickets = ticket_re_pattern.findall(message)

    if not tickets:
        return NO_JIRA_TICKET_MESSAGE

    if auth == None:
        return None

    for ticket in tickets:
        try:
            issue = proxy.jira1.getIssue(auth, ticket)
        except xmlrpclib.Fault, e:
            if e.faultString.find(FAULT_MSG_ISSUE_NOT_FOUND) >= 0:
                return INVALID_JIRA_TICKET_MESSAGE
            else:
                raise

    # Check if issue is subtask or task-split
    if issue['type'] == '8' or issue['type'] == '5':
        return INVALID_ISSUE_TYPE_MESSAGE

    return None

def build_ticket_re(auth):
    projects = proxy.jira1.getProjectsNoSchemes(auth)
    return build_ticket_re_for_project_list(map(lambda project: project['key'], projects));

def build_ticket_re_for_project_list(projects):
    pattern_string = '\\b('
    for idx, project in enumerate(projects):
        if (idx>0):
            pattern_string +='|'
        pattern_string +=project
        pattern_string +='-\d+?'

    pattern_string +=')\\b';

    return re.compile(pattern_string)

def login():
    try:
        auth = proxy.jira1.login(JIRA_USER, JIRA_PASSWORD)
    except:
        print >> sys.stderr, 'Cannot connect to Jira: ' + str(sys.exc_info()[1])
        sys.exit(2)

    return auth

try:
    auth = login()
    isAuthenticated = True
except:
    isAuthenticated = False

if isAuthenticated:
    ticket_re_pattern = build_ticket_re(auth)
else:
    ticket_re_pattern = build_ticket_re_for_project_list(PROJECT_KEYS);

repo = os.getcwd()
basedir = os.path.join(repo, "..")

line = sys.stdin.read()
(base, commit, ref) = line.strip().split()
commits = get_log(base, commit)

for c, msg in commits.iteritems():
    err_msg = check_message(auth if isAuthenticated else None, msg, ticket_re_pattern)

    if err_msg:
        print >> sys.stderr, 'Error: %s\nCommit message:\n%s' % (err_msg, msg)
        print >> sys.stderr, 'Install pre-commit hook (https://bigbrassband.com/api-doc.html#cmhook) to run this check at the commit time'
        sys.exit(1)
```

<kbd>Last updated: December 2025</kbd>
