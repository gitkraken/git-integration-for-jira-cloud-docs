---

title: Connecting SSH Git Repositories to Jira Cloud
description: Learn how to connect SSH git repositories to Jira Cloud, including SSH key generation and configuration.
taxonomy:
    category: git-integration-for-jira-cloud

---

**What’s on this page:**
- [Introduction](#introduction)
- [Generating SSH Keys](#generating-ssh-keys)
  - [Windows](#windows)
  - [Linux/MacOS](#linuxmacos)
- [Power Users](#power-users)
- [Connecting SSH Git Repositories](#connecting-ssh-git-repositories)

&nbsp;
* * *
&nbsp;

### Introduction

SSH git repositories can be integrated with Jira Cloud using [**Git Integration for Jira**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview).

&nbsp;

### Generating SSH Keys

Generate an SSH key pair before proceeding. We recommend a **4096-bit key**.

&nbsp;

#### Windows

For Windows users, we recommend to use [**PuTTY**](https://www.putty.org/) and use PuTTYgen to generate public and private SSH keys.

<img src='/wp-content/uploads/gij-workting-with-puttygen-key-dlg.png' style='margin: 25px auto;max-width:100%;' />

1.  Launch **PuTTYgen** and refer to the above image for the rest of the steps on this section.

2.  Set _**Type of key to generate**_ to **RSA**.

3.  Set _**Number of bits in a generated key**_ to **4096**.

4.  Click **Generate**.

5.  Follow screen instructions such as moving your mouse pointer on random locations on the blank area of the PuTTYgen dialog. Do this until the progress bar completely fills up and the SSH key pair is generated.

6.  Entering a **Passphrase** for the generated key is optional but will ensure a more secure connection.

7.  Save your generated public and private key to a file by clicking the respective options.

8.  Copy the generated key. This is the public key that you will be using on the SSH configuration page of your git host.

9.  For the private key, see the note below.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        PuTTY creates a private key in its own ".ppk" format. To convert it to ".pem":<br>
        <ul style='margin-bottom:0px !important'>
            <li>The user should do the <b>Conversions</b> ➜ <b>Export OpenSSH key</b> menu option in PuTTYgen.</li>
            <li>Add/upload this file to Git Integration for Jira app ➜ <b>SSH keys</b> or when prompted on connecting SSH git repositories in Jira.</li>
        </ul>
    </div>
    </div>
</div>

You can also use the git bash command line to generate SSH key pair. For detailed information, see [**Generate SSH via Git bash**](https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key).<br><br>Read on the section in our online documentation, [**Generating SSH Keys**](/git-integration-for-jira-cloud/working-with-ssh-keys-gij-cloud), and follow specific information for the git host and platform that you use.

&nbsp;

#### Linux/MacOS

On Linux and MacOS, this generates an SSH key in RSA format:

```bash
ssh-keygen -t rsa -b 4096 -m pem -C "your_email@example.com"
```

MacOs often incorrectly creates an OpenSSH format certificate. For more details, see information on this [common problem](https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key). |

&nbsp;

### Power Users

Git Integration for Jira supports RSA format for private SSH keys. To convert your SSH key pair to the supported format, use this syntax:

```bash
ssh-keygen -p -P "old_password" -N "new_password" -m pem
```

&nbsp;

### Connecting SSH Git Repositories

1.  Generate an SSH key pair as stated in the previous section.

2.  Obtain the Clone SSH git URL from your git host repository page.

3.  On your Jira Cloud dashboard, go to menu Apps ➜ **Git Integration: Manage integrations**.

4.  On the top-right corner click on **Add integration**.

5.  Under Self-hosted group, click on **Plain git repository**.

6.  Paste the SSH git clone URL into the **Host URL** field.

7.  Paste the Private SSH key on the provided box or click **Upload Key File** to upload a private SSH key file.

8.  Enter the **Passphrase** of the private SSH key, if any. Otherwise, leave it blank.

9.  Click on **Add Integration** to complete this process.


The connected repository is listed in the git configuration page.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For Jira Cloud integration, we recommend to use the <a href='/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud'><b>Git service integration</b></a> panel for connecting multiple git repositories. It provides additional features that are not present with SSH integrations in Jira Cloud.
    </div>
    </div>
</div>

<br>

<kbd>Last updated: December 2025</kbd>

