---

title: Connecting SSH Git Repositories (Jira Cloud)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
SSH git repositories can be integrated with Jira Cloud via Git Integration for Jira app.

1.  [**Generate an SSH key pair**](/wiki/spaces/GITCLOUD/pages/1923023617/Working+with+SSH+keys). We recommend to generate a 4096-bit key.

2.  Obtain the SSH git clone URL from your git host repository page.

3.  On your Jira Cloud dashboard, go to menu Apps ➜ **Git Integration:** **Manage Git repositories**. The following screen is displayed.

4.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923023732/gitcloud-connect-ssh-repo(c).png?version=1&modificationDate=1631014765738&cacheVersion=1&api=v2&width=646&height=340)

    On the Full feature integrations panel, click **Git**. The Connect to Git Repository wizard is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923023732/gitcloud-ssh-connect-gitrepo(c).png?version=1&modificationDate=1631014765746&cacheVersion=1&api=v2&width=544&height=382)
    *   Paste the clone URL into the **Remote Git URL** field.

5.  Click **Next**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923023732/gitcloud-connect-ssh-repo-addkey(c).png?version=1&modificationDate=1631014765751&cacheVersion=1&api=v2&width=646&height=298)
    *   Paste the private SSH key on the provided box or click **Upload Key File** to upload a private SSH key file.

    *   Enter the _**Passphrase**_ of the private SSH key, if any. Otherwise, leave it blank.

6.  Click **Connect** to complete this setup.



The connected repository is listed in the git configuration page.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923023732/gitcloud-connect-ssh-repo-cfg-list.png?version=1&modificationDate=1631014765755&cacheVersion=1&api=v2)

For Jira Cloud integration, we recommend to use the Auto-connect integration panel for connecting git repositories. It supports multiple git repository connections and provides additional features that are not present in SSH integration.

[« Generating SSH keys](/wiki/spaces/GITCLOUD/pages/1923023647/Generating+SSH+Keys)

[Adding a public SSH key »](/wiki/spaces/GITCLOUD/pages/1923023758/Adding+a+public+SSH+Key)

