---

title: User Guide - GIJ Cloud
description: End user guide for Git Integration for Jira Cloud - learn how to view and create Git data in Jira
taxonomy:
    category: git-integration-for-jira-cloud

---

## Introduction to GIJ

Thank you for using Git Integration for Jira! This guide explains how Git information displays in Jira through our application.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Have an idea for an improvement or want to request a specific feature? Submit a feature request on our <a href='https://gitkraken.canny.io/git-integration-for-jira-feedback'>Feature Request Board</a>.
    </div>
    </div>
</div>

&nbsp;

## Jira Issue View

GIJ displays commits, branches, and pull/merge requests associated with a specific Jira issue. To link items to a Jira issue, include the Jira issue key in the commit message, branch name, or pull/merge request title.

See [Linking Git Commits](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud/) for more details.

**Breakdown of information provided by GIJ in Jira issues:**

![Jira Issue View](/wp-content/uploads/Jira-Issue-Breakdown-2025.png)

**Activity Stream - Git Commits**

1. Git Commits tab in the activity stream, organized by repository
2. Individual commit with the developer who made it
3. Commit message
4. Commit line change summary by file
5. Link to view code diff in Jira

**Git Integration Panel**

6. Options to create a branch or pull request directly from a Jira issue
7. Associated branches and pull requests with status icons

The [Git Rollup Tab](/git-integration-for-jira-cloud/git-roll-up-tab-gij-cloud/) shows a summary of files, lines changed, and the developers who made changes associated with the Jira issue.

![Git Rollup Tab](/wp-content/uploads/gij-gitcloud-jira-issue-rollup-tab-2025.png)

&nbsp;

## Linking Behavior

GIJ uses the Jira issue key to determine whether repository activity (commits, branches, pull/merge requests) links to any Jira items. Include the Jira issue key in the commit message, branch name, or pull request title. The key can appear anywhere in the message or name.

See [Linking Git Commits to Jira Issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud/) for more details.

![Jira Issue Key](/wp-content/uploads/Jira-Issue-key-linking-cloud.png)

![Commit Example](/wp-content/uploads/Linking-Commit-example.png)

![Pull request Example](/wp-content/uploads/Pull-Request-Linking-Example.png)

&nbsp;

## Creating Branches

You can [create branches](/git-integration-for-jira-cloud/create-branch-gij-cloud/) directly from a Jira issue using GIJ.

**To create a branch:**

1. Open the Git Integration panel from the right side of the Jira issue.
2. Click **Create branch**.

![Create Branch 1](/wp-content/uploads/Enduserguide-Cloud-Create-Branch-1-2025.png)

3. Select the repository to create the branch in.
4. Select the source branch.
5. Enter the branch name. Make sure the Jira issue key is included.
6. Click **Create branch**.

![Create Branch 2](/wp-content/uploads/Enduserguide-Cloud-Create-Branch-2-2025.png)

A confirmation popup appears after the branch is created. Click the link to open the newly created branch directly.

&nbsp;

## Creating Pull/Merge Requests

You can [create pull/merge requests](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud/) directly from Jira using GIJ.

**To create a pull/merge request:**

1. Open the Git Integration panel from the right side of the Jira issue.
2. Click **Create Pull Request** or **Create Merge Request**.

![Create PR 1](/wp-content/uploads/Enduserguide-Cloud-Creating-PR-1-2025.png)

3. Select the repository.
4. Select the source and target branches.
5. Verify the title contains the Jira issue key.
6. Click **Create pull/merge request**.

![Create PR 2](/wp-content/uploads/Enduserguide-Cloud-Creating-PR-2-2025.png)

A confirmation popup appears after the pull/merge request is created. Click the link to open it directly.

&nbsp;

## GIJ User Settings

GIJ lets you manage your connected apps, default repository, default branch, and personal access tokens through the [GIJ User Settings](/git-integration-for-jira-cloud/user-settings-gij-cloud/) page.

**To access User Settings:**

1. Click your Jira profile picture icon.
2. Select **Git Integration: User Settings**.

![User-Settings](/wp-content/uploads/GIJ-General-Settings-navigation-cloud-2025.png)

### Connected Apps

Enable or disable the visibility of GitKraken and GitLens icons in Jira issues. These icons let you open specific Git items in the respective application directly from the issue.

![Connected Apps](/wp-content/uploads/GIJ-Cloud-User-Settings-Connnected-Apps.png)

![Connected Apps - icons](/wp-content/uploads/GIJ-Connected-Apps-Jiraissue-icons-2025.png)

### Default Repository

Set a default repository on a per-project basis.

![Default-repo](/wp-content/uploads/GIJ-Cloud-User-Settings-Default-Repo.png)

### Default Branch

Set a default branch for a specific repository, configured by Jira project.

![Default-Branch](/wp-content/uploads/GIJ-Cloud-User-Settings-Default-Branch.png)

### Personal Access Tokens

Manage the personal access tokens used to authenticate your requests to create branches and pull requests directly from Jira. You need to provide a token for each integration.

You can enter an existing personal access token or click the link to create a new token. The link takes you directly to the token creation page for that Git service.

See [Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud/) for detailed instructions.

![PAT](/wp-content/uploads/GIJ-Cloud-User-Settings-PAT.png)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
