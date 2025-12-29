---
title: Linking git commits to Jira issues
description: How to link Git commits, branches, and pull requests to Jira issues
taxonomy:
    category: git-integration-for-jira-cloud
---

Link your git commits to Jira issues by including the issue key in the commit message.

**On this page:**
- [Understand commit linking](#understand-commit-linking)
- [Follow best practices for linking](#follow-best-practices-for-linking)
- [Associate commits manually](#associate-commits-manually)
- [Link branches to a Jira issue](#link-branches-to-a-jira-issue)
- [Link pull or merge requests to a Jira issue](#link-pull-or-merge-requests-to-a-jira-issue)

&nbsp;
* * *
&nbsp;

## Understand Commit Linking

Git Integration for Jira selects commits by issue key. Include issue keys in your commit messages every time you commit.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Example:</b> The commit message <b>"PRJ-50 fixed issue"</b> links to issue #50 in the PRJ project. This assumes you have a Jira project with the key "PRJ" and someone created issue #50 within that project.
    </div>
    </div>
</div>

<img src='/wp-content/uploads/gij-gitcloud-git-commits-commits-info.png' style='margin-top:25px auto;max-width:100%;display:block;' />

<div style='margin-top:10px'><i>Example: The commit message <b>"TEST-1 Update..."</b> links to Jira issue TEST-1.</i></div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Commits from non-master branches appear only if the master branch does not contain them.
    </div>
    </div>
</div>

&nbsp;

## Follow Best Practices for Linking

When working with sub-tasks, include both the parent and sub-task issue keys in your commit message. This approach:
- Displays the commit in both places
- Prevents sub-task commits from getting lost among parent issue commits

<img src='/wp-content/uploads/gij-gitcloud-git-commit-commit-sel-subtask.png' style='margin:25px auto' />

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The maximum commit message length is <b>8,000 characters</b>.
    </div>
    </div>
</div>

### Support for Renamed Projects

Git Integration for Jira supports commits that use the old Jira key after a project rename (for example, `TEST-16` to `PROJ-16`).

Two scenarios apply after a rename or move:
- The Jira project key was renamed and the commit message contains the old key (from before you installed Git Integration for Jira)
- A Jira issue was moved to another project and the message contains the old key (from before you installed Git Integration for Jira)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira Activity Stream:</b> Only commits linked to Jira issues appear in the Activity Stream—not all commits from connected repositories.
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

## Associate Commits Manually

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        These steps apply to Jira Cloud instances with Git Integration for Jira installed.
    </div>
    </div>
</div>

Access the **Change commit issues** feature from two locations:

**From the Issue Page:**
1. Open the issue page.
2. Go to the **Git Commits** tab.
3. Click **View Full Commit**.
4. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon to modify associations.

![](/wp-content/uploads/gij-gitcloud-view-full-commit-issue-page-sel.png-2025.png)

**From the Repository Browser:**
1. Go to **Apps** ➜ **Git Integration: Repository browser**.
2. Click a repository that contains commits.
3. Click the ![edit](/wp-content/uploads/gij-edit-icon-dark.png) icon on the commit you want to modify.

![](/wp-content/uploads/gij-gitcloud-repo-browser-assoc-sel-with-browse-2025.png)

### Method 1: Use the Dropdown

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-dropdown-2025.png' style='margin:25px auto 35px auto;display:block;' />

1. Click the dropdown arrow in the **Associated issues to commit** field.
2. Select a Jira issue from the list.
3. Repeat to associate additional issues.
4. Click **X** next to an issue to remove that association.
5. Click **Save** to apply changes.

### Method 2: Type to Search

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-typetext-2025.png' style='margin:25px auto 35px auto;display:block;' />

1. Type a Jira issue key or a word from an issue summary.
2. Select a matching issue from the results.
3. Repeat to associate additional issues.
4. Click **X** next to an issue to remove that association.
5. Click **Save** to apply changes.

### Association Permissions

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Jira administrators can add or remove any associations.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Project administrators can add or remove associations within their projects.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Commit authors can add or remove their own associations if they have <b>View Development Tools</b> access.
    </div>
    </div>
</div>

### Multiple Associations

If a commit is associated with multiple Jira issues, you see all linked issues in the dialog:

<img src='/wp-content/uploads/gij-gitcloud-assoc-commits-dlg-multiple-2025.png' style='margin:25px auto 35px auto;display:block;' />

In this example, the commit is associated with issues `TEST-1` and `TEST-4`.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Saving changes triggers a repository reindex to display the new associations.
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

## Link Branches to a Jira Issue

Include the Jira issue key in the branch name when you create a new branch.

### Create a Branch in Your Git Service (GitHub Example)

<img src='/wp-content/uploads/gij-github-web-create-branch-sample.png' style='margin:25px auto;max-width:100%;display:block;' />

1. Click the branch dropdown (showing **master** or your current branch).
2. Enter a new branch name that includes the Jira issue key.
3. Click the result to create the branch.

### Create a Branch from Jira

1. Open a Jira issue.
2. Click **Git Integration** in the right sidebar.
3. Click **Create branch**.
4. Select a repository.
5. Select the source branch to use as a base.
6. Edit the proposed branch name if needed, but keep the Jira issue key.
7. Click **Create branch**.

&nbsp;
* * *
&nbsp;

## Link Pull or Merge Requests to a Jira Issue

Include the Jira issue key in the pull request title or description when you create a new PR/MR.

### Create a Pull Request in Your Git Service

![](/wp-content/uploads/gij-github-web-create-pull-request-sample.png)

1. Set the base and compare branches (for example, feature branch to master).
2. Enter a title that includes the Jira issue key.
3. Optionally, include the Jira issue key in the description for additional linking.
4. Submit the pull request.

### Create a Pull Request from Jira

1. Open a Jira issue.
2. Click **Git Integration** in the right sidebar.
3. Click **Create pull request** (or **Create merge request** for GitLab).
4. Select a repository.
5. Select the source branch.
6. Select the target branch.
7. Edit the proposed name if needed, but keep the Jira issue key.
8. Submit the request.

&nbsp;
* * *
&nbsp;

[**Prev:** Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud)

[**Next:** Smart commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
