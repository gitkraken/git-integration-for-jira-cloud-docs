---

title: Connecting to a Single Git Repository (HTTP/HTTPS)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
This process requires an existing git host repository. Obtain the **HTTPS** git clone URL from the repository home of your git host service. The figure below is an example from GitHub:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/923238448/github-single-repo-demo-clone-url.png?version=1&modificationDate=1648631602082&cacheVersion=1&api=v2&width=680&height=389)


To connect a git repository to Jira via the Git Integration for Jira app:

1.  On your Jira dashboard menu, go to **Apps** ➜ **Git Integration: Manage integrations**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/923238448/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1648628168314&cacheVersion=1&api=v2)

2.  On the Manage integrations page, click **Add integration.**

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/923238448/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1648628220465&cacheVersion=1&api=v2)

3.  On the following screen, click on the **Single git repository integration** panel for your integration type.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/923238448/gitcloud-managed-ui-single-repo-sel(c).png?version=1&modificationDate=1648630480246&cacheVersion=1&api=v2)

4.  The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/923238448/gitcloud-managed-ui-single-repo-add-new-http(c).png?version=1&modificationDate=1648631775497&cacheVersion=1&api=v2)
    *   For the **Host URL**, enter the HTTP/HTTPS repository git clone URL. Initially, this URL can be obtained from the repository's project page.

    *   Enter login credentials for this repository integration. If 2FA is enabled for this account, enter the personal access token (PAT) for the password instead.

    *   Enable/disable [SSL Verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud-gij-cloud/) for this repository integration.

5.  Click **Add integration** to complete this setup.


The repository is now connected for use with Jira.

