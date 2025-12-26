---

title: Edit repository settings
description: How to configure repository connection and feature settings
taxonomy:
    category: git-integration-for-jira-cloud

---

<b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>HOSTED</b> <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>EXTERNAL</b>

On the Manage repositories page, click ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit repository** for the selected repository to open its repository configuration page where you can change connection settings.

![](/wp-content/uploads/gij-gitcloud-edit-repo-cfg-single-repo-2025.png)

Use the options below to configure repository settings.

&nbsp;

## Connection Settings

| Option | Description | Repository type |
| :--- | :--- | :--- |
| _**Enable this integration**_ | Toggle to enable/disable this repository for use with Jira. | SINGLE<br> INTEGRATION |
| _**Display Name**_ | This is the alias that appears in the Repository column. | SINGLE<br> INTEGRATION |
| _**Repository Origin**_ | This is the URL path to a clone of the repository. | INTEGRATION |
| _**Username, Password/Token**_ | Displays username used for this repository configuration. Enter a new password/token if the password/token has changed since the last configuration. | SINGLE |
| _**Private SSH Key**_ | If the private SSH key was changed, enter the new private SSH key in the provided box or upload the new private SSH key. | SINGLE |
| _**Optional SSH Key Passphrase**_ | If the configured private SSH key has a passphrase, enter it in the provided box. | SINGLE |
| _**SSL Verify**_ | <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>VSTS/AZURE</b> <b style='background-color:#FFEED1; padding:1px 5px; color:#CC5900; border-radius:3px; margin: 0 5px; font-size: small;'>GITLAB</b> <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>GITHUB</b><br>Set to enabled/disabled for the current git host integration.<br><br>The **SSL Verify** option is set to `Enabled` by default. If set to `Disabled`, Git Integration for Jira ignores verification of SSL certificates when connecting to a git server.<br><div class="bbb-callout bbb--info" style='margin-bottom:0px'><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">The <b>SSL Verify</b> setting is available in Jira Server, Data Center, and Jira Cloud. This option is not available for non-fetched repositories.</div></div></div> | SINGLE |

&nbsp;

## Feature Settings

| Option | Description | Repository type |
| :--- | :--- | :--- |
| _**Main Branch**_ | Set the main branch. The default setting is `master`. | SINGLE, <br>INTEGRATION |
| _**Indexing triggers**_ | Displays the indexing triggers URL for this repository. Click the adjacent copy icon to send the indexing triggers URL to the system clipboard. Use this URL to set up webhook to your git host service. | SINGLE, <br>INTEGRATION |
| _**Tags**_ | Set whether to show all tags or show only tags with matching regex pattern. For more information on git tags, see [Git tags](/git-integration-for-jira-cloud/git-tags-gij-cloud). | SINGLE, <br>INTEGRATION |
| _**Smart Commits & Workflow Triggers**_ | Enable/disable this setting to allow users to use the [smart commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud) feature. | SINGLE, <br>INTEGRATION |
| _**Project Permissions: Restrict to projects**_ | The default setting is **Associate with all projects**. You can restrict access to the Repository Browser and Git Commit tabs (Advanced) for the selected repository by [setting the project associations](/git-integration-for-jira-cloud/associating-project-permissions-gij-cloud). | SINGLE, <br>INTEGRATION |
| _**Web Linking**_ | _Optional._<br><br>The web linking feature adds links to your git hosting provider directly into the Git Commits tab. For special integrations (Auto-Connect), this feature is configured automatically. For more information, see [Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud). | SINGLE |

&nbsp;

Click **Save** to save the changes and apply the settings.

Click **Cancel** to return to the manage git configuration page and discard the changes.

&nbsp;
* * *

[**Prev:** Edit integration settings](/git-integration-for-jira-cloud/edit-integration-gij-cloud/)

[**Next:** Edit nested repository settings](/git-integration-for-jira-cloud/edit-nested-repository-settings-gij-cloud/)

&nbsp;

### More Related Topics About Managing Repository/Integration Configuration

[Managing integration or repository configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Managing integrations via Actions (Jira Cloud)](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud/) (Git Integration for Jira Cloud)

[Edit integration settings](/git-integration-for-jira-cloud/edit-integration-gij-cloud/)

**Edit repository settings** (this page)

[Edit nested repository settings](/git-integration-for-jira-cloud/edit-nested-repository-settings-gij-cloud/) (Git Integration for Jira Cloud)

[SSL verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud/) (Git Integration for Jira Cloud)

[View repository indexing logs](/git-integration-for-jira-cloud/view-repository-indexing-logs-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect an integration or repository configuration](/git-integration-for-jira-cloud/removing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect a nested repository configuration](/git-integration-for-jira-cloud/removing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Associating project permissions](/git-integration-for-jira-cloud/associating-project-permissions-gij-cloud/) (Git Integration for Jira Cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
