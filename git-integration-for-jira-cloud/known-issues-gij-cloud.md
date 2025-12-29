---
title: Known Issues (GIJ Cloud)
description: Known issues and workarounds for Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This page documents known issues and limitations in Git Integration for Jira Cloud along with available workarounds.

**On this page:**
- [Repository limits per integration](#repository-limits-per-integration)
- [2GB object size limit](#2gb-object-size-limit)
- [Smart commits user search issue](#smart-commits-user-search-issue)
- [Microsoft pull request status updates](#microsoft-pull-request-status-updates)
- [Microsoft PAT organization permission](#microsoft-pat-organization-permission)
- [SSH repository automation triggers](#ssh-repository-automation-triggers)
- [Tag loading timeout](#tag-loading-timeout)
- [Left sidebar loading delay](#left-sidebar-loading-delay)
- [Duplicate Smart Commit commands](#duplicate-smart-commit-commands)
- [Web links not updating](#web-links-not-updating)

&nbsp;
* * *
&nbsp;

## Repository Limits Per Integration

Git Integration for Jira Cloud limits the number of connected repositories per integration:

| Git Service | Maximum Repositories |
|-------------|---------------------|
| GitHub | 10,000 |
| GitLab | 10,000 |
| All others | 10,000 |

_Reference: GITCL-1395, GITCL-1846_

&nbsp;

## 2GB Object Size Limit

Git Integration for Jira uses the JGit library, which does not support objects over 2GB in size stored in git repositories.

**Workaround:** Remove large objects from repository history or use Git LFS for large files.

&nbsp;

## Smart Commits User Search Issue

Some users have smart commits attributed to the app user rather than specific users when user search via email fails.

**Workaround:** Use the assignable users API endpoint:

```
/rest/api/2/user/assignable/search?issueKey=ABC-123
```

_Reference: GITCL-800_

&nbsp;

## Microsoft Pull Request Status Updates

Microsoft integrations require all pull requests for configured repositories to be requested each time for status updates. Microsoft's Pull Request APIs do not provide filtering by last changed date/time.

_Reference: GIT-3889_

&nbsp;

## Microsoft PAT Organization Permission

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b>

When creating personal access tokens (PAT) for Microsoft/Azure integrations, select **All accessible organizations**. Otherwise, the integration will not work.

See [Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) for instructions.

For more information, see the [official Azure DevOps PAT documentation](https://developercommunity.visualstudio.com/content/problem/902833/azure-devops-personal-access-token-does-).

_Reference: GIT-3978_

&nbsp;

## SSH Repository Automation Triggers

Automation for Jira triggers work with auto-connected integrations and single HTTPS authenticated git repositories, but single repositories authenticated via SSH are not supported by Atlassian Jira Cloud.

See Atlassian bug: [JSWCLOUD-20935](https://jira.atlassian.com/browse/JSWCLOUD-20935)

**Workaround:** Use HTTP/HTTPS connections for single repository git URLs:

| Connection Type | Example | Trigger Support |
|-----------------|---------|-----------------|
| SSH (not supported) | `git@github.com:admin/repo.git` | ❌ |
| HTTPS (supported) | `https://github.com/admin/repo.git` | ✅ |

_Reference: GITCL-1624_

&nbsp;

## Tag Loading Timeout

Loading tags on integrations with large git history can take a long time. Git Integration for Jira Cloud limits tag loading to **10 seconds** before timing out.

&nbsp;

## Left Sidebar Loading Delay

The Git Integration for Jira app panel in the left sidebar takes up to 10 seconds to load.

![](/wp-content/uploads/gij-left-sidebar-loading-delay-bug-example.png)

Atlassian has opened a [bug ticket](https://ecosystem.atlassian.net/browse/ACJIRA-2415) for this issue.

&nbsp;

## Duplicate Smart Commit Commands

When both Atlassian and GitKraken Smart Commit processors are enabled, users see duplicate `#comment` and `#time` commands.

![](/wp-content/uploads/gij-gitcloud-gencfg-dup-smart-commits-sel.png)

| Processor | Commands Supported |
|-----------|-------------------|
| Atlassian | `#comment`, `#time`, `#<transition>` + workflow triggers |
| GitKraken | `#comment`, `#time`, `#<transition>`, `#assign`, `#label` |

**Recommendation:** Use Atlassian processor (default) for workflow trigger support. Use GitKraken processor only if you need `#assign` and `#label` commands.

_Reference: GITCL-1334_

&nbsp;

## Web Links Not Updating

In rare cases, web links for branches and tags do not update automatically after modifying the web-linking template.

**Workaround:**

![](/wp-content/uploads/gij-cloud-disable-reenable-plain-git-repo-via-actions.png)

1. Temporarily disable the affected Plain Git integration.
2. Re-enable the integration to apply the web linking update.

_Reference: GITCL-3981_

<kbd>Last updated: December 2025</kbd>
