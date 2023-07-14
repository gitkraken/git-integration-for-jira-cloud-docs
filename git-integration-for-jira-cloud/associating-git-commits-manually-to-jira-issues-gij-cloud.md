---

title: Associating git commits manually to Jira issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/cq3r68b9ou?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px;margin-bottom:35px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/cq3r68b9ou'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

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

To manually link a git commit to a Jira issue, access the **Change commit issues** feature from the following locations:

*   Projects (sidebar) ➜ **Git Commits** ➜ click _View Full Commit_. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon to modify commit associations.

    ![](/wp-content/uploads/gij-gitcloud-view-full-commit-dlg-sel.png)

*   Issue page ➜ **Git Commits** tab ➜ click _View Full Commit_. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon to modify commit associations.

    ![](/wp-content/uploads/gij-gitcloud-view-full-commit-issue-page-sel.png)

*   Jira dashboard menu Apps ➜ **Git Integration: Repository browser** ➜ click a repository _with git commits_. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon on the commit in the repository view.

    ![](/wp-content/uploads/gij-gitcloud-repo-browser-assoc-sel-with-browse.png)

&nbsp;

The following dialog is displayed.

### Method 1

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-dropdown.png' style='margin:25px auto 35px auto;display:block;' />

Add, edit or delete linked Jira issue keys in the _**Associated issues to commit**_ field:

*   Click the dropdown arrow and select a Jira issue from the list.
*   The selected Jira issue is associated to the currently configured commit.
*   Repeat the same process to associate one or more Jira issues.
*   Click **X** to remove selected commit association(s).

### Method 2

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-typetext.png' style='margin:25px auto 35px auto;display:block;' />

*   Type a Jira issue key or a word from a Jira issue summary and the list will try to display them.
*   Click a Jira issue from the list to associate it to the currently configure commit.
*   Repeat the same process to associate one or more Jira issues.
*   Click **X** to remove selected commit association(s).

Click **Save** to save the changes.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        JIRA administrators can add/remove any association(s).
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Project administrators can add/remove any association(s) in that project.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The authors of the commit can add/remove the association, if they have the View Development Tools access.
    </div>
    </div>
</div>

If the commit is associated with multiple Jira issues, you will see the following:

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-multiple.png' style='margin:25px auto 35px auto;display:block;' />

In the above example, the selected commit is associated with Jira issues `TEST-1` and `TEST-4`.

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

&nbsp;
* * *

[**Prev:** Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud/)

[**Next:** Smart commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud/)

