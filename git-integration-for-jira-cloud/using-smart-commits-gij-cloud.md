---

title: Using Smart Commits
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Smart Commits enable users to perform actions on Jira issues from a single commit. In a commit message, enter the issue key and some desired action such as resolving an issue, closing an issue, time tracking or all of them.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/923664519/smart-commit-example.png?version=1&modificationDate=1606548093273&cacheVersion=1&api=v2&width=510&height=157)

For example, if a user wants to log specified time with worklog comment, adds a comment, and resolve the issue TEST-100, enter the commit message as follows:

**TEST-100 #time** 2h 30m _Fixed code_ **#comment** _Merge to master_ **#resolve**

Enable/disable this feature via:

*   Connect to Git repository wizard (first screen)

*   Manage Git repositories ➜Actions ➜ **Edit repository settings** ➜ Smart Commits and Workflow Triggers

*   Manage Git repositories ➜Actions ➜ **Show integration repositories** ➜ click a repository ➜ Smart Commits and Workflow Triggers


See our [Smart Commits Overview](/git-integration-for-jira-cloud/smart-commits-overview-gij-cloud) to learn further about syntax and structure; then follow the link at the bottom of that page to learn more information on advanced syntax.