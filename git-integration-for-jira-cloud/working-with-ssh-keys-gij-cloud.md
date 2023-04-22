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
<br>

## Getting started

Before connecting repositories via SSH, users are required to generate SSH keys for use with the remote git host (_public key_) and for Git Integration app in Jira (_private key_).

Generated SSH keys always come in pair. (**Example:** `id_rsa.pub` and `id_rsa`)

For establishing safety connection with SSH, upload a **public key** to the SSH server and set the **private key** to the SSH client.

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
        <p style='margin-bottom:0px !important'>For more information, see known issue <a href='/git-integration-for-jira-cloud/ssh-key-file-format-is-invalid-gij-cloud'>SSH key format is invalid</a>.</p>
    </div>
    </div>
</div>
<br>

## Windows

For Windows, we recommend to use [**PuTTY**](https://www.putty.org/) and use PuTTYgen to generate public and private SSH keys.

<img src='/wp-content/uploads/gij-workting-with-puttygen-key-dlg.png' style='margin:25px auto;display:block;max-width:100%' width=479px height=471px />

1.  Launch **PuTTYgen** and refer to the above image for the rest of the steps on this section.

2.  Set _**Type of key to generate**_ to **RSA**.

3.  Set _**Number of bits in a generated key**_ to **4096**.

4.  Click **Generate**.

5.  Follow screen instructions such as moving your mouse pointer on random locations on the blank area of the PuTTYgen dialog. Do this until the progress bar completely fills up and the SSH key pair is generated.

6.  Entering a **Passphrase** for the generated key is optional but will ensure a more secure connection.

7.  Save your generated public and private key to a file by clicking the respective options.

8.  Copy the generated key. This is the public key that you will be using on the SSH configuration page of your git host.

9.  For the private key, see the notes below.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        PuTTY creates a private key in its own ".ppk" format. To convert it to ".pem", the user should do the <b>Conversions</b> ➜ <b>Export OpenSSH key</b> menu option in PuTTYgen. Add/upload this file to Git Integration for Jira app ➜ <b>SSH keys</b> or when prompted on connecting SSH git repositories in Jira via Connect wizard.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        You can also use the git bash command line to generate SSH key pair. For detailed information, see <a href='https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key'><b>Generate SSH via Git bash</b></a>.
    </div>
    </div>
</div>
<br>

Read on the article, [Generating SSH Keys](/git-integration-for-jira-cloud/generating-ssh-keys-gij-cloud/), and follow specific information for the git host and platform that you use.

## Linux/MacOS

On Linux and MacOS, this generates an SSH key in RSA format:<br>
```ssh-keygen -t rsa -b 4096 -m pem -C "your_email@example.com"```

MacOS often incorrectly creates an OpenSSH format certificate. For more details, see information on this [**common problem**](https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key).

&nbsp;

* * *

&nbsp;

[**Prev:** Installation via Atlassian Marketplace](/git-integration-for-jira-cloud/installation-via-atlassian-marketplace-gij-cloud)

[**Next:** Generating SSH keys](/git-integration-for-jira-cloud/generating-ssh-keys-gij-cloud)

