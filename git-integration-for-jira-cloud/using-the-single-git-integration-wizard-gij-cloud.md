---

title: Using the Single git integration wizard
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Connect specific single git repositories to Jira by performing the following steps:

## Getting started

**Step 1** – Click on the **Single git repository integration** panel.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024154/gitcloud-managed-ui-single-repo-sel.png?version=1&modificationDate=1647944395874&cacheVersion=1&api=v2)

## HTTP(S) Authentication

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024154/github-https-git-clone-url-loc.png?version=1&modificationDate=1650104187735&cacheVersion=1&api=v2)

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Obtain the HTTPS git clone URL from the repository’s project page of your git account. Use this for <b><i>Step 2a</i></b>.
    </div>
    </div>
</div>
<br>

**Step 2a** – Enter the HTTPS repository git clone URL into the **Host URL** field. The login form automatically appears if the provided URL requires HTTP credentials. Provide login credentials as required.

_If two-factor authentication is enabled in your git host service account, enter the personal access token as the password_.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024154/gitcloud-managed-ui-single-repo-add-new.png?version=1&modificationDate=1647944814969&cacheVersion=1&api=v2)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The HTTP authorization errors indicate that the credentials provided are not valid.
    </div>
    </div>
</div>
<br>

## SSH authentication

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024154/github-ssh-git-clone-url-loc.png?version=1&modificationDate=1650104394405&cacheVersion=1&api=v2)

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Obtain the SSH git clone URL from the repository’s project page of your git account. Use this for <b><i>Step 2b</i></b>.
    </div>
    </div>
</div>

**Step 2b** – Enter the SSH repository git clone URL into the **Host URL** field. The input form for SSH private key is automatically displayed if the provided URL requires SSH credentials.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024154/gitcloud-managed-ui-single-repo-add-new-ssh.png?version=1&modificationDate=1647945930110&cacheVersion=1&api=v2)

Upload the private key file by clicking **Upload Key File** and navigate to the private key file. Otherwise, paste the private key text into the provided box.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Take note that the SSH server is the Git server (git service such as GitHub, GitLab etc.); and the SSH client is the Jira server (in this case, the Jira Cloud instance).
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
        When setting up repositories with the Git Integration app, you need to have the necessary access permissions on the private key in the Git server to proceed.
    </div>
    </div>
</div>

For establishing safety connection with SSH, upload a public Key to the SSH server and set the private Key to the SSH client.

If the [generated SSH key pair](/git-integration-for-jira-cloud/working-with-ssh-keys-gij-cloud) has a passphrase, enter the _**Passphrase**_ for your private key.


**Step 3** – Click **Add integration** to complete this setup.

Finally, after completing the setup, the wizard will index the git repository to build change history. This completes the setup and the newly added repository appears on the integration list in the Manage integrations page.

## See next topics

[Using the Git service integration wizard](/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud)

[Self-signed HTTPS integration](/git-integration-for-jira-cloud/self-signed-https-integration-gij-cloud)

