---

title: Working with SSH keys
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

SSH keys are required in order to provide secure connection with the remote git host. The Git Integration for Jira app uses one set of keys for accessing all configured repositories.

Follow this guide if you are one of the users who are limited to or wanted to use SSH to securely connect to your git repositories.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Features such as branch and pull/merge request creation are only available to repositories/git hosts that were connected via the Full feature integration (<i>formerly Auto-connect integration</i>).
    </div>
    </div>
</div>

&nbsp;

**On this page:**
- [Getting started](#getting-started)
- [Generating SSH keys on Windows](#generating-ssh-keys-on-windows)
- [Generating SSH keys on Linux/MacOS](#generating-ssh-keys-on-linuxmacos)
- [Git host specific SSH key instructions](#git-host-specific-ssh-key-instructions)
- [Connecting SSH Git Repositories](#connecting-ssh-git-repositories)
- [Adding a public SSH key to your Git server](#adding-a-public-ssh-key-to-your-git-server)
- [Updating a private SSH key](#updating-a-private-ssh-key)

&nbsp;

* * *

&nbsp;

## Getting started

Before connecting repositories via SSH, users are required to generate SSH keys for use with the remote git host (_public key_) and for Git Integration app in Jira (_private key_).

Generated SSH keys always come in pair. (**Example:** `id_rsa.pub` and `id_rsa`)

For establishing safety connection with SSH, upload a **public key** to the SSH server and set the **private key** to the SSH client.

In this case, the SSH server is the Git server and the SSH client is the Jira server. Therefore:

*   Git server — public key
*   Jira server — private key

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Note that Git Integration for Jira app SSH key:
        <ul>
            <li>must not be created using the OpenSSH format.</li>
            <li>must be the private key.</li>
            <li>must use the supported certificate format: RSA.</li>
            <li>must use the supported storage format: OpenSSL PEM.</li>
        </ul>
        <hr>
        <p style='margin-bottom:0px !important'>For more information, see known issue <a href='/git-integration-for-jira-cloud/ssh-key-file-format-is-invalid-gij-cloud'>SSH key format is invalid</a>.</p>
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Generating SSH keys on Windows

For Windows, we recommend to use [**PuTTY**](https://www.putty.org/) and use PuTTYgen to generate public and private SSH keys.

<img src='/wp-content/uploads/gij-workting-with-puttygen-key-dlg.png' style='margin:25px auto;display:block;max-width:100%' width=479px height=471px />

1.  Launch **PuTTYgen** and refer to the above image for the rest of the steps on this section.

2.  Set _**Type of key to generate**_ to **RSA**.

3.  Set _**Number of bits in a generated key**_ to **4096**.

4.  Click **Generate**.

5.  Follow screen instructions such as moving your mouse pointer on random locations on the blank area of the PuTTYgen dialog. Do this until the progress bar completely fills up and the SSH key pair is generated.

6.  Entering a **Passphrase** for the generated key is optional but will ensure a more secure connection.

7.  Save your generated public and private key to a file by clicking the respective options.

8.  Copy the generated key. This is the public key that you will be using on the SSH configuration page of your git host.

9.  For the private key, see the notes below.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        PuTTY creates a private key in its own ".ppk" format. To convert it to ".pem", the user should do the <b>Conversions</b> ➜ <b>Export OpenSSH key</b> menu option in PuTTYgen. Add/upload this file to Git Integration for Jira app ➜ <b>SSH keys</b> or when prompted on connecting SSH git repositories in Jira via Connect wizard.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        You can also use the git bash command line to generate SSH key pair. For detailed information, see <a href='https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key'><b>Generate SSH via Git bash</b></a>.
    </div>
    </div>
</div>

&nbsp;

## Generating SSH keys on Linux/MacOS

On Linux and MacOS, this generates an SSH key in RSA format:

```
ssh-keygen -t rsa -b 4096 -m pem -C "your_email@example.com"
```

MacOS often incorrectly creates an OpenSSH format certificate. For more details, see information on this [**common problem**](https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key).

&nbsp;

* * *

&nbsp;

## Git host specific SSH key instructions

Configure and generate SSH keys for the following git hosting systems by following the reference links on each sub-section:

### Beanstalk

*   For MacOS, see [Working with Git on MacOS](http://guides.beanstalkapp.com/version-control/git-on-mac.html).
*   For Windows, see [Working with Git on Windows](http://guides.beanstalkapp.com/version-control/git-on-windows.html).
*   For Linux, see [Working with Git on Linux](http://guides.beanstalkapp.com/version-control/git-on-linux.html).

### Bitbucket

*   For MacOS/Linux, see [Setting up SSH for Git on MacOS/Linux](https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/#Set-up-SSH-on-macOS-Linux).
*   For Windows, see [Set up SSH for Git on Windows](https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/).

### GitHub

[Check for existing SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys) before you proceed to generate new keys.

See GitHub supported platforms for generating SSH keys by following [this article](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

### GitLab

*   See reference, [Installing Git for MacOS/Windows/Linux](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
*   For creating SSH keys, see [Generating SSH Public Key](https://docs.gitlab.com/ee/user/ssh.html). Also see the video demonstration [here](https://about.gitlab.com/blog/2014/03/04/add-ssh-key-screencast/).

### GitLab CE/EE

Follow the above GitLab references for GitLab CE/EE. Then verify that your GitLab server should have the following SSH settings:

<img src='/wp-content/uploads/gij-gitlab-server-ssh-settings.png' style='margin:25px auto;display:block;' />

*   Enabled Git access protocols -- **Both SSH and HTTP(s)**
*   RSA SSH keys -- **Are allowed**

Other SSH key formats may be supported by Git Integration for Jira app, but prefer to use RSA format for your SSH git connections.

### VSTS, TFS, Azure DevOps and Azure Repos

The SSH support starts with TFS 2013 and later versions.

*   For information about TFS/Azure DevOps Server, see [MS Team Foundation Server](https://azure.microsoft.com/en-us/services/devops/server/).
*   For general reference and terms, see [Git Experience Futures](https://devblogs.microsoft.com/devops/git-experience-futures/).

### Gerrit

The Git Integration for Jira app supports Gerrit web linking.

*   For information about Gerrit software, see [Gerrit Software Wiki](http://en.wikipedia.org/wiki/Gerrit_(software)) and [Gerrit at Code Review](https://code.google.com/p/gerrit/).
*   For general reference and installation, see [Gerrit documentation](https://gerrit-review.googlesource.com/Documentation/). [Ubuntu installation](https://gerrit-review.googlesource.com/Documentation/linux-quickstart.html) and fixing [registration error](https://issues.gerritcodereview.com/issues/40001679).
*   For information on SSH on Gerrit, see [SSH and Gerrit](https://gerrit-documentation.storage.googleapis.com/Documentation/2.11/user-upload.html#_ssh).
*   For details on User Change-IDs, see [Change-IDs in Gerrit](https://git.eclipse.org/r/Documentation/user-changeid.html).

### GitBlit

*   For information about Gitblit, see [GitBlit official website](https://www.gitblit.com/).
*   For general reference and installation, see [GitBlit Configuration](http://gitblit.com/administration.html), [Using HTTP/HTTPS Transport](http://gitblit.com/setup_transport_http.html) and [Built-in Authentication](http://gitblit.com/setup_authentication.html).
*   For information on SSH on GitBlit, see [GitBlit: Using the SSH Transport](http://gitblit.com/setup_transport_ssh.html).
*   For GitBlit related FAQ, see [GitBlit Frequently Asked Questions](http://gitblit.com/faq.html).

### Gitolite

*   For full reference and installation, see [All About Gitolite](https://gitolite.com/gitolite/index.html).
*   For information on SSH on Gitolite, see [SSH and Gitolite](https://gitolite.com/gitolite/ssh.html).
*   For details on user key management, see [Managing User Keys in Gitolite](https://gitolite.com/gitolite/contrib/ukm.html).

### Git-scm

*   See reference, [Installing Git for MacOS/Windows/Linux](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).
*   For creating SSH keys, see [Connecting to GitHub with SSH](https://help.github.com/en/articles/connecting-to-github-with-ssh).

&nbsp;

* * *

&nbsp;

## Connecting SSH Git Repositories

SSH git repositories can be integrated with Jira Cloud via Git Integration for Jira app.

We recommend to generate a **4096-bit** key using the instructions above.

To connect an SSH repository:

1.  On your Jira dashboard menu, go to **Apps** ➜ **Git Integration: Manage integrations.**

2.  On the Manage integrations page, click **Add integration.**

3.  On the following screen, at the Quick start integration section:
    *   Click on the **SSH** tab.
    *   Enter the git clone URL on the provided box.

4.  Click **Connect** to complete this process.
    *   If prompted, enter login credentials for this repository integration. If 2FA is enabled for this account, enter the personal access token (PAT) for the password instead.
    *   Enable/disable [SSL Verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud) for this repository integration.

The repository is now connected for use with Jira.

&nbsp;

* * *

&nbsp;

## Adding a public SSH key to your Git server

Add a public SSH key to your remote git host to prepare its repositories for connection with the Git Integration for Jira app.

Do the following steps to setup SSH for your remote git host:

1.  Login to your remote git host service.

2.  Go to the SSH configuration page, if supported.

    See examples: [Adding SSH key in GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) or [Adding SSH key in GitLab](https://docs.gitlab.com/ee/user/ssh.html#add-an-ssh-key-to-your-gitlab-account).

3.  Paste the public key to the provided box (GitLab) or upload the public key file and complete the setup (GitHub).

4.  Verify your SSH connection to the git host server.

&nbsp;

* * *

&nbsp;

## Updating a private SSH key

If a new SSH key pair is generated for the configured repository, do the following steps:

1.  On the Manage integrations page list, click on ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit integration** for the SSH-connected git repository.

    ![](/wp-content/uploads/gij-gitmgr-actions-edit-integration-ssh-repo.png)

2.  Change the Private SSH key field (highlighted below) by pasting with the updated value or uploading the Private SSH key file.

    ![](/wp-content/uploads/gij-gitmgr-actions-edit-integration-ssh-credentials-sel.png)

    If a passphrase is present, enter it on the provided box.

3.  Click **Save** to save the settings.

