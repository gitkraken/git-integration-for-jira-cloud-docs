---
title: Connecting SSH Git Repositories to Jira Cloud
description: Learn how to connect SSH git repositories to Jira Cloud, including SSH key generation and configuration.
taxonomy:
    category: git-integration-for-jira-cloud
---

Connect SSH git repositories to Jira Cloud using [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview).

**On this page:**
- [Generate SSH keys](#generate-ssh-keys)
  - [Generate SSH keys on Windows](#generate-ssh-keys-on-windows)
  - [Generate SSH keys on Linux/MacOS](#generate-ssh-keys-on-linuxmacos)
- [Convert SSH key format](#convert-ssh-key-format)
- [Connect an SSH git repository](#connect-an-ssh-git-repository)

&nbsp;
* * *
&nbsp;

## Generate SSH Keys

Before connecting an SSH repository, generate an SSH key pair. Use a **4096-bit RSA key** for optimal security.

&nbsp;

### Generate SSH Keys on Windows

Windows users should use [PuTTY](https://www.putty.org/) and PuTTYgen to generate SSH keys.

<img src='/wp-content/uploads/gij-workting-with-puttygen-key-dlg.png' style='margin: 25px auto;max-width:100%;' />

1. Launch **PuTTYgen**.

2. Set **Type of key to generate** to **RSA**.

3. Set **Number of bits in a generated key** to **4096**.

4. Click **Generate**.

5. Move your mouse pointer randomly over the blank area until the progress bar fills and the key pair generates.

6. (Optional) Enter a **Passphrase** to secure the key.

7. Click **Save public key** and **Save private key** to save both keys to files.

8. Copy the generated public key from the text box. Use this key on your git host's SSH configuration page.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        PuTTY saves private keys in its proprietary ".ppk" format. To convert to ".pem" format:
        <ol style='margin-bottom:0px !important'>
            <li>In PuTTYgen, select <b>Conversions</b> ➜ <b>Export OpenSSH key</b>.</li>
            <li>Upload this file to Git Integration for Jira ➜ <b>SSH keys</b>, or provide it when connecting SSH git repositories.</li>
        </ol>
    </div>
    </div>
</div>

You can also generate SSH keys using Git Bash. For details, see [Generate SSH via Git Bash](https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key).

For platform-specific instructions, see [Generating SSH Keys](/git-integration-for-jira-cloud/working-with-ssh-keys-gij-cloud).

&nbsp;

### Generate SSH Keys on Linux/MacOS

Run this command to generate an RSA SSH key:

```bash
ssh-keygen -t rsa -b 4096 -m pem -C "your_email@example.com"
```

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        MacOS sometimes creates OpenSSH format certificates instead of PEM format. For more details, see this <a href='https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key'>common issue and solution</a>.
    </div>
    </div>
</div>

&nbsp;

## Convert SSH Key Format

Git Integration for Jira requires RSA format for private SSH keys. Convert your existing key pair with this command:

```bash
ssh-keygen -p -P "old_password" -N "new_password" -m pem
```

&nbsp;

## Connect an SSH Git Repository

1. Generate an SSH key pair using the steps above.

2. Copy the SSH clone URL from your git host repository page.

3. In Jira, go to **Apps** ➜ **Git Integration: Manage integrations**.

4. Click **Add integration** in the top-right corner.

5. Under the **Self-hosted** group, select **Plain git repository**.

6. Paste the SSH clone URL into the **Host URL** field.

7. Paste your private SSH key into the text box, or click **Upload Key File** to upload the key file.

8. Enter the key's **Passphrase** if you set one. Otherwise, leave it blank.

9. Click **Add Integration** to complete the setup.

The connected repository appears in your git configuration page.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For Jira Cloud, we recommend using the <a href='/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud'><b>Git service integration</b></a> panel to connect multiple repositories. It provides additional features not available with SSH integrations.
    </div>
    </div>
</div>

<kbd>Last updated: December 2025</kbd>
