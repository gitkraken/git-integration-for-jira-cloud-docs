---

title: GitHub App integration
description: How to integrate GitHub repositories using the GitHub App with Jira Cloud
taxonomy:
    category: git-integration-for-jira-cloud

---

GitHub offers a variety of integration options, including: API, OAuth, and more recently GitHub Apps. There are a number of benefits to using GitHub app over OAuth:

*   GitHub apps are by nature an organization installation. A separate GitHub account or service user is not required.

*   Because GitHub apps require GitHub administrator authorization, we can rely on the GitHub app having administrator permissions.

*   Determine repository access at the organization or repository level for the integration

*   GitHub apps have a higher rate limit than OAuth.

For more details, see the [GitHub Apps article](https://docs.github.com/en/developers/apps/getting-started-with-apps/differences-between-github-apps-and-oauth-apps).

### New integration options

A new integration option is added into the Add integration Connect screen:

1.  GitHub App (GitHub.com and GitHub Enterprise Cloud)

There are two terms:

*   **GitHub Application (GHA)** – GHA itself is a set of authorization information. It is created in some GitHub organization during the first step of connecting a GHA integration with the Git Integration for Jira app.  

*   **Installation of a GitHub Application** –  To get access to repositories inside the organization, an admin has to install the GHA in the organization. During the installation of GHA, the administrator selects the scope that will be available for this installation of this GHA. It is the second step of connecting a GHA integration.

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

Check GitHub Apps permission for your organization:

1.  On your GitHub web portal, go to your organization ➜ **Settings** tab.

2.  On the sidebar, click Developer settings ➜ **GitHub Apps**.

![](/wp-content/uploads/gij-github-app-org-setting-GHA-c.png)

&nbsp;

### Pre-requisites

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 3px; font-size: small;padding:2px 7px'>IMPORTANT!</b>

*   As an initial configuration requirement, admins need to install the GHA in an organization. After this setup, only then that Jira instance can read the repositories with Git Integration for Jira app.

&nbsp;

### Limitations

*   If you remove the GitHub App integration from the Manage Integrations screen, remember that this does not remove the GitHub App from the GitHub Organization. Make sure you uninstall the corresponding GitHub App from the GitHub Organization after disconnecting the integration.

&nbsp;

### Integrate to a GitHub App

1.  On your Jira dashboard menu, go to Apps ➜ **Git Integration for Jira by GitKraken**.

    ![](/wp-content/uploads/gij-github-app-integrations.png)

2.  On the top right corner, click on the Add integration button. **GitHub**.

3.  Click on the GitHub App option

    ![](/wp-content/uploads/github-app-integration.png)

4.  Enter **Organization name**.

5.  Click **Connect GitHub.com** to continue.

    ![](/wp-content/uploads/gij-github-app-create-app.png)

6. Click **Create GitHub App…** to proceed.

7. Choose:

    *   **All repositories** – to connect all repositories from this organization.

    *   **Only select repositories** – lets you select a specific repository for this setup.

    ![](/wp-content/uploads/gij-github-app-install-app.png)

8. Click **Install** to complete this process.

9. Select the repositories and click on **Connect repositories**

    ![](/wp-content/uploads/gij-github-app-select-repos.png)

10.  On the *Configure Additional options* screen, change the configuration according your needs. You can change:
    
    *   Integration display name

    *   Require User PAT - If you will have users create branches and pull requests

    *   Indexing Triggers

    *   Project permissions

    ![](/wp-content/uploads/gij-github-app-int-setting.png)

11. Click on **Save options**

    The GitHub App integration is now displayed in the Git repositories configuration list.

&nbsp;

### Post-install notes

The GitHub App is created automatically by the Git Integration for Jira app. For any related questions, please contact [gijsupport@gitkraken.com](mailto:gijsupport@gitkraken.com.)

*   You can reconfigure connected repositories in the Edit integration settings page for this GitHub App integration.
    ![](/wp-content/uploads/gij-github-app-edit-integration.png)

*   Make sure that the following properties are not be changed for this GitHub App integration:
    *   **GitHub App name**
    *   Post installation
    *   Webhook attributes
    *   Private keys
    *   Any settings on the Permissions and Events page
    *   Any settings on the installation page

*   Admins can restrict repositories using the JMESpath filter to avoid a case when a user tries to connect thousands of heavy repositories resulting in decreased Jira performance.

*   A GitHub installation can be suspended in two ways:
    *   **_From the owner side_** -- Press **Disconnect Integration** on the Integration Connection settings for the selected integration via Git Integration for Jira actions. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 3px; font-size: small;padding:2px 7px'>RECOMMENDED</b>
    *   **_From the user side_** -- Press **Suspend** on the GitHub portal for the GHA installation. <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 3px; font-size: small;padding:2px 7px'>NOT RECOMMENDED</b>

*   A GitHub App must be deleted by its owner. If several users have access to Repository Management, only one of them can actually remove the app from the Git server after the GitHub App integration is removed.

&nbsp;

[**Back to:** Integration basics](/git-integration-for-jira-cloud/introduction-to-git-integration-gij-cloud) (Git Integration for Jira Cloud)

---

### More Git Integration for Jira app features

See the [Features section](/git-integration-for-jira-cloud/features-gij-cloud) to learn more about Git Integration for Jira app features.

