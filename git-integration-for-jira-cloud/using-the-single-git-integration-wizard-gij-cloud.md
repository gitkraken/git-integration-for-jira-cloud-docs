---

title: Using the Single git integration wizard
description: How to connect single git repositories using the integration wizard
taxonomy:
    category: git-integration-for-jira-cloud

---

Connect specific single git repositories using Git Integration for Jira.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Copy the git clone URL from your repository home portal before proceeding.
    </div>
    </div>
</div>

&nbsp;

### Step 1

On the Manage integrations page, click **Add integration**.

![](/wp-content/uploads/gij-gitcloud-managed-ui-integrations-page-2025.png)

&nbsp;

### Step 2

On the Git hosting service selection screen, use the **Quick start** section by pasting the git clone URL in the provided box (HTTPS or SSH), then click **Connect** to proceed.

You can also click **Plain Git Repository** to connect single git repositories.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-single-repo-sel-https-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

&nbsp;

### Step 3

Set up the integration depending on the type of git clone URL you are using. Enter the git clone URL into the **Host URL** field. The login form automatically adjusts to the type of URL provided.

&nbsp;

#### 3a. HTTPS Authentication

![](/wp-content/uploads/gij-gitcloud-managed-ui-single-repo-add-new-http-2025.png)

Provide login credentials as required, then click **Add integration** to complete this setup.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If two-factor authentication is enabled in your git host service account, enter the personal access token as the password.
    </div>
    </div>
</div>

&nbsp;

### 3b. SSH Authentication

![](/wp-content/uploads/gij-gitcloud-quick-start-plain-git-integration-ssh-2025.png)

Provide SSH credentials as required, then click **Add integration** to complete this setup.

If the [generated SSH key pair](/git-integration-for-jira-cloud/working-with-ssh-keys-gij-cloud) has a passphrase, enter the **Passphrase** for your private key.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The SSH server is the Git server (git service such as GitHub, GitLab, etc.), and the SSH client is the Jira server (in this case, the Jira Cloud instance).
    </div>
    </div>
</div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>SSH</b><br>
        When setting up repositories with Git Integration for Jira, you need the necessary access permissions on the private key in the Git server to proceed.
    </div>
    </div>
</div>

&nbsp;

### Setup Complete

After completing the setup, the wizard indexes the git repository to build change history. This completes the setup, and the newly added repository appears in the integration list on the Manage integrations page.

&nbsp;
* * *

[**Prev:** Using the Git service integration wizard](/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud)

[**Next:** Self-signed HTTPS integration](/git-integration-for-jira-cloud/self-signed-https-integration-gij-cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
