---

title: Connecting to a Single Git Repository (SSH)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This process requires an existing git host repository. Obtain the **SSH** git clone URL from the repository home of your git host service. The figure below is an example from GitHub:

![](/wp-content/uploads/gij-gitcloud-github-clone-repo-url-ssh.png)


To connect a git repository to Jira via the Git Integration for Jira app:

1.  On your Jira dashboard menu, go to **Apps** ➜ **Git Integration: Manage integrations.**

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup.png)

3.  On the following screen, at the Quick start integration section of the page:

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-single-repo-sel-ssh.png)

    *   Click on the **SSH** tab.
    *   Enter the git clone URL on the provided box.

4.  Click **Connect** to complete this process.

    *   If prompted, enter login credentials for this repository integration. If 2FA is enabled for this account, enter the personal access token (PAT) for the password instead.

    *   Enable/disable [SSL Verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud-gij-cloud) for this repository integration.

The repository is now connected for use with Jira.

You may also configure repository settings for this integration via:

*   Manage integration page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit integration ➜ Feature settings.

*   Manage repositories page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit repository ➜ Feature settings.

&nbsp;
* * *
&nbsp;

[**Prev:** Connecting to a Single Git Repository (HTTP/HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

[**Next:** Setting up weblinks](/git-integration-for-jira-cloud/setting-up-web-links-gij-cloud)


