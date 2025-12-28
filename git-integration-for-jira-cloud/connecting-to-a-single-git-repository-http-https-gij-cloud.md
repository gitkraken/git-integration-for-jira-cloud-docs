---

title: Connecting to a Single Git Repository
description: Learn how to connect a single git repository to Jira Cloud using HTTP/HTTPS or SSH protocols with Git Integration for Jira.
taxonomy:
    category: git-integration-for-jira-cloud

---

This guide covers connecting a single git repository to Jira using either HTTP/HTTPS or SSH protocols.

**On this page:**
- [Connecting via HTTP/HTTPS](#connecting-via-httphttps)
- [Connecting via SSH](#connecting-via-ssh)
- [Configuring Repository Settings](#configuring-repository-settings)

&nbsp;

* * *

&nbsp;

## Connecting via HTTP/HTTPS

This process requires an existing git host repository. Obtain the **HTTPS** git clone URL from the repository home of your git host service. The figure below is an example from GitHub:

![](/wp-content/uploads/gij-github-single-repo-demo-clone-url-2025.png)

To connect a git repository to Jira via the Git Integration for Jira app:

1.  On your Jira dashboard menu, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-2025.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-2025.png)

3.  On the following screen, at the Quick start integration section of the page:

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-single-repo-sel-https-2025.png)

    *   Click on the **HTTPS** tab.
    *   Enter the git clone URL on the provided box.

4.  Click **Connect** to complete this process.

    *   If prompted, enter login credentials for this repository integration. If 2FA is enabled for this account, enter the personal access token (PAT) for the password instead.

    *   Enable/disable [SSL Verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud) for this repository integration.

The repository is now connected for use with Jira.

&nbsp;

* * *

&nbsp;

## Connecting via SSH

This process requires an existing git host repository. Obtain the **SSH** git clone URL from the repository home of your git host service. The figure below is an example from GitHub:

![](/wp-content/uploads/gij-gitcloud-github-clone-repo-url-ssh-2025.png)

To connect a git repository to Jira via the Git Integration for Jira app:

1.  On your Jira dashboard menu, go to **Apps** ➜ **Git Integration: Manage integrations.**

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-2025.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-2025.png)

3.  On the following screen, at the Quick start integration section of the page:

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-single-repo-sel-ssh-2025.png)

    *   Click on the **SSH** tab.
    *   Enter the git clone URL on the provided box.

4.  Click **Connect** to complete this process.

    *   If prompted, enter login credentials for this repository integration. If 2FA is enabled for this account, enter the personal access token (PAT) for the password instead.

    *   Enable/disable [SSL Verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud) for this repository integration.

The repository is now connected for use with Jira.

&nbsp;

* * *

&nbsp;

## Configuring Repository Settings

You may configure repository settings for this integration via:

*   Manage integration page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit integration ➜ Feature settings.

*   Manage repositories page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit repository ➜ Feature settings.

&nbsp;
* * *
&nbsp;

[**Prev:** Introduction to Git integration](/git-integration-for-jira-cloud/introduction-to-git-integration-gij-cloud)

[**Next:** Setting up weblinks](/git-integration-for-jira-cloud/setting-up-web-links-gij-cloud)

<br>

<kbd>Last updated: December 2025</kbd>

