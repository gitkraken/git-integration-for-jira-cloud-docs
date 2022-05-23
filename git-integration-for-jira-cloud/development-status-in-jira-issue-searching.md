---

title: Development status in Jira issue searching
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
In the Jira search interface you will have a new column to add: **Development**.

This column is displayed in the following order of precedence:

1.  **Blank** (no commits or pull requests are declined/closed)

2.  **\# of Commits** (when no pull requests are associated)

3.  **Merged** (all associated pull requests are merged or closed)

4.  **Under Review** (at least one associated pull request is open)


![](https://bigbrassband.atlassian.net/wiki/download/attachments/1940914287/image-20200724-103833.png?version=1&modificationDate=1631349148620&cacheVersion=1&api=v2)

