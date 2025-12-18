---

title: Linking git commits to Jira issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

To create a link between your Git commit and a Jira issue, developers must include the issue key into the commit comment.

&nbsp;

**On this page:**
- [How commit linking works](#how-commit-linking-works)
- [Best practices for linking](#best-practices-for-linking)
- [Associating git commits manually to Jira issues](#associating-git-commits-manually-to-jira-issues)
- [How to link branches to a Jira issue](#how-to-link-branches-to-a-jira-issue)
- [How to link pull or merge requests to a Jira issue](#how-to-link-pull-or-merge-requests-to-a-jira-issue)

&nbsp;

* * *

&nbsp;

## How commit linking works

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/cs229y2gzj?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:30px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/cs229y2gzj'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

Commits are selected by issue key. Developers should add them to comments every time the commits are made.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For example, the <b>"PRJ-50 fixed issue"</b> comment – this assumes that you have configured a Jira project with the key <b>'PRJ'</b> and someone has created the issue <b>#50</b> within this project.
    </div>
    </div>
</div>

<img src='/wp-content/uploads/gij-gitcloud-git-commits-commits-info.png' style='margin-top:25px auto;max-width:100%;display:block;' />

<div style='margin-top:10px'><i>Example Git commit message: <b>"TEST-1 Update..."</b><br>
In this case, <b>"TEST-1"</b> is the issue key linking the commit message to the Jira issue.</i></div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Commits that are part of non-master branches will be included only if the master branch doesn't have them.
    </div>
    </div>
</div>

&nbsp;

## Best practices for linking

As a best practice to work with sub-task — put the parent and sub-task Jira issue keys in the commit message so that the commit shows in both places. This way, the commit for the sub-task does not get lost in the many commits of the parent issue.

<img src='/wp-content/uploads/gij-gitcloud-git-commit-commit-sel-subtask.png' style='margin:25px auto' />

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The maximum commit message length limit is <b>8,000 characters</b>.
    </div>
    </div>
</div>

The Git Integration for Jira app supports commits that used the old Jira key in the commit message after a project rename to a new key name (Example: `TEST-16` to `PROJ-16`).

There are two scenarios related to the rename/move:

*   The Jira project key was renamed and the commit message contains the old key prior to the installation of the Git Integration for Jira app.

*   The Jira issue was moved from one project to another project and the message contains the old key prior to the installation of the Git Integration for Jira app.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira Activity Stream</b><br>
        Only the commits that are linked to Jira issues will show on the Jira Activity Stream (not all commits in repositories).
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Associating git commits manually to Jira issues

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

To manually link a git commit to a Jira issue, access the **Change commit issues** feature from the following locations:

*   Projects (sidebar) ➜ **Git Commits** ➜ click _View Full Commit_. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon to modify commit associations.

    ![](/wp-content/uploads/gij-gitcloud-view-full-commit-dlg-sel.png)

*   Issue page ➜ **Git Commits** tab ➜ click _View Full Commit_. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon to modify commit associations.

    ![](/wp-content/uploads/gij-gitcloud-view-full-commit-issue-page-sel.png)

*   Jira dashboard menu Apps ➜ **Git Integration: Repository browser** ➜ click a repository _with git commits_. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon on the commit in the repository view.

    ![](/wp-content/uploads/gij-gitcloud-repo-browser-assoc-sel-with-browse.png)

### Method 1: Using the dropdown

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-dropdown.png' style='margin:25px auto 35px auto;display:block;' />

Add, edit or delete linked Jira issue keys in the _**Associated issues to commit**_ field:

*   Click the dropdown arrow and select a Jira issue from the list.
*   The selected Jira issue is associated to the currently configured commit.
*   Repeat the same process to associate one or more Jira issues.
*   Click **X** to remove selected commit association(s).

### Method 2: Type to search

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-typetext.png' style='margin:25px auto 35px auto;display:block;' />

*   Type a Jira issue key or a word from a Jira issue summary and the list will try to display them.
*   Click a Jira issue from the list to associate it to the currently configured commit.
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

&nbsp;

## How to link branches to a Jira issue

Associate branches to a Jira issue by inserting the Jira issue key to the branch name when creating them.

### Via Git service (GitHub example)

<img src='/wp-content/uploads/gij-github-web-create-branch-sample.png' style='margin:25px auto;max-width:100%;display:block;' />

Create a branch and associate it to a Jira issue:

1.  Select the _master_ branch dropdown.

2.  Enter a new branch name on the search box. Mention a Jira issue key in the name to associate it to the said Jira issue.

3.  Click the result to create the new branch.

### Via Git Integration for Jira app

This can also be easily done via Jira issue Git integration developer panel:

1.  Open a Jira issue.

2.  On the right sidebar, click on **Git Integration**. This opens the Jira issue Git integration developer panel.

3.  Click **Create branch**.

4.  Select a repository.

5.  Select the Source branch to use as base.

6.  The Branch name is automatically generated populated from the issue summary with inserted Jira issue key.

7.  Edit the proposed name but leave the Jira issue key as is or accept the generated branch name as it is.

&nbsp;

* * *

&nbsp;

## How to link pull or merge requests to a Jira issue

Associate pull or merge requests to a Jira issue by inserting the Jira issue key to the pull request when creating them.

### Via Git service

![](/wp-content/uploads/gij-github-web-create-pull-request-sample.png)

Create a pull/merge request and associate it to a Jira issue:

1.  Set base and compare as required. (branch to master)

2.  Enter a new pull request title on the provided box. Mention a Jira issue key in the title to associate it to the said Jira issue.

3.  Also, mentioning a Jira issue key on the description will associate this pull request to the said Jira issue.

### Via Git Integration for Jira app

This can also be easily done via Jira issue Git integration developer panel:

1.  Open a Jira issue.

2.  On the right sidebar, click on **Git Integration**. This opens the Jira issue Git integration developer panel.

3.  Click **Create pull request** or **Create merge request** (GitLab).

4.  Select a repository.

5.  Select the Source branch to use as base.

6.  Select the Target branch to merge the source branch to.

7.  The PR/MR name is automatically generated populated from the issue summary with inserted Jira issue key.

8.  Edit the proposed name but leave the Jira issue key as is or accept the generated name as it is.

&nbsp;

* * *

&nbsp;

[**Prev:** Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud)

[**Next:** Smart commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud)

