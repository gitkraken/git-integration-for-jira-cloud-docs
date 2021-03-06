---

title: SSH FAQ
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This page contains related questions on Git Integration for Jira Cloud app SSH connections in Jira.

Use the FAQ below to find answers to common questions. Feel free to contact our support team ([support@bigbrassband.com](mailto:support@bigbrassband.com?subject=Help%20on%20SSH%20issues%20-)) if you don't see what you're looking for.

- [Does this app support authenticating to git repositories via SSH?](#does-this-app-support-authenticating-to-git-repositories-via-ssh)
- [Why do I need to provide a PRIVATE KEY to the Git Integration for Jira Cloud app instead of a PUBLIC KEY?](#why-do-i-need-to-provide-a-private-key-to-the-git-integration-for-jira-cloud-app-instead-of-a-public-key)
- [How do I configure/connect an SSH remote git repository to Jira?](#how-do-i-configureconnect-an-ssh-remote-git-repository-to-jira)

* * *

## Does this app support authenticating to git repositories via SSH?

Yes.

SSH keys with and without passphrases are supported.

## Why do I need to provide a PRIVATE KEY to the Git Integration for Jira Cloud app instead of a PUBLIC KEY?

The PRIVATE KEY is needed by the SSH client, which is the Jira Cloud, to connect to the Git server via SSH.

## How do I configure/connect an SSH remote git repository to Jira?

In Jira, use the **Connect to Git Repository** wizard to configure SSH integration with any remote git repositories.

1.  On your Jira dashboard > **Git** menu > **Manage git repositories**.
2.  Click **Connect to Git Repository**. The **Connect to Git Repository** wizard appears.
3.  Enter **Repository location** of your SSH git server. Click **Next**.
4.  Upload the private key or paste it on the provided field. Click **Next**.
5.  Enter **Passphrase** (if required). Click **Next**.
The wizard will start cloning the selected repository. When the process is complete, the Permissions dialog is displayed.6.  Leave settings as is and click **Next**.
7.  Click **Finish** to complete the setup. The repository is added to the repositories list.

Here's a video to guide you step-by-step as stated above:

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/qmumdo048n?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align="center">
    <i>Watch the video guide by clicking <a href="https://bigbrassband.wistia.com/medias/qmumdo048n" target="_blank"><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

