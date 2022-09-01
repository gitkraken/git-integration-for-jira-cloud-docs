---

title: Associating git commits manually to Jira issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/cq3r68b9ou?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top: 5px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/cq3r68b9ou'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The process steps in this section applies to Jira Cloud instance with installed Git Integration for Jira app.
    </div>
    </div>
</div>
<br>

To manually link a git commit to a Jira issue, access the **Change commit issues** feature from the following locations:

*   Projects (sidebar) ➜ **Git Commits** ➜ click _View Full Commit_. Click the Pencil(edit) icon to modify commit associations.

    ![](/wp-content/uploads/gij-gitcloud-view-full-commit-dlg-sel.png)

*   Issue page ➜ **Git Commits** tab ➜ click _View Full Commit_. Click the Pencil(edit) icon to modify commit associations. |

    ![](/wp-content/uploads/gij-gitcloud-view-full-commit-issue-page-sel.png)

*   Jira dashboard menu Apps ➜ **Git Integration: Repository browser** ➜ click a repository _with git commits_. Click the <img src='/wp-content/uploads/gij-edit-icon-dark.png' /> icon on the commit in the repository view.

    ![](/wp-content/uploads/gij-gitcloud-repo-browser-assoc-sel-with-browse.png)

<br>

The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-dropdown.png)

Add, edit or delete linked Jira issue keys in the _**Associated issues to commit**_ field:

*   Click the dropdown arrow and select a Jira issue from the list.
*   The selected Jira issue is associated to the currently configured commit.
*   Repeat the same process to associate one or more Jira issues.
*   Click **X** to remove selected commit association(s).

![](/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-typetext.png)

*   Type a Jira issue key or a word from a Jira issue summary and the list will try to display them.
*   Click a Jira issue from the list to associate it to the currently configure commit.
*   Repeat the same process to associate one or more Jira issues.
*   Click **X** to remove selected commit association(s).

Click **Save** to save the changes.

![(info)](/wp-content/uploads/bbb-info-20.png) JIRA administrators can add/remove any association(s).

![(info)](/wp-content/uploads/bbb-info-20.png) Project administrators can add/remove any association(s) in that project.

![note](/wp-content/uploads/bbb-alert-20.png)The authors of the commit can add/remove the association, if they have the View Development Tools access.


If the commit is associated with multiple Jira issues, you will see the following:

![](/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-multiple.png)

In the above example, the selected commit is associated with Jira issues `TEST-1` and `TEST-4` .

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Saving the changes triggers a repository reindexing to show new associations.
    </div>
    </div>
</div>
<br>

