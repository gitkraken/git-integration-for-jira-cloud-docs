---

title: Edit integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

On the Manage integrations page. click on <img src='/wp-content/uploads/actions-icon.png' style='margin: 0 3px' /> Actions ➜ **Edit integration** for the selected integration to open its configuration page.

![](/wp-content/uploads/gitcloud-manage-integration-actions-edit-cfg.png)

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The displayed options and settings depends on the type of connected git service.
    </div>
    </div>
</div>

&nbsp;

## Connection settings

![](/wp-content/uploads/gitcloud-edit-integration-connection-cfg.png)

The connection settings page contains configuration options to manage integration connection and displayed repositories.

Utilize the following options to configure the selected integration:

| Option | Description |
| :--- | :--- |
| _**Enable this integration**_ | Toggle to enable or disable this integration for use with Jira. |
| _**Reconnect**_ | Click on this button to refresh the integration connection and indexing. |
| _**Display Name**_ | This is the name that will appear on the Integration column in the Manage integrations page. |
| _Advanced:_  <br>_**Custom API Path**_ | The Git Integration for Jira app supports this feature for GitHub and GitLab integrations. For more details, see [**Working with Custom API Path**](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud/). |
| _Advanced:_  <br>_**JMESPath Filters**_ | JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. For more information, see [**Working with JMESPath Filters**](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud/). |

&nbsp;

## Feature settings

![](/wp-content/uploads/gij-gitcloud-edit-integration-features-cfg.png)

The Feature settings page contains configuration options related to user and project access, and the indexing triggers URL.

| Option | Description |
| :--- | :--- |
| _**Indexing triggers**_ | This is the automatically-generated webhook URL upon installation of Git Integration for Jira Cloud app.<br><br>Use the URL to setup webhook triggers to your git host service which allows immediate reindex of connected integrations. |
| _**Require User PAT**_ | Enable this option to require users to provide PAT which will be used for branch and merge/pull request creation/deletion (via the developer panel on the Jira issue page). This is a security feature of Git Integration for Jira app for git hosts that support two-factor authentication.<br><div class="bbb-callout bbb--tip"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">This option requires the <a href='/git-integration-for-jira-cloud/repository-browser-gij-cloud'>Repository Browser</a>() feature enabled.</div></div></div><br><div class="bbb-callout bbb--info"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">This setting is only available for integrations connected via <a href='/git-integration-for-jira-cloud/introduction-to-git-integration-gij-cloud/'>Git service integration panel.</div></div></div> |
| _**Project permissions**_ | This feature allows administrators to configure project associations with repositories/integration to restrict which users can view development information. For more information, see [Associating project permissions](/git-integration-for-jira-cloud/associating-project-permissions-gij-cloud/). |

&nbsp;

## Choose repositories

![](/wp-content/uploads/gij-gitcloud-managed-ui-github-repo-sel.png)

The Choose repositories settings page contains configuration options to manage which repositories to connect to Jira.

Adjacent to the **Search** function are the search filters for which repositories are to be displayed.

On the panel highlighted in blue are selection options for which repositories to connect. Repositories inside an organization can also be included (provided that the current service user has access permissions for these).

On the **Organizations** section, select all or specific repositories to connect to Jira.

* * *

Click **Cancel** to return to the Manage integrations page and discard the changes made to the settings.

Click **Save** to save the changes and apply the integration settings.

&nbsp;
* * *
&nbsp;

[**Prev:** Managing integrations via Actions (Jira Cloud)](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud/)

[**Next:** https://help.gitkraken.com/git-integration-for-jira-cloud/edit-repository-gij-cloud/](/git-integration-for-jira-cloud/edit-repository-gij-cloud/)

### More related topics about managing repository/integration configuration

[Managing integration or repository configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Managing integrations via Actions (Jira Cloud)](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud/) (Git Integration for Jira Cloud)

**Edit integration** (this page)

[Edit repository](/git-integration-for-jira-cloud/edit-repository-gij-cloud/) (Git Integration for Jira Cloud)

[SSL Verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud/) (Git Integration for Jira Cloud)

[View repository indexing logs](/git-integration-for-jira-cloud/view-repository-indexing-logs-gij-cloud/) (Git Integration for Jira Cloud)

[Removing integration or repository configuration](/git-integration-for-jira-cloud/removing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Associating project permissions](/git-integration-for-jira-cloud/associating-project-permissions-gij-cloud/) (Git Integration for Jira Cloud)

