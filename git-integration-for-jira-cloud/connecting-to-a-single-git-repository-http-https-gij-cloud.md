---

title: Connecting to a Single Git Repository (HTTP/HTTPS)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This process requires an existing git host repository. Obtain the **HTTPS** git clone URL from the repository home of your git host service. The figure below is an example from GitHub:

![](/wp-content/uploads/gij-github-single-repo-demo-clone-url.png)


To connect a git repository to Jira via the Git Integration for Jira app:

1.  On your Jira dashboard menu, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup.png)

3.  On the following screen, at the Quick start integration section of the page:

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-single-repo-sel-https.png)

    *   Click on the **HTTPS** tab.
    *   Enter the git clone URL on the provided box.

4.  Click **Connect** to complete this process.

    *   If prompted, enter login credentials for this repository integration. If 2FA is enabled for this account, enter the personal access token (PAT) for the password instead.

    *   Enable/disable [SSL Verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud-gij-cloud) for this repository integration.

The repository is now connected for use with Jira.

You may also configure repository settings for this integration via:

*   Manage integration page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit integration ➜ Feature settings.

*   Manage repositories page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit repository ➜ Feature settings.

<br>
<br>
<hr>
<br>
<br>

[**« Prev:** Introduction to Git integration](/git-integration-for-jira-cloud/introduction-to-git-integration-gij-cloud)

[**» Next:** Connecting to a Single Git Repository (SSH)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-ssh-gij-cloud)

