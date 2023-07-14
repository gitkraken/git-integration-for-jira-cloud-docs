---

title: SSH FAQ
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This page contains related questions on Git Integration for Jira Cloud app SSH connections in Jira.

Use the FAQ below to find answers to common questions. Feel free to contact our [support team](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/) if you don't see what you're looking for.

- [Does this app support authenticating to git repositories via SSH?](#does-this-app-support-authenticating-to-git-repositories-via-ssh)
- [Why do I need to provide a PRIVATE KEY to the Git Integration for Jira Cloud app instead of a PUBLIC KEY?](#why-do-i-need-to-provide-a-private-key-to-the-git-integration-for-jira-cloud-app-instead-of-a-public-key)
- [How do I configure/connect an SSH remote git repository to Jira?](#how-do-i-configureconnect-an-ssh-remote-git-repository-to-jira)

&nbsp;
* * *
&nbsp;

### Does this app support authenticating to git repositories via SSH?

Yes.

SSH keys with and without passphrases are supported.

&nbsp;

### Why do I need to provide a PRIVATE KEY to the Git Integration for Jira Cloud app instead of a PUBLIC KEY?

The PRIVATE KEY is needed by the SSH client, which is the Jira Cloud, to connect to the Git server via SSH.

&nbsp;

### How do I configure/connect an SSH remote git repository to Jira?

In Jira, use the **[Plain git integration](/git-integration-for-jira-cloud/using-the-single-git-integration-wizard-gij-cloud/)** wizard to configure SSH integration with any remote git repositories.

Here's a video to guide you step-by-step as stated above:

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/qmumdo048n?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align="center" style='margin-top:10px'>
    <i>Watch the video guide by clicking <a href="https://bigbrassband.wistia.com/medias/qmumdo048n" target="_blank"><b>here</b></a> to open this video in a new browser tab<br> for more viewing options.</i>
</div>

