---
title: Creating Personal Access Tokens
description: Create personal access tokens (PATs) for GitHub, GitLab, Azure DevOps, TFS, and AWS CodeCommit to authenticate with Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

Personal access tokens (PATs) provide secure authentication for connecting git services to Git Integration for Jira Cloud. This page provides step-by-step instructions for creating PATs on each supported git host.

**On this page:**
- [Create a GitHub or GitHub Enterprise PAT](#create-a-github-or-github-enterprise-pat)
- [Create a GitLab PAT](#create-a-gitlab-pat)
- [Create an Azure DevOps or VSTS PAT](#create-an-azure-devops-or-vsts-pat)
- [Create a TFS 2017+ PAT](#create-a-tfs-2017-pat)
- [Create an Azure DevOps Server PAT](#create-an-azure-devops-server-pat)
- [Create AWS CodeCommit credentials](#create-aws-codecommit-credentials)

&nbsp;
* * *
&nbsp;

## Create a GitHub or GitHub Enterprise PAT

If you enable two-factor authentication for your GitHub account, you must create a PAT to access your git repositories. We recommend enabling two-factor authentication for increased security.

1. Log in to GitHub and go to your profile settings.

    ![](/wp-content/uploads/gij-github-ghe-profile-settings.png)

2. Click **Developer settings** in the sidebar.

    ![](/wp-content/uploads/gij-github-user-settings-sidebar-dev-cfg.png)

3. Click **Personal access tokens** in the sidebar.

4. Click **Generate new token**.

5. Configure your token:

    ![](/wp-content/uploads/gij-jira-cloud-github-mfa-gen-access-token.png)

    a. Enter a descriptive name in the **Note** field (for example, `git-integration-for-jira`).

    b. Set the **Expiration** according to your organization's policies.

    c. Under **Select scopes**, select the **repo** scope (this automatically includes all sub-scopes).

6. Click **Generate token**.

7. Copy the token immediately. This is the only time GitHub displays it.

&nbsp;
* * *
&nbsp;

## Create a GitLab PAT

GitLab uses personal access tokens (PATs) for authentication starting with version 8.8. If you enable two-factor authentication, you must create a PAT to access your repositories.

1. Log in to GitLab and go to your profile settings (**Profile icon** ➜ **Preferences**).

    ![](/wp-content/uploads/gij-gitlab-user-profile-settings.png)

2. Click **Access Tokens** in the sidebar.

    ![](/wp-content/uploads/gij-gitlab-user-settings-sidebar-access-token.png)

3. Configure your token:

    ![](/wp-content/uploads/gij-jira-cloud-gitlab-mfa-gen-access-token.png)

    a. Enter a descriptive **Name** (for example, `Git Integration for Jira`).

    b. Set the **Expiration date** according to your organization's policies, or leave blank for no expiration.

    c. Select the **api** scope.

4. Click **Create personal access token**.

5. Copy the token immediately. This is the only time GitLab displays it.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <b>api</b> scope enables creating branches and merge requests from the Jira issue developer panel.
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

## Create an Azure DevOps or VSTS PAT

PATs let you access Azure Repos without using your username or password directly.

1. In the Azure DevOps portal, click the user settings icon in the top-right corner.

    ![](/wp-content/uploads/gij-vsts-azure-devops-user-profile-settings.png)

2. Click **Personal access tokens**.

3. Click ![(plus)](/wp-content/uploads/gij-icon-add.png) **New Token**.

4. Configure your token:

    ![](/wp-content/uploads/gij-vsts-azure-create-pats-jira-server-cloud.png)

    a. Enter a descriptive name (for example, `git-integration-for-jira`).

    b. Set **Organization** to **All accessible organizations**. This setting is required.

    c. Set the lifespan according to your organization's policies. Select **Custom defined** for longer expiration dates.

    d. Set **Scopes** to **Custom defined**.

    e. Set **Code** to **Read & write**.

5. Click **Create**.

6. Copy the token immediately. Use this token as your password.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>About scopes:</b>
        <ul style='margin-bottom:0px !important'>
            <li><code>Code (read)</code> — View commits, smart commits, and browse repositories</li>
            <li><code>Code (read and write)</code> — All read permissions plus create branches and pull requests from Jira</li>
        </ul>
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

## Create a TFS 2017+ PAT

TFS 2017 and later versions support PATs for on-premises installations.

1. In the TFS portal, click the user settings icon in the top-right corner, then click **Security**.

    ![](/wp-content/uploads/gij-tfs-201718-acct-menu-panel.png)

2. On the Personal Access Token page, click **Add**.

    ![](/wp-content/uploads/gij-tfs-201718-create-pat-screen-sample.png)

3. Enter a descriptive name in **Description**.

4. Set the token lifespan according to your organization's policies.

5. Set **Authorized Scopes** to **Selected scopes**, then choose:
    - **Code (read)** — For viewing commits, smart commits, and browsing repositories
    - **Code (read and write)** — For the above plus creating branches and pull requests from Jira

6. Click **Create token**.

7. Copy the token immediately. Use this token as your password.

&nbsp;
* * *
&nbsp;

## Create an Azure DevOps Server PAT

Azure DevOps Server (formerly Visual Studio Team Foundation Server) supports PATs for on-premises installations.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Azure DevOps Server was previously named Visual Studio Team Foundation Server (TFS).
    </div>
    </div>
</div>

1. In the Azure DevOps Server portal, click your profile icon in the top-right corner, then click **Security**.

    ![](/wp-content/uploads/gij-azure-devops-2019-acct-settings.png)

2. On the Personal Access Token page, click ![(plus)](/wp-content/uploads/gij-icon-add.png) **Add**.

    ![](/wp-content/uploads/gij-azure-devops-2019-pat-settings.png)

3. Enter a descriptive name in **Description**.

4. Set the token lifespan according to your organization's policies.

5. Set **Authorized Scopes** to **Selected scopes**, then choose:
    - **Code (read)** — For viewing commits, smart commits, and browsing repositories
    - **Code (read and write)** — For the above plus creating branches and pull requests from Jira

6. Click **Create token**.

7. Copy the token immediately. Use this token as your password.

&nbsp;
* * *
&nbsp;

## Create AWS CodeCommit Credentials

AWS CodeCommit uses IAM Access Keys instead of personal access tokens. An Access Key ID and Secret Access Key serve the same purpose as a PAT.

### Required IAM Permissions

Grant these [AWS CodeCommit IAM Policy actions](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_awscodecommit.html) to enable branch and pull request creation from Jira:

- `CodeCommit:Write:CreateBranch`
- `CodeCommit:Write:CreatePullRequest`

### Create an Access Key

1. In AWS IAM, go to **Users** ➜ select your user ➜ **Security credentials**.

2. Click **Create access key**.

    ![](/wp-content/uploads/gij-IAM-user-create-access-key-diagram.png)

3. Copy both the Access Key ID and Secret Access Key immediately.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        AWS IAM allows a maximum of two Access Keys per IAM user.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Create a dedicated IAM user for Git Integration for Jira tasks. Do not share Access Keys with other applications.
    </div>
    </div>
</div>

<kbd>Last updated: December 2025</kbd>
