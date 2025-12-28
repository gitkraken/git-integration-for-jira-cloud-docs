---

title: Linking git commits to Jira issues
description: How to link Git commits, branches, and pull requests to Jira issues
taxonomy:
    category: git-integration-for-jira-cloud

---

To create a link between your Git commit and a Jira issue, developers must include the issue key in the commit comment.

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

## How Commit Linking Works

Commits are selected by issue key. Developers should add them to comments every time they make commits.

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
        Commits that are part of non-master branches are included only if the master branch doesn't have them.
    </div>
    </div>
</div>

&nbsp;

## Best Practices for Linking

As a best practice when working with sub-tasks, put the parent and sub-task Jira issue keys in the commit message so that the commit shows in both places. This way, the commit for the sub-task does not get lost in the many commits of the parent issue.

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

Git Integration for Jira supports commits that used the old Jira key in the commit message after a project rename to a new key name (Example: `TEST-16` to `PROJ-16`).

Two scenarios relate to the rename/move:

*   The Jira project key was renamed and the commit message contains the old key prior to installing Git Integration for Jira.

*   The Jira issue was moved from one project to another project and the message contains the old key prior to installing Git Integration for Jira.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira Activity Stream</b><br>
        Only commits linked to Jira issues appear in the Jira Activity Stream (not all commits in repositories).
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Associating Git Commits Manually to Jira Issues

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The process steps in this section apply to Jira Cloud instances with Git Integration for Jira installed.
    </div>
    </div>
</div>

To manually link a git commit to a Jira issue, access the **Change commit issues** feature from the following locations:

*   Issue page ➜ **Git Commits** tab ➜ click _View Full Commit_. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon to modify commit associations.

    ![](/wp-content/uploads/gij-gitcloud-view-full-commit-issue-page-sel.png-2025.png)

*   Jira dashboard menu Apps ➜ **Git Integration: Repository browser** ➜ click a repository _with git commits_. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon on the commit in the repository view.

    ![](/wp-content/uploads/gij-gitcloud-repo-browser-assoc-sel-with-browse-2025.png)

### Method 1: Using the Dropdown

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-dropdown-2025.png' style='margin:25px auto 35px auto;display:block;' />

Add, edit, or delete linked Jira issue keys in the _**Associated issues to commit**_ field:

*   Click the dropdown arrow and select a Jira issue from the list.
*   The selected Jira issue is associated to the currently configured commit.
*   Repeat the same process to associate one or more Jira issues.
*   Click **X** to remove selected commit association(s).

### Method 2: Type to Search

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-typetext-2025.png' style='margin:25px auto 35px auto;display:block;' />

*   Type a Jira issue key or a word from a Jira issue summary and the list displays matching results.
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
        Jira administrators can add/remove any association(s).
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
        The authors of the commit can add/remove the association if they have the View Development Tools access.
    </div>
    </div>
</div>

If the commit is associated with multiple Jira issues, you see the following:

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-multiple-2025.png' style='margin:25px auto 35px auto;display:block;' />

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

## How to Link Branches to a Jira Issue

Associate branches to a Jira issue by inserting the Jira issue key in the branch name when creating them.

### Via Git Service (GitHub Example)

<img src='/wp-content/uploads/gij-github-web-create-branch-sample.png' style='margin:25px auto;max-width:100%;display:block;' />

Create a branch and associate it to a Jira issue:

1.  Select the _master_ branch dropdown.

2.  Enter a new branch name in the search box. Mention a Jira issue key in the name to associate it to the Jira issue.

3.  Click the result to create the new branch.

### Via Git Integration for Jira App

You can also do this via the Jira issue Git integration developer panel:

1.  Open a Jira issue.

2.  On the right sidebar, click **Git Integration**. This opens the Jira issue Git integration developer panel.

3.  Click **Create branch**.

4.  Select a repository.

5.  Select the Source branch to use as base.

6.  The Branch name is automatically generated from the issue summary with inserted Jira issue key.

7.  Edit the proposed name but leave the Jira issue key as is, or accept the generated branch name as it is.

&nbsp;

* * *

&nbsp;

## How to Link Pull or Merge Requests to a Jira Issue

Associate pull or merge requests to a Jira issue by inserting the Jira issue key in the pull request when creating them.

### Via Git Service

![](/wp-content/uploads/gij-github-web-create-pull-request-sample.png)

Create a pull/merge request and associate it to a Jira issue:

1.  Set base and compare as required. (branch to master)

2.  Enter a new pull request title in the provided box. Mention a Jira issue key in the title to associate it to the Jira issue.

3.  Mentioning a Jira issue key in the description also associates this pull request to the Jira issue.

### Via Git Integration for Jira App

You can also do this via the Jira issue Git integration developer panel:

1.  Open a Jira issue.

2.  On the right sidebar, click **Git Integration**. This opens the Jira issue Git integration developer panel.

3.  Click **Create pull request** or **Create merge request** (GitLab).

4.  Select a repository.

5.  Select the Source branch to use as base.

6.  Select the Target branch to merge the source branch to.

7.  The PR/MR name is automatically generated from the issue summary with inserted Jira issue key.

8.  Edit the proposed name but leave the Jira issue key as is, or accept the generated name as it is.

&nbsp;

* * *

&nbsp;

[**Prev:** Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud)

[**Next:** Smart commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
