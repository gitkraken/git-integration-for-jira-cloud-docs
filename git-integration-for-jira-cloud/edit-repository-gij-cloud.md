---

title: Edit repository
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
<b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>HOSTED</b> <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>EXTERNAL</b>

On the Manage repositories page, click Actions ➜ **Edit repository** for the selected repository to open its repository configuration page where you can change the settings of the connected repository.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1977384961/gitcloud-edit-repo-cfg-single-repo.png?version=1&modificationDate=1648989722770&cacheVersion=1&api=v2)

Utilize the options below for configuring repository settings.

## Connection settings

| Option | Description | Repository type |
| :--- | :--- | :--- |
| _**Enable this integration**_ | Toggle to enable/disable this repository for use with Jira. | SINGLE, <br>INTEGRATION |
| _**Display Name**_ | This is the alias that will appear in the Repository column. | SINGLE, <br>INTEGRATION |
| _**Repository Origin**_ | This is the URL path to a clone of the repository. | INTEGRATION |
| _**Username, Password/Token**_ | Displays username used for this repository configuration. Enter a new password/token if the password/token has changed since the last configuration. | SINGLE |
| _**Private SSH Key**_ | If the private SSH key was changed, enter the new private SSH key on the provided box or upload the new private SSH key. | SINGLE |
| _**Optional SSH Key Passphrase**_ | If the configured private SSH key has a passphrase, enter it on the provided box. | SINGLE |
| _**SSL Verify**_ | VSTS \| AZURE GITLAB GITHUB  <br>Set to enabled/disabled for the current git host integration.<br><br>The **SSL Verify** option is set to `Enabled` by default. If set to `Disabled`, the Git Integration for Jira app will ignore verification of SSL certificates when connecting to a git server.<br><br>The **SSL Verify** setting is available in Jira Server, Data Center and Jira Cloud. This option is not available for non-fetched repositories. | SINGLE |

<br>

## Feature settings

| Option | Description | Repository type |
| :--- | :--- | :--- |
| _**Main Branch**_ | Set the main branch. The default setting is `master`. | SINGLE, <br>INTEGRATION |
| _**Indexing triggers**_ | Displays the indexing triggers URL for this repository. Click the adjacent copy icon to send the indexing triggers URL to the system clipboard. Use this URL to setup webhook to your git host service. | SINGLE, <br>INTEGRATION |
| _**Tags**_ | Set whether to show all tags or show on tags with matching regex pattern. For more information on git tags, see [Git tags](/git-integration-for-jira-cloud/git-tags-gij-cloud). | SINGLE, <br>INTEGRATION |
| _**Smart Commits & Workflow Triggers**_ | Enable/disable this setting to allows the users to use the [smart commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud) feature. | SINGLE, <br>INTEGRATION |
| _**Project Permissions: Restrict to projects**_ | The default setting is **Associate with all projects**. You can restrict access to the Repository Browser and Git Commit tabs (Advanced) for the selected repository by [setting the project associations](/git-integration-for-jira-cloud/associating-project-permissions-gij-cloud). | SINGLE, <br>INTEGRATION |
| _**Web Linking**_ | _Optional._<br><br>The web linking feature adds links to your git hosting provider directly into the Git Commits tab. For special integrations (Auto-Connect), this feature is configured automatically. For more information on about this topic, see [Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud). | SINGLE |

Click **Save** to save the changes and apply the settings.

Click **Cancel** to return to the manage git configuration page and discard the changes.

