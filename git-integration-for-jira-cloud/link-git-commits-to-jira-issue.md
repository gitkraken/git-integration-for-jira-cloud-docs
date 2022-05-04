---

title: Link git commits to Jira issue
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Link git commits to Jira issue

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/923238543/Link+git+commits+to+Jira+issue>

* * *

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/cs229y2gzj) _and view the video in a new browser tab._

  
Open a Jira issue then go to the Git Commits tab.  In this tab, you will see commits, files changed, links to external repository, commit author and more.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/923238543/git-commits-example.png?version=1&modificationDate=1606547550198&cacheVersion=1&api=v2)

_In the above example, the issue key **GIT-924** text is inserted into a_  
_git commit message to link the commit to this issue._

The git commit will get associated with the Jira issue if the commit message includes the exact issue ID. The Git Integration for Jira app will automatically index new commits and associate the referenced issue. For better readability, place the issue key text at the start of the commit message.  

 Git administrator »

If you want to enforce the commit with a hook, please install this Git commit hook script - [Commit-msg Hook](/wiki/spaces/GITCLOUD/pages/179011603/Commit-msg+Hook).