---

title: GitHub App integration
description: How to integrate GitHub repositories using the GitHub App with Jira Cloud
taxonomy:
    category: git-integration-for-jira-cloud

---

GitHub offers several integration options: API, OAuth, and GitHub Apps. GitHub Apps provide these advantages over OAuth:

*   GitHub Apps install at the organization level without requiring a separate GitHub account or service user.

*   GitHub Apps require administrator authorization, ensuring consistent admin-level permissions.

*   You can control repository access at the organization or repository level.

*   GitHub Apps have higher rate limits than OAuth.

For more details, see the [GitHub Apps article](https://docs.github.com/en/developers/apps/getting-started-with-apps/differences-between-github-apps-and-oauth-apps).

### New integration options

The Add integration screen includes a GitHub App option for GitHub.com and GitHub Enterprise Cloud.

Key terms:

*   **GitHub Application (GHA)** – A set of authorization information created in a GitHub organization during the first step of connecting a GHA integration with Git Integration for Jira.

*   **GHA Installation** – To access repositories in an organization, an admin installs the GHA and selects the available scope. This is the second step of connecting a GHA integration.

&nbsp;

### Permissions

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        You must be a GitHub organization owner or have GitHub admin permissions in a repository to install/uninstall a GitHub App on that organization. If a GitHub App is installed in a repository and requires organization permissions, the GitHub organization owner must approve the application.
    </div>
    </div>
</div>

To check GitHub Apps permissions for your organization:

1.  In your GitHub web portal, go to your organization ➜ **Settings** tab.

2.  In the sidebar, click Developer settings ➜ **GitHub Apps**.

![](/wp-content/uploads/gij-github-app-org-setting-GHA-c.png)

&nbsp;

### Pre-requisites

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 3px; font-size: small;padding:2px 7px'>IMPORTANT!</b>

*   Admins must install the GHA in an organization before the Jira instance can read repositories with Git Integration for Jira.

&nbsp;

### Limitations

*   If you remove the GitHub App integration from the Manage Integrations screen, remember that this does not remove the GitHub App from the GitHub Organization. Make sure you uninstall the corresponding GitHub App from the GitHub Organization after disconnecting the integration.

&nbsp;

### Integrate to a GitHub App

1.  In your Jira dashboard menu, go to Apps ➜ **Git Integration for Jira by GitKraken**.

    ![](/wp-content/uploads/gij-github-app-integrations.png)

2.  Click **Add integration** in the top right corner, then select **GitHub**.

3.  Click **GitHub App**.

    ![](/wp-content/uploads/github-app-integration.png)

4.  Enter your **Organization name**.

5.  Click **Connect GitHub.com**.

    ![](/wp-content/uploads/gij-github-app-create-app.png)

6.  Click **Create GitHub App…**.

7.  Choose a repository scope:

    *   **All repositories** – Connects all repositories from this organization.

    *   **Only select repositories** – Lets you select specific repositories.

    ![](/wp-content/uploads/gij-github-app-install-app.png)

8.  Click **Install**.

9.  Select the repositories and click **Connect repositories**.

    ![](/wp-content/uploads/gij-github-app-select-repos.png)

10. On the **Configure Additional options** screen, configure these settings:
    
    *   Integration display name

    *   Require User PAT (if users will create branches and pull requests)

    *   Indexing Triggers

    *   Project permissions

    ![](/wp-content/uploads/gij-github-app-int-setting.png)

11. Click **Save options**.

    The GitHub App integration now appears in the Git repositories configuration list.

&nbsp;

### Post-install notes

Git Integration for Jira creates the GitHub App automatically. For questions, contact [gijsupport@gitkraken.com](mailto:gijsupport@gitkraken.com).

*   Reconfigure connected repositories in the Edit integration settings page for this GitHub App integration.
    ![](/wp-content/uploads/gij-github-app-edit-integration.png)

*   Do not change these GitHub App properties:
    *   **GitHub App name**
    *   Post installation
    *   Webhook attributes
    *   Private keys
    *   Settings on the Permissions and Events page
    *   Settings on the installation page

*   Use the JMESpath filter to restrict repositories and prevent users from connecting thousands of repositories, which can decrease Jira performance.

*   Suspend a GitHub installation using one of these methods:
    *   **From the owner side** – Click **Disconnect Integration** in the Integration Connection settings for the selected integration via Git Integration for Jira actions. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 3px; font-size: small;padding:2px 7px'>RECOMMENDED</b>
    *   **From the user side** – Click **Suspend** on the GitHub portal for the GHA installation. <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 3px; font-size: small;padding:2px 7px'>NOT RECOMMENDED</b>

*   Only the owner can delete a GitHub App. If multiple users have Repository Management access, only one can remove the app from the Git server after the GitHub App integration is removed.

&nbsp;

[**Back to:** Integration basics](/git-integration-for-jira-cloud/introduction-to-git-integration-gij-cloud) (Git Integration for Jira Cloud)

---

### More Git Integration for Jira app features

See the [Features section](/git-integration-for-jira-cloud/features-gij-cloud) to learn more about Git Integration for Jira app features.

<kbd>Last updated: December 2025</kbd>
