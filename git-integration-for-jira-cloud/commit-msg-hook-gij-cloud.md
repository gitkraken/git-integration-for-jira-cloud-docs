---
title: Commit-msg Hook
description: Configure the commit-msg client-side hook to validate Jira ticket references in commit messages.
taxonomy:
    category: git-integration-for-jira-cloud
---

The commit-msg hook validates commit messages before they're accepted. Use this client-side hook to ensure all commits reference valid Jira tickets.

**On this page:**
- [Understand the commit-msg hook](#understand-the-commit-msg-hook)
- [Install the hook](#install-the-hook)
- [Configure the script](#configure-the-script)
- [Sample script](#sample-script)

&nbsp;
* * *
&nbsp;

## Understand the Commit-msg Hook

This hook enables developers to:

- Commit code locally multiple times before pushing to the server
- Merge auto-commits with auto-messages that don't reference Jira tickets

The commit-msg hook is a Python script that runs on each developer's local machine. No server-side hook is required.

&nbsp;

## Install the Hook

1. Download the sample [commit-msg file](https://bigbrassband.com/files/commit-msg.zip).

2. Place the file in your local repository at: **`.git/hooks/commit-msg`**

3. Set executable permissions (Linux/macOS only):
   ```bash
   chmod +x .git/hooks/commit-msg
   ```

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Windows users:</b> Executable permissions are not required. To run the hook without Python installed, see <a href='https://docs.python.org/2/faq/windows.html#how-do-i-make-an-executable-from-a-python-script'>Python on Windows FAQ</a>.
    </div>
    </div>
</div>

&nbsp;

## Configure the Script

Edit these settings in the script file:

| Setting | Description | Example |
|---------|-------------|---------|
| `JIRA_XMLRPC` | Path to your Jira instance | `https://jira.example.com/rpc/xmlrpc` |
| `JIRA_USER` | Developer's Jira username | `developer1` |
| `JIRA_PASSWORD` | Developer's Jira password | `password123` |
| `JIRA_TICKET_PATTERN` | Regex pattern to find ticket references | `re.compile(r'\[(\w+7-\d+?)\]')` |

&nbsp;

## Sample Script

```py
#!/usr/bin/python
#
# This script is intended to be run as a commit-msg script in a GIT
# repository and check the presence of Jira ticket numbers in the log messages.
#
#    - NO_Jira_TICKET_MESSAGE (an error message returned to the user when the
#      svn commit message doesn't contain a jira ticket);
#    - INVALID_JIRA_TICKET_MESSAGE (an error message returned to the user when
#      the svn commit message contains an invalid jira ticket);
#    - JIRA_XMLRPC (url of the Jira XML-RPC server);
#    - JIRA_USER (name of the Jira user who has permission to look up issues in
#      the Jira server);
#    - JIRA_PASSWORD (password of the Jira user described above);

import sys
import re
import xmlrpclib

NO_JIRA_TICKET_MESSAGE = \
'No Jira ticket present in the commit message. \
Please include the Jira ticket enclosed in brackets: [ABC-789].'
INVALID_JIRA_TICKET_MESSAGE = \
'Proper Jira ticket syntax was found, but none were valid tickets. \
Please check the tickets and try again.'
TOO_MANY_JIRA_TICKETS_MESSAGE = \
'Only 1 Jira ticket is allowed per commit. Please commit only 1 change at a time.'
INVALID_ISSUE_TYPE_MESSAGE = \
'You may not commit against subtasks or task-splits. \
Please commit against the parent ticket.'

JIRA_XMLRPC = 'https://jira.example.com/rpc/xmlrpc'
JIRA_USER = 'user'
JIRA_PASSWORD = 'password'
JIRA_TICKET_PATTERN = re.compile(r'\[(\w+?-\d+?)\]')

FAULT_MSG_ISSUE_NOT_FOUND = 'com.atlassian.jira.rpc.exception.RemotePermissionException'

def check_message(message):
    tickets = JIRA_TICKET_PATTERN.findall(message)

    if not tickets:
        return NO_JIRA_TICKET_MESSAGE

    if len(tickets) > 1:
        return TOO_MANY_JIRA_TICKETS_MESSAGE

    ticket = tickets[0]

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

proxy = xmlrpclib.ServerProxy(JIRA_XMLRPC)

try:
    auth = proxy.jira1.login(JIRA_USER, JIRA_PASSWORD)
except:
    print >> sys.stderr, 'Cannot connect to Jira: ' + str(sys.exc_info()[1])
    sys.exit(2)

msg_file = open(sys.argv[1], 'r')
msg = msg_file.read()

err_msg = check_message(msg)

if err_msg:
    print >> sys.stderr, 'Error: %s\nCommit message:\n%s' % (err_msg, msg)
    sys.exit(1)
```

<kbd>Last updated: December 2025</kbd>
