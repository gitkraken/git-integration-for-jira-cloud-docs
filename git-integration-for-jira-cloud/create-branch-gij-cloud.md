---

title: Create Branch and Pull/Merge Request
description: Learn how to create branches and pull/merge requests directly from Jira issues using Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud

---

<!-- FEATURES -->

The Git Integration for Jira app adds two features to the Jira issue developer panel – **Create branch** and **Create pull/merge request**. For more information on where to access them, see the [Jira Git integration development panel documentation](/git-integration-for-jira-cloud/jira-issue-page-gij-cloud#jira-git-integration-development-panel).

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
       Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>On this page:</b><br>
        <ul style='margin-bottom:0px;'>
            <li><a href='#default-branch'>Default branch</a></li>
            <li><a href='#create-branch'>Create branch</a></li>
            <li><a href='#create-pull-or-merge-request'>Create pull or merge request</a></li>
        </ul>
    </div>
    </div>
</div>

&nbsp;

## Default branch

Most git integrations allow changing the default branch of the repository/project to something other than "master". This change reflects in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this feature where Git Integration for Jira app retrieves the default branch from almost all integrations and applies this setting at the repository level. For Gerrit, the default main branch is always "master".

You can only change the main branch for repositories within an integration on the git server.

&nbsp;

* * *

&nbsp;

## Create branch

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira administrator notes</b><br>
        <ul style='margin-bottom:0px'>
            <li>
                Jira users can provide their own personal access tokens (PAT) even if the Jira admin does not require them. See <a href="/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud">Require Personal Access Tokens for user actions (create branch/pull request)</a> for configuration instructions.
            </li>
            <li>
                The <b>View developer tools</b> <i>permission</i> is required to view the Source Code panel (see more in <a href='/git-integration-for-jira-cloud/issue-git-source-code-panel-gij-cloud'>Issue Git Source Code Panel</a>). Jira users must also have the <b>Browse Project</b> <i>permissions</i> to a project associated with a repository to view.
            </li>
            <li>
                You can disable the create branch feature for all Jira users (regardless of permissions) in <a href="/git-integration-for-jira-cloud/general-settings-gij-cloud#git-integration-options">General settings</a>.
            </li>
        </ul>
    </div>
    </div>
</div>

The Create branch feature allows Jira users to create a git branch directly from the Jira issue.

![](/wp-content/uploads/gij-gitcloud-create-branch-dlg.png)

&nbsp;

### Advantages of creating branches from Jira

When you create a branch from within Jira:

- The branch name automatically includes the issue key (necessary for branch ↔ issue association) and issue summary.

- You can customize default branch naming conventions to match your development workflow. For example: `${issuetype:New Issue,new,Bug Fix,bug}/${issuekey}-${summary}` generates "`bug/PRJ-123-add-more-logging`" (See [General settings](/git-integration-for-jira-cloud/general-settings-gij-cloud) for more information).

- You can require each Jira user to provide their Personal Access Token for creating branches. This option adds friction to creating branches/pull requests but enforces git server user permissions and provides better attribution for actions. See [Require Personal Access Tokens for user actions (create branch/pull request)](/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud) for more information.

- Each Jira user can set a **Default repository** for the current Jira project. (See [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) for more information).

&nbsp;

### Supported platforms for Create branch

- Full feature integrations:
    - GitHub
    - GitLab
    - Bitbucket Cloud
    - AWS CodeCommit
    - Azure DevOps
    - Microsoft Visual Studio Team Services (VSTS)
    - Microsoft Team Foundation Server (TFS)

- Supported in the Atlassian Jira Cloud [iOS](https://www.atlassian.com/software/jira/mobile-app), [Android](https://www.atlassian.com/software/jira/mobile-app), and [MacOS](https://www.atlassian.com/software/jira/mac) apps.

- Company-managed and Team-managed Jira projects supported.

- New and old Jira Issue View supported.

&nbsp;

### Steps to creating a git branch in Jira

1. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>PREREQUISITE</b> A Jira administrator configures a Full feature integration in the Git Integration for Jira Cloud app. See the <a href='/git-integration-for-jira-cloud/integration-guide-gij-cloud'>Integration Guide</a> for more information.

2. To access the Create branch action, do one of the following:
    - Enable the **Git Development panel**, or
    - Open the [Issue Git Source Code Panel](/git-integration-for-jira-cloud/issue-git-source-code-panel-gij-cloud)

3. Click **Create branch** in one of the panels from step 2.

4. Select a git repository.
    - Optional: Designate the repository as the default selected repository for the current Jira project. To configure default repositories for more than one Jira project, use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.
    - Use the search box to find the specific repository.

5. If a [personal access token is required](/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud) (and not yet provided), follow the on-screen instructions to provide a [personal access token](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) with the correct permissions for the selected repository.

6. Select a base branch.

7. Verify the branch name is correct. Edit as desired. Note: The Jira issue key must remain in the branch name to create the branch ↔ Jira issue association.

8. Click **Create branch**.

Make a commit to this branch, then continue to create a pull/merge request.

&nbsp;

* * *

&nbsp;

## Create pull or merge request

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira administrator notes</b><br>
        <ul style='margin-bottom:0px'>
            <li>
                Jira users can provide their own personal access tokens (PAT) even if the Jira admin does not require them. See <a href="/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud">Require Personal Access Tokens for user actions (create branch/pull request)</a> for configuration instructions.
            </li>
            <li>
                The <b>View developer tools</b> <i>permission</i> is required to view the Source Code panel (see more in <a href="/git-integration-for-jira-cloud/issue-git-source-code-panel-gij-cloud">Issue Git Source Code Panel</a>). Jira users must also have the <b>Browse Project</b> <i>permissions</i> to a project associated with a repository to view.
            </li>
            <li>
                You can disable the create pull request feature for all Jira users (regardless of permissions) in <a href="/git-integration-for-jira-cloud/general-settings-gij-cloud#git-integration-options">General settings</a>.
            </li>
        </ul>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>GitLab note</b><br>
        GitLab uses the term Merge Request rather than Pull Request (used by other major git services). In this article, Pull Request and Merge Request are interchangeable.
    </div>
    </div>
</div>

The **Create pull request** feature allows Jira users to create a git pull request directly from the Jira issue.

![](/wp-content/uploads/gij-gitcloud-create-pull-req-dlg-2025.png)

&nbsp;

### Advantages of creating pull requests from Jira

When you create a pull request from within Jira:

- The pull request title automatically includes the issue key (necessary for pull request ↔ issue association) and issue summary.

- You can require each Jira user to provide their Personal Access Token for creating pull requests. This option adds friction to creating pull requests/branches but enforces git server user permissions and provides better attribution for actions. See [Require Personal Access Tokens for user actions (create branch/pull request)](/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud) for more information.

- Each Jira user can set a **Default repository** for the current Jira project. (See User settings for more information).

&nbsp;

### Supported platforms for Create pull request

- Full feature integrations:
    - GitHub
    - GitLab
    - Bitbucket Cloud
    - AWS CodeCommit
    - Azure DevOps
    - Microsoft Visual Studio Team Services (VSTS)
    - Microsoft Team Foundation Server (TFS)

- Supported in the Atlassian Jira Cloud [iOS](https://www.atlassian.com/software/jira/mobile-app), [Android](https://www.atlassian.com/software/jira/mobile-app), and [MacOS](https://www.atlassian.com/software/jira/mac) apps.

- Company-managed and Team-managed Jira projects supported.

- New and old Jira Issue View supported.

&nbsp;

### Steps to creating a git pull request in Jira

1. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>PREREQUISITE</b> A Jira administrator configures a Full feature integration in the Git Integration for Jira Cloud app. See the <a href='/git-integration-for-jira-cloud/integration-guide-gij-cloud'>Integration Guide</a> for more information.

    <div class="bbb-callout bbb--alert">
        <div class="irow">
        <div class="ilogobox">
            <span class="logoimg"></span>
        </div>
        <div class="imsgbox">
            <b>Important</b><br>
            The source branch for the pull/merge request must have a commit. You must fulfill this condition to create a pull/merge request via the Jira Git Integration panel.
        </div>
        </div>
    </div>

2. To access the Create pull/merge request action, do one of the following:
    - Enable the **Git Development panel**, or
    - Open the [Issue Git Source Code Panel](/git-integration-for-jira-cloud/issue-git-source-code-panel-gij-cloud)

3. Click **Create pull request** in one of the panels from step 2.

4. Select a git repository.
    - Optional: Designate the repository as the default selected repository for the current Jira project. To configure default repositories for more than one Jira project, use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.
    - Use the search box to find the specific repository.

5. If a [personal access token is required](/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud) (and not yet provided), follow the on-screen instructions to provide a [personal access token](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) with the correct permissions for the selected repository.

6. Select a source branch.

7. Select a target branch.

8. Verify the pull request title is correct. Edit as desired. Note: The Jira issue key must remain in the pull request name to create the pull request ↔ Jira issue association.

9. Click **Create pull request**.

&nbsp;

### Associating pull/merge request to Jira issue

A git service user can create a PR/MR via the Git host service portal by adding a Jira issue key in the PR/MR title. The system automatically adds this to the Pull/Merge request list in the Jira issue Git developer panel.

| Git service portal |
| :---: |
| ![](/wp-content/uploads/gij-gitcloud-git-host-pull-req-assoc-test.png) |

| Jira issue PR/MR list view |
| :---: |
| ![](/wp-content/uploads/gij-gitcloud-jira-dev-panel-pull-req-list-assoc-sel-2025.png) |

Additionally, creating a PR/MR via the Git developer panel automatically associates the PR/MR with the Jira issue.

&nbsp;

* * *

&nbsp;

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If you still have a question, reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

<kbd>Last updated: December 2025</kbd>
