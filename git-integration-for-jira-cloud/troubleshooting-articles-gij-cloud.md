---
title: Troubleshooting articles
description: Solutions and workarounds for common issues with Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This collection of troubleshooting guides provides workarounds and solutions to help you get up and running with Git Integration for Jira Cloud.

**On this page:**
- [Why don't I see commits?](#why-dont-i-see-commits)
- [License expiration session error](#license-expiration-session-error)
- [Licensing error - installCheck failed](#licensing-error---installcheck-failed)
- [Create branch or pull request features missing](#create-branch-or-pull-request-features-missing)
- [Connection error for self-hosted git servers](#connection-error-for-self-hosted-git-servers)
- [Repositories missing from Azure DevOps integration](#repositories-missing-from-azure-devops-integration)
- [SSH key file format is invalid](#ssh-key-file-format-is-invalid)
- [Error while reindexing - Java heap space](#error-while-reindexing---java-heap-space)
- [OAuth connection error with Azure DevOps](#oauth-connection-error-with-azure-devops)
- [OAuth error with Azure DevOps Active Directory](#oauth-error-with-azure-devops-active-directory)
- [Empty repository list after Azure Repos integration](#empty-repository-list-after-azure-repos-integration)
- [Reconnecting Azure DevOps OAuth integrations](#reconnecting-azure-devops-oauth-integrations)

&nbsp;
* * *
&nbsp;

## Why Don't I See Commits?

![](/wp-content/uploads/gij-troubleshoot-how-do-i-see-commits-top.png)

Follow these steps to diagnose missing commits:

### Step 1: Verify app installation and license

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

1. Install from [Atlassian Marketplace](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview).
2. Go to ![](/wp-content/uploads/actions-icon.png) Jira Settings ➜ Apps ➜ **Manage apps**.
3. Verify the license is valid and the application is active.

<img src='/wp-content/uploads/gij-gitcloud-manage-apps-1455.png' style='max-width:100%;margin:25px auto;display:block' />

### Step 2: Check user permissions

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

Use the Permission Helper to verify the user has **Development Tools** permission.

Go to ![](/wp-content/uploads/actions-icon.png) Jira settings ➜ System ➜ **Permission Helper**.

### Step 3: Verify repository connection

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

Check if the repository with the commit is connected:

**Via Manage Repositories page:**

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-via-repo-1455.png)

**Via Repository Browser:**

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-reindex-since-commit-1455.png)

### Step 4: Check reindex status

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

Repositories update automatically every 8-15 minutes. To reindex manually:

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-reindex-manually-01.png)

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-reindex-manually-02.png)

Set up webhooks for immediate indexing:

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-webhooks.png)

### Step 5: Check project association

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

1. Go to Manage integrations page.
2. Click ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit integration**.
3. Scroll to **Project Permissions**.
4. Set project associations or check **Associate all projects**.

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-associate-projects.png)

### Step 6: Verify commit message format

Include the Jira issue key in commit messages:

**Valid examples:**
- `ABC-123 added a bug fix`
- `MAIN-345 adding important new feature`

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-valid-key.png)

GitLab commit example:

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-gitlab.png)

### Step 7: Find indexed commits in Repository Browser

The commit may be indexed but not associated with any Jira issue:

1. Navigate to **Repository browser**.
2. Find the repository and commit (select the branch if needed).
3. Click **Change** to fix commit association.

![](/wp-content/uploads/gij-gitcloud-finding-indexed-commits-in-jira-cloud.gif)

### Step 8: Verify commits display

View commits in the Jira issue:

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-new-jira.png)

**Still not seeing commits?** Contact [gijsupport@gitkraken.com](mailto:gijsupport@gitkraken.com) or use the [GIJ Cloud Support Portal](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

&nbsp;
* * *
&nbsp;

## License Expiration Session Error

### Problem

You receive a `SessionTokenNotFoundException` error and cannot use GIJ features.

### Diagnosis

![](/wp-content/uploads/gij-dc-cloud-session-token-not-found-error.png)

### Solution

This error indicates the trial or license has expired. Renew your Git Integration for Jira app license to resolve the error.

If the license was expired for an extended period, you may see "There is no Enabled installID" after renewing. Contact [support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/) for manual enablement.

&nbsp;
* * *
&nbsp;

## Licensing Error - installCheck Failed

### Problem

Licensing fails to fully provision during installation.

### Diagnosis

![](/wp-content/uploads/gij-licensing-installcheck-failed-error.png)

### Solution

Reinstall the app:

1. Navigate to **Manage Apps**.
2. Expand **Git Integration for Jira Cloud**.
3. Click **Unsubscribe** (required before uninstalling).
4. Click **Uninstall**.
5. Reinstall **Git Integration for Jira** from Marketplace.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Stopping trial</b><br>
        Stop the evaluation/trial before uninstalling the app.<br>
        <img src='/wp-content/uploads/gij-gitcloud-manage-apps-git-cloud-admin.png' style='margin:25px auto;max-width:100%;display:block;' />
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

## Create Branch or Pull Request Features Missing

See [Why don't I see commits?](#why-dont-i-see-commits) for troubleshooting steps related to repository connections and permissions.

&nbsp;
* * *
&nbsp;

## Connection Error for Self-Hosted Git Servers

### Problem

Cannot connect Jira Cloud to self-hosted git servers behind a firewall.

### Solution

Add the Git Integration for Jira Cloud indexing service to your allowlist. See [Whitelist GIJ Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud).

&nbsp;
* * *
&nbsp;

## Repositories Missing from Azure DevOps Integration

### Problem

Some or all repositories in Azure DevOps integrations are not visible.

### Causes and Solutions

**1. Permissions**

The connecting Azure DevOps user must have repository access. Grant appropriate access to required repositories.

**2. Access Level**

`Basic` or `Visual Studio Professional` access is required for Code access.

![](/wp-content/uploads/gij-azure-devops-code-access-level.png)

See [Azure DevOps Access Levels](https://docs.microsoft.com/en-us/azure/devops/organizations/security/access-levels?view=azure-devops).

**3. Repository Format**

Only git repositories are supported. Team Foundation Version Control (TFVC) repositories are not supported.

Convert TFVC to git:
- [Migrate from TFVC to Git](https://docs.microsoft.com/en-us/devops/develop/git/migrate-from-tfvc-to-git)
- [Import repositories from TFVC to Git](https://docs.microsoft.com/en-us/azure/devops/repos/git/import-from-tfvc?view=azure-devops)

&nbsp;
* * *
&nbsp;

## SSH Key File Format Is Invalid

### Problem

SSH key is rejected with "The key format is invalid" message.

<img src='/wp-content/uploads/gij-private-key.png' width=494 height=454 style='max-width:100%;display:block;margin:25px auto;' />

### Requirements

SSH keys must:
- Not use OpenSSH format
- Be the private key (not public)
- Use RSA certificate format
- Use OpenSSL PEM storage format

### Solution: Create a New SSH Key

**On Linux and macOS:**

```bash
ssh-keygen -t rsa -b 4096 -m pem -C your_email@example.com
```

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        macOS sometimes creates OpenSSH format certificates incorrectly. See <a href='https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key'>this solution</a>.
    </div>
    </div>
</div>

**On Windows (using PuTTY):**

1. Download [PuTTY](https://www.putty.org/).
2. Open PuTTYgen.
3. Set **Type of key** to **RSA**.
4. Set **Number of bits** to **4096**.
5. Click **Generate** and move the mouse pointer randomly.
6. Optionally enter a **Passphrase**.
7. Save the public and private keys.
8. Convert to PEM: **Conversions** ➜ **Export OpenSSH key**.
9. Upload the private key to Git Integration for Jira app.

&nbsp;
* * *
&nbsp;

## Error While Reindexing - Java Heap Space

### Problem

JGit library does not support objects over 2GB in git repositories.

### Solutions

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Changing git repository history can result in data loss. Proceed with care.
    </div>
    </div>
</div>

**Option 1: Remove large objects**
- [Removing large files from Git without losing history](https://support.acquia.com/hc/en-us/articles/360004334093-Removing-large-files-from-Git-without-losing-history)
- [GitHub: Removing files from repository history](https://help.github.com/en/articles/removing-files-from-a-repositorys-history)
- [GitLab: Reducing repository size using Git](https://docs.gitlab.com/ee/user/project/repository/reducing_the_repo_size_using_git.html)
- [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)

**Option 2: Use Git LFS**

Move large files to [Git LFS](https://git-lfs.github.com/), which Git Integration for Jira supports.

**Option 3: Filter the repository**

Use [Custom API Path](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud) or [JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud) to exclude the repository.

&nbsp;
* * *
&nbsp;

## OAuth Connection Error with Azure DevOps

### Problem

OAuth connection error or 401 error when integrating Azure DevOps.

### Solution

Enable third-party OAuth access:

1. Go to your Azure DevOps portal home page.
2. Click an organization ➜ **Organization Settings**.
3. Under **Security**, click **Policies**.
4. Set **Third-party application access via OAuth** to **ON**.

![](/wp-content/uploads/gij-vsts-azure-devops-org-cfg-policy-oauth.png)

&nbsp;
* * *
&nbsp;

## OAuth Error with Azure DevOps Active Directory

### Problem

OAuth connection error with Azure DevOps connected to Active Directory.

### Solution

1. Enable third-party OAuth access (see above).
2. Disable conditional access policy validation:

![](/wp-content/uploads/gij-enable-conditional-access-policy-AD.png)

&nbsp;
* * *
&nbsp;

## Empty Repository List After Azure Repos Integration

### Problem

Integration shows INDEXED status but the repository list is empty.

![](/wp-content/uploads/gij-gitcloud-azure-no-repo-manage-repos.png)

### Solution

1. Switch from OAuth to personal access token authentication.
2. Verify PAT configuration. See [Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud).
3. Follow the OAuth troubleshooting steps in previous sections.

&nbsp;
* * *
&nbsp;

## Reconnecting Azure DevOps OAuth Integrations

<b style='background-color:#FFEED1; padding:1px 5px; color:#CC5900; border-radius:3px; margin: 0 5px; font-size: small;'>WORKAROUND</b>

Microsoft OAuth app client secrets expire after 5 years. All customers must reconnect their integrations.

### Requirements

- Jira administrator permissions
- Azure DevOps / VSTS account

### Steps

1. Go to **Manage integrations** in Git Integration for Jira.
2. Click on the integration name.
3. Click **Reconnect**.
4. Log in to Azure DevOps / VSTS with the account to associate.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        Reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

<kbd>Last updated: December 2025</kbd>
