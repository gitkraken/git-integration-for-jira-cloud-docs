---

title: Connecting to a Single Git Repository (SSH)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This process requires an existing git host repository. Obtain the **SSH** git clone URL from the repository home of your git host service. The figure below is an example from GitHub:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/923238489/gitcloud-github-clone-repo-url-ssh.png?version=1&modificationDate=1648633431257&cacheVersion=1&api=v2&width=680&height=382)


To connect a git repository to Jira via the Git Integration for Jira app:

1.  On your Jira dashboard menu, go to **Apps** ➜ **Git Integration: Manage integrations.**

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/923238489/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1648633621940&cacheVersion=1&api=v2)

2.  On the Manage integrations page, click **Add integration.**

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/923238489/gitcloud-managed-ui-webhook-idx-setup(c).png?version=2&modificationDate=1648634005172&cacheVersion=1&api=v2)

3.  On the following screen, click on the **Single git repository integration** panel for your integration type.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/923238489/gitcloud-managed-ui-single-repo-sel(c).png?version=1&modificationDate=1648634134113&cacheVersion=1&api=v2)

4.  The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/923238489/gitcloud-managed-ui-single-repo-add-new-ssh-2(c).png?version=1&modificationDate=1648634474929&cacheVersion=1&api=v2)
    *   For the **Host URL**, enter the SSH repository git clone URL. Initially, this URL can be obtained from the repository's project page. Configuration options for SSH settings are displayed.

    *   For SSH credentials, upload or paste the private SSH key in the respective box. _If your SSH key has a passphrase, enter it on the provided box._

5.  Click **Add integration** to complete this setup.


The repository is now connected for use with Jira.

