---
title: Troubleshooting articles
description: Solutions and workarounds for common issues with Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This collection of troubleshooting guides provides workarounds and solutions for common issues with Git Integration for Jira Cloud.

**On this page:**
- [Why don't I see commits?](#why-dont-i-see-commits-git-integration-for-cloud)
- [License expiration shows as session error](#when-a-gij-license-expires-it-shows-up-as-a-session-error)
- [Licensing error - installCheck failed](#licensing-error---installcheck-failed)
- [Missing Create branch or pull request features](#why-dont-i-see-the-create-branch-or-pull-request-features)
- [Connection error for self-hosted git servers](#connection-error-for-self-hosted-git-servers)
- [Repositories missing from Azure DevOps integration](#repositories-missing-from-azure-devops-or-vsts-integration)
- [SSH key file format is invalid](#ssh-key-file-format-is-invalid)
- [Error while reindexing - Java heap space](#error-while-reindexing---java-heap-space--object-too-large)
- [OAuth connection error with Azure DevOps](#oauth-connection-error-or-error-401-page-with-azure-devops-integration)
- [OAuth connection error with Azure DevOps Active Directory](#oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration)
- [Empty list of repositories after Azure Repos integration](#empty-list-of-repositories-after-integration-of-azure-repos)
- [Reconnecting Azure DevOps OAuth integrations](#reconnecting-azure-devops-and-vsts-oauth-integrations)

&nbsp;
* * *
&nbsp;

## Why don't I see commits? (Git Integration for Cloud)

![](/wp-content/uploads/gij-troubleshoot-how-do-i-see-commits-top.png)

Follow this troubleshooting checklist to resolve missing commits.

### Step 1: Verify app installation and license

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

1. Install from [Atlassian Marketplace](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview).
2. Go to ![](/wp-content/uploads/actions-icon.png) **Jira Settings** ➜ **Apps** ➜ **Manage apps**.
3. Verify the license is valid and the application is active.

<img src='/wp-content/uploads/gij-gitcloud-manage-apps-1455.png' style='max-width:100%;margin:25px auto;display:block' />

### Step 2: Check user permissions

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

Use the **Permission Helper** to verify the user has **Development Tools** permission:

Go to ![](/wp-content/uploads/actions-icon.png) **Jira settings** ➜ **System** ➜ **Permission Helper**.

### Step 3: Verify repository connection

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

Check repository connection using either method:

**Via Manage Repositories:**

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-via-repo-1455.png)

**Via Repository Browser:**

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-reindex-since-commit-1455.png)

### Step 4: Check reindex status

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

Repositories update automatically every 8-15 minutes. To reindex manually:

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-reindex-manually-01.png)

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-reindex-manually-02.png)

**For faster indexing:** Configure webhooks to index commits immediately.

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-webhooks.png)

### Step 5: Check project association

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

1. Go to **Manage integrations**.
2. Click ![](/wp-content/uploads/actions-icon.png) **Actions** ➜ **Edit integration**.
3. Scroll to **Project Permissions**.
4. Set project associations or check **Associate all projects**.

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-associate-projects.png)

### Step 6: Verify commit message contains issue key

Include the Jira issue key in your commit message:

**Valid examples:**
- `ABC-123 added a bug fix`
- `MAIN-345 adding important new feature`

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-valid-key.png)

**GitLab commit example:**

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-gitlab.png)

### Step 7: Find indexed commits in Repository browser

The commit may be indexed but not associated with any Jira issues:

1. Navigate to **Repository browser**.
2. Find the repository and commit (select the branch if needed).
3. Click **Change** to fix commit association.

![](/wp-content/uploads/gij-gitcloud-finding-indexed-commits-in-jira-cloud.gif)

### Step 8: Verify commits display

Commits appear in the Jira issue view:

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-new-jira.png)

**Still not seeing commits?** Contact [gijsupport@gitkraken.com](mailto:gijsupport@gitkraken.com) or use the [GIJ Cloud Support Portal](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

## When a GIJ license expires, it shows up as a session error

### Problem

You receive a `SessionTokenNotFoundException` error and cannot use GIJ features.

### Diagnosis

The session error persists after page reload:

![](/wp-content/uploads/gij-dc-cloud-session-token-not-found-error.png)

### Solution

This error indicates an expired trial or license. Renew your Git Integration for Jira app license to resolve the error.

If the license expired for an extended period, you may see "There is no Enabled installID" after renewal. Submit a [support request](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/) for manual enablement.


## Licensing error - installCheck failed

### Problem

The Git Integration for Jira Cloud app licensing fails to fully provision during installation.

### Diagnosis

You see a message similar to:

![](/wp-content/uploads/gij-licensing-installcheck-failed-error.png)

### Solution

Reinstall the app:

1. Navigate to **Manage Apps**.
2. Locate and expand **Git Integration for Jira Cloud**.
3. Click **Unsubscribe** (required before uninstalling).
4. Click **Uninstall**.
5. Install **Git Integration for Jira** again.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Stop the evaluation/trial before uninstalling the app.<br>
        <img src='/wp-content/uploads/gij-gitcloud-manage-apps-git-cloud-admin.png' style='margin:25px auto;max-width:100%;display:block;' />
    </div>
    </div>
</div>

## Why don't I see the Create branch or pull request features?

Check that your integration supports these features and that you have the required permissions. See the [Feature matrix](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud) for supported features by git service.

## Connection error for self-hosted git servers

### Problem

Cannot connect Jira Cloud to self-hosted git servers behind a firewall.

### Diagnosis

You see an error similar to:

```
TrackedGitLabRepoException: Can not connect to GitLab server
```

### Solution

Add the Git Integration for Jira Cloud indexing service to your allowlist. See [Whitelist GIJ Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud).

## Repositories missing from Azure DevOps (or VSTS) integration

### Problem

Some or all repositories in Azure DevOps integrations are not visible.

### Diagnosis

Check these three areas:

| Issue | Requirement |
|-------|-------------|
| Permissions | Connecting user must have repository access |
| Access Level | Minimum `Basic` or `Visual Studio Professional` (Code access required) |
| Repository format | Only git format repositories supported (not TFVC) |

![](/wp-content/uploads/gij-azure-devops-code-access-level.png)

See [Azure DevOps Access Levels](https://docs.microsoft.com/en-us/azure/devops/organizations/security/access-levels?view=azure-devops).

### Solutions

1. **Permissions:** Assign appropriate repository access.
2. **Access level:** Grant at least `Basic` access.
3. **Repository format:** Convert TFVC to git format:
   - [Migrate from TFVC to Git](https://docs.microsoft.com/en-us/devops/develop/git/migrate-from-tfvc-to-git)
   - [Import repositories from TFVC to Git](https://docs.microsoft.com/en-us/azure/devops/repos/git/import-from-tfvc?view=azure-devops)


## SSH key file format is invalid

### Problem

SSH key is rejected when connecting a repository.

### Requirements

SSH keys for Git Integration for Jira must:
- Not use OpenSSH format
- Be the private key (not public)
- Use RSA certificate format
- Use OpenSSL PEM storage format

### Diagnosis

You see: "The key format is invalid. Please check your private key."

<img src='/wp-content/uploads/gij-private-key.png' width=494 height=454 style='max-width:100%;display:block;margin:25px auto;' />

### Solution

**Create a new SSH key:**

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
      macOS may incorrectly create OpenSSH format certificates. See this <a href='https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key' target='_blank'><b>common problem</b></a>.
    </div>
  </div>
</div>

**On Windows (using PuTTY):**

1. Download [PuTTY](https://www.putty.org/).
2. Open PuTTYgen.
3. Set **Type of key** to **RSA**.
4. Set **Number of bits** to **4096**.
5. Click **Generate** and move your mouse as instructed.
6. Optionally enter a passphrase.
7. Save public and private keys.
8. Convert to PEM: **Conversions** ➜ **Export OpenSSH key**.
9. Upload the PEM file to Git Integration for Jira ➜ **SSH Keys**.


## Error while reindexing - Java heap space / Object too large

### Problem

Git Integration for Jira uses the JGit library, which does not support objects over 2GB.

### Diagnosis

Error in Jira logs:

```
Object too large (2,271,263,009 bytes), rejecting the pack. 
Max object size limit is 2,147,483,639 bytes.
```

### Solutions

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Changing git repository history can result in data loss. Proceed with caution.
    </div>
    </div>
</div>

**Option 1:** Remove objects larger than 2GB from repository history:
- [Removing large files from Git without losing history](https://support.acquia.com/hc/en-us/articles/360004334093-Removing-large-files-from-Git-without-losing-history)
- [GitHub: Removing files from repository history](https://help.github.com/en/articles/removing-files-from-a-repositorys-history)
- [GitLab: Reducing repository size using Git](https://docs.gitlab.com/ee/user/project/repository/reducing_the_repo_size_using_git.html)
- [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)

**Option 2:** Move large files to [Git LFS](https://git-lfs.github.com/).

**Option 3:** Filter out the repository using [Custom API Path](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud) or [JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

## OAuth connection error or error 401 page with Azure DevOps integration

### Problem

OAuth connection error or 401 page when integrating Azure DevOps.

### Cause

Third-party OAuth access is disabled in Azure DevOps security settings.

### Solution

1. Go to your Azure DevOps portal home page.
2. Click an organization ➜ **Organization Settings**.
3. Under **Security**, click **Policies**.
4. Set **Third-party application access via OAuth** to **ON**.

![](/wp-content/uploads/gij-vsts-azure-devops-org-cfg-policy-oauth.png)

## OAuth connection error or error 401 page with Azure DevOps with Active Directory integration

### Problem

OAuth connection error or 401 page with Azure DevOps connected to Active Directory.

### Cause

Conditional access policy requires MFA for untrusted locations.

### Solution

1. Enable **Third-party application access via OAuth** (see above).
2. Set conditional access policy validation to **OFF**:

![](/wp-content/uploads/gij-enable-conditional-access-policy-AD.png)

## Empty list of repositories after integration of Azure Repos

### Problem

Azure repository list is empty after integration, but status shows INDEXED.

![](/wp-content/uploads/gij-gitcloud-azure-no-repo-manage-repos.png)

### Solution

1. Switch from OAuth to personal access token authentication.
2. Verify PAT configuration per [Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud).

If the problem persists, see the Azure DevOps OAuth troubleshooting sections above.

## Reconnecting Azure DevOps and VSTS OAuth integrations

<b style='background-color:#FFEED1; padding:1px 5px; color:#CC5900; border-radius:3px; margin: 0 5px; font-size: small;'>WORKAROUND</b>

Microsoft OAuth app client secrets expire after 5 years. All customers must reconnect their integrations.

### Requirements

- Jira administrator permissions
- Azure DevOps / VSTS account

### Steps

1. Go to **Manage integrations** in Git Integration for Jira.
2. Click the integration name.
3. Click **Reconnect**.
4. Log in to Azure DevOps / VSTS with your account.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        Reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

<kbd>Last updated: December 2025</kbd>
