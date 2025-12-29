---
title: Require Personal Access Tokens for user actions (create branch/pull request)
description: Configure Git Integration for Jira Cloud to require personal access tokens for user actions like creating branches and pull requests.
taxonomy:
    category: git-integration-for-jira-cloud
---

**On this page:**
- [Understand user attribution](#understand-user-attribution)
- [Enable the Require User PAT setting](#enable-the-require-user-pat-setting)
- [User experience after enabling](#user-experience-after-enabling)
- [Supported integrations](#supported-integrations)

&nbsp;
* * *
&nbsp;

## Understand User Attribution

By default, Git Integration for Jira performs branch and pull request creation using the integration account (the account used for indexing). This means all actions appear as if the integration account performed them.

![](/wp-content/uploads/gij-jira-cloud-create-branch-example-01-2025.png)

For teams that need to track who performed each action, Jira administrators can require individual users to provide their own personal access tokens. This ensures each user's git service account is attributed to their actions.

&nbsp;

## Enable the Require User PAT Setting

1. Go to **Manage Git repositories**.

2. Add a new integration or click ![](/wp-content/uploads/actions-icon.png) **Actions** ➜ **Edit integration settings** for an existing integration.

    ![](/wp-content/uploads/gij-req-pat-gitmgr-actions-edit-git-settings-2025.png)

3. Locate the **Require User PAT** setting.

    ![](/wp-content/uploads/gij-req-pat-gitmgr-page-actions-control-cfg-2025.png)

4. Select the checkbox to enable the requirement.

5. Click **Update** to save your changes.

&nbsp;

## User Experience After Enabling

### Initial Setup Prompt

When a user tries to create a branch or pull request, they see a message indicating setup is required:

![](/wp-content/uploads/gij-req-pat-create-branch-dlg-setup-your-pat-2025.png)

### Enter Personal Access Token

Clicking the setup link takes the user to **User settings** where they enter their PAT:

![](/wp-content/uploads/gij-req-pat-seruo-pat-dlg-2025.png)

If the user does not have a token or their existing token has expired, they can click **New token** to generate one. See [Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) for instructions.

### After Token Configuration

With a valid PAT saved, the user can create branches and pull requests normally:

![](/wp-content/uploads/gij-req-pat-create-branch-dlg-after-pat-is-setup-2025.png)

### Important Notes

- PATs are saved per integration by individual Jira users
- The same token applies to both branch and pull request creation
- Users must have **View Development Tools** permission in the Jira project context to view Git Integration for Jira content

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>TFS 2013 and TFS 2015 limitation:</b> These versions do not support PATs. If you enable <b>Require User PAT</b> for these integrations, users cannot create or delete branches and pull requests.
    </div>
    </div>
</div>

&nbsp;

## Supported Integrations

User attribution with personal access tokens works with these integrations:

- GitHub.com
- GitHub Enterprise
- GitLab.com
- GitLab self-managed
- Microsoft Azure DevOps
- Microsoft Visual Studio Team Services (VSTS)
- Microsoft Team Foundation Server (TFS 2017+)
- AWS CodeCommit

&nbsp;

<div style='border-top: 1px solid #456; width: 40%; padding-bottom: 12px'></div>
<div style='font-size: 12px;'>
    <sup>1</sup> <i>Logo owned by <a href='https://gitlab.com/'>GitLab Inc</a> used under <a href='https://creativecommons.org/licenses/by-nc-sa/4.0/'>license</a>.
    <p>&nbsp;&nbsp;All product names, logos, and brands are property of their respective owners.<p><i>
</div>

<kbd>Last updated: December 2025</kbd>
