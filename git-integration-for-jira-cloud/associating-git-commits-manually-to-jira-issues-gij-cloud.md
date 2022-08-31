---

title: Associating git commits manually to Jira issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/cq3r68b9ou) _to open this video in a new browser tab for more viewing options._

The process steps in this section applies to Jira Cloud instance with installed Git Integration for Jira app.


To manually link a git commit to a Jira issue, access the **Change commit issues** feature from the following locations:

*   Projects (sidebar) ➜ **Git Commits** ➜ click _View Full Commit_. Click the Pencil(edit) icon to modify commit associations.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-view-full-commit-dlg-sel.png?version=1&modificationDate=1645083351662&cacheVersion=1&api=v2)

*   Issue page ➜ **Git Commits** tab ➜ click _View Full Commit_. Click the Pencil(edit) icon to modify commit associations. |

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-view-full-commit-issue-page-sel.png?version=1&modificationDate=1645083924640&cacheVersion=1&api=v2)

*   Jira dashboard menu Apps ➜ **Git Integration: Repository browser** ➜ click a repository _with git commits_. Click the <img src='/wp-content/uploads/gij-edit-icon-dark.png' /> icon on the commit in the repository view.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-repo-browser-assoc-sel-with-browse.png?version=2&modificationDate=1645085300064&cacheVersion=1&api=v2)

<br>

The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-assoc-commits-dlg-dropdown.png?version=1&modificationDate=1645085650577&cacheVersion=1&api=v2)

Add, edit or delete linked Jira issue keys in the _**Associated issues to commit**_ field:

*   Click the dropdown arrow and select a Jira issue from the list.
*   The selected Jira issue is associated to the currently configured commit.
*   Repeat the same process to associate one or more Jira issues.
*   Click **X** to remove selected commit association(s).

* * *

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-assoc-commits-dlg-typetext.png?version=1&modificationDate=1645085657664&cacheVersion=1&api=v2)

*   Type a Jira issue key or a word from a Jira issue summary and the list will try to display them.
*   Click a Jira issue from the list to associate it to the currently configure commit.
*   Repeat the same process to associate one or more Jira issues.
*   Click **X** to remove selected commit association(s).

Click **Save** to save the changes.

![(info)](/wp-content/uploads/bbb-info-20.png) JIRA administrators can add/remove any association(s).

![(info)](/wp-content/uploads/bbb-info-20.png) Project administrators can add/remove any association(s) in that project.

The authors of the commit can add/remove the association, if they have the View Development Tools access.


If the commit is associated with multiple Jira issues, you will see the following:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025256/gitcloud-assoc-commits-dlg-multiple.png?version=1&modificationDate=1645086506177&cacheVersion=1&api=v2&width=453&height=209)

In the above example, the selected commit is associated with Jira issues `TEST-1` and `TEST-4` .

Saving the changes triggers a repository reindexing to show new associations.

