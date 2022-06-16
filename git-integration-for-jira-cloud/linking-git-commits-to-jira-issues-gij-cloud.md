---

title: Linking git commits to Jira issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
To create a link between your Git commit and a Jira issue, developers must include the issue key into the commit comment.

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/qmumdo048n) _to open this video in a new browser tab for more viewing options._


Commits are selected by issue key. Developers should add them to comments every time the commits are made.

_For example, the “**PRJ-50 fixed issue**” comment – this assumes that you have configured a Jira project with the key ‘**PRJ**’ and someone has created the issue **#50** within this project._

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025229/gitcloud-git-commits-commits-info.png?version=2&modificationDate=1634642210752&cacheVersion=1&api=v2&width=680&height=309)

_Example Git commit message: “**TEST-1 Update…**”._
_In this case, “**TEST-1**” is the issue key linking the commit message to the Jira issue._

Commits that are part of non-master branches will be included only if the master branch doesn't have them.


As a best practice to work with sub-task — put the parent and sub-task Jira issue keys in the commit message so that the commit shows in both places. This way, the commit for the sub-task does not get lost in the many commits of the parent issue.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025229/gitcloud-git-commit-commit-sel-subtask.png?version=1&modificationDate=1634643954720&cacheVersion=1&api=v2&width=680&height=164)

The maximum commit message length limit is **8,000 characters**.


The Git Integration for Jira app supports commits that used the old Jira key in the commit message after a project rename to a new key name (Example: `TEST-16` to `PROJ-16`).

There are two scenarios related to the rename/move:

*   The Jira project key was renamed and the commit message contains the old key prior to the installation of the Git Integration for Jira app.

*   The Jira issue was moved from one project to another project and the message contains the old key prior to the installation of the Git Integration for Jira app.


**Jira Activity Stream**
Only the commits that are linked to Jira issues will show on the Jira Activity Stream (not all commits in repositories).

[Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud)

[Associating git commits manually to Jira issues](/git-integration-for-jira-cloud/associating-git-commits-manually-to-jira-issues-gij-cloud)

