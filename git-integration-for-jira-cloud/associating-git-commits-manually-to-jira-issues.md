---

title: Associating git commits manually to Jira issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/cq3r68b9ou) _to open this video in a new browser tab for more viewing options._

The process steps in this section applies to Jira Cloud instance with installed Git Integration for Jira app.


To manually link a git commit to a Jira issue, access the **Change commit issues** feature from the following locations:

|     |
| --- |
| *   Projects (sidebar) ➜ **Git Commits** ➜ click _View Full Commit_. Click the ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) edit icon to modify commit associations. |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-view-full-commit-dlg-sel.png?version=1&modificationDate=1645083351662&cacheVersion=1&api=v2) |

|     |
| --- |
| *   Issue page ➜ **Git Commits** tab ➜ click _View Full Commit_. Click the ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) edit icon to modify commit associations. |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-view-full-commit-issue-page-sel.png?version=1&modificationDate=1645083924640&cacheVersion=1&api=v2) |

|     |
| --- |
| *   Jira dashboard menu Apps ➜ **Git Integration: Repository browser** ➜ click a repository _with git commits_. Click the ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) edit icon on the commit in the repository view. |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-repo-browser-assoc-sel-with-browse.png?version=2&modificationDate=1645085300064&cacheVersion=1&api=v2) |


The following dialog is displayed. Add, edit or delete linked Jira issue keys in the _**Associated issues to commit**_ field.

|     |     |
| --- | --- |
| *   Click the dropdown arrow and select a Jira issue from the list.<br>    <br>*   The selected Jira issue is associated to the currently configured commit.<br>    <br>*   Repeat the same process to associate one or more Jira issues.<br>    <br>*   Click **X** to remove selected commit association(s). | *   Type a Jira issue key or a word from a Jira issue summary and the list will try to display them.<br>    <br>*   Click a Jira issue from the list to associate it to the currently configure commit.<br>    <br>*   Repeat the same process to associate one or more Jira issues.<br>    <br>*   Click **X** to remove selected commit association(s). |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-assoc-commits-dlg-dropdown.png?version=1&modificationDate=1645085650577&cacheVersion=1&api=v2) | ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025256/gitcloud-assoc-commits-dlg-typetext.png?version=1&modificationDate=1645085657664&cacheVersion=1&api=v2) |


Click **Save** to save the changes.

![(info)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/information.png) JIRA administrators can add/remove any association(s).

![(info)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/information.png) Project administrators can add/remove any association(s) in that project.

![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) The authors of the commit can add/remove the association, if they have the View Development Tools access.


If the commit is associated with multiple Jira issues, you will see the following:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025256/gitcloud-assoc-commits-dlg-multiple.png?version=1&modificationDate=1645086506177&cacheVersion=1&api=v2&width=453&height=209)

In the above example, the selected commit is associated with Jira issues `TEST-1` and `TEST-4` .

Saving the changes triggers a repository reindexing to show new associations.

[« Linking git commits to Jira issues](/wiki/spaces/GITCLOUD/pages/1923025229/Linking+git+commits+to+Jira+issues)

[Smart commits »](/git-integration-for-jira-cloud/Smart-commits)

