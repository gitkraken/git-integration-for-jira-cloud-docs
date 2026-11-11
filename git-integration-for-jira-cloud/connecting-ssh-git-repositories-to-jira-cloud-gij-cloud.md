---
title: "Connecting SSH Git Repositories to Jira Cloud"
description: "Learn how to connect SSH git repositories to Jira Cloud, including SSH key generation and configuration."
product: "Git Integration for Jira Cloud"
feature: "Connecting SSH Git Repositories to Jira Cloud"
content_type: "security"
audience: "all"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "all"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "security"]
llms_include: true
taxonomy:
    category: git-integration-for-jira-cloud
custom_fields:
    nav_category: "how-to-articles-gij-cloud"
    nav_label: "Connecting SSH Git Repositories to Jira Cloud"
    nav_order: 100
    nav_parent: "how-to-articles-gij-cloud"
    page_type: "content"
---
<kbd>Last updated: March 2026</kbd>

Connect SSH git repositories to Jira Cloud using [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview).

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

> **Note:** PuTTY saves private keys in its proprietary ".ppk" format. To convert to ".pem" format:
>
> 1. In PuTTYgen, select **Conversions** ➜ **Export OpenSSH key**.
> 2. Upload this file to Git Integration for Jira ➜ **SSH keys**, or provide it when connecting SSH git repositories.

You can also generate SSH keys using Git Bash. For details, see [Generate SSH via Git Bash](https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key).

For platform-specific instructions, see [Generating SSH Keys](/git-integration-for-jira-cloud/working-with-ssh-keys-gij-cloud).

&nbsp;

### Generate SSH Keys on Linux/MacOS

Run this command to generate an RSA SSH key:

```bash
ssh-keygen -t rsa -b 4096 -m pem -C "your_email@example.com"
```

> **Warning:** MacOS sometimes creates OpenSSH format certificates instead of PEM format. For more details, see this [common issue and solution](https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key).

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

> **Note:** For Jira Cloud, we recommend using the [**Git service integration**](/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud) panel to connect multiple repositories. It provides additional features not available with SSH integrations.

