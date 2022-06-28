---

title: Edit integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
On the Manage integrations page. click on Actions ➜ **Edit integration** for the selected integration to open its configuration page.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923024559/gitcloud-manage-integration-actions-edit-cfg.png?version=1&modificationDate=1648985387880&cacheVersion=1&api=v2&width=680&height=271)

The displayed options and settings depends on the type of connected git service.

## Connection settings

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923024559/gitcloud-edit-integration-connection-cfg.png?version=2&modificationDate=1648985663542&cacheVersion=1&api=v2&width=680&height=595)

The connection settings page contains configuration options to manage integration connection and displayed repositories.

Utilize the following options to configure the selected integration:

| **Option** | **Description** |
| --- | --- |
| _**Enable this integration**_ | Toggle to enable or disable this integration for use with Jira. |
| _**Reconnect**_ | Click on this button to refresh the integration connection and indexing. |
| _**Display Name**_ | This is the name that will appear on the Integration column in the Manage integrations page. |
| _Advanced:_  <br>_**Custom API Path**_ | The Git Integration for Jira app supports this feature for GitHub and GitLab integrations. For more details, see [**Working with Custom API Path**](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud). |
| _Advanced:_  <br>_**JMESPath Filters**_ | JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. For more information, see [**Working with JMESPath Filters**](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud). |

## Feature settings

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024559/gitcloud-manage-integrations-actions-edit-cfg-02.png?version=1&modificationDate=1648986619409&cacheVersion=1&api=v2)

The Feature settings page contains configuration options related to user and project access, and the indexing triggers URL.

| **Option** | **Description** |
| --- | --- |
| _**Indexing triggers**_ | This is the automatically-generated webhook URL upon installation of Git Integration for Jira Cloud app.<br><br>Use the URL to setup webhook triggers to your git host service which allows immediate reindex of connected integrations. |
| _**Require User PAT**_ | Enable this option to require users to provide PAT which will be used for branch and merge/pull request creation/deletion (via the developer panel on the Jira issue page). This is a security feature of Git Integration for Jira app for git hosts that support two-factor authentication.<br><br>This option requires the [**Repository Browser**](/git-integration-for-jira-cloud/repository-browser-gij-cloud) feature enabled.<br><br>This setting is only available for integrations connected via [**Git service integration** panel](/git-integration-for-jira-cloud/introduction-to-git-integration-gij-cloud). |
| _**Project permissions**_ | This feature allows administrators to configure project associations with repositories/integration to restrict which users can view development information. For more information, see [Associating project permissions](/git-integration-for-jira-cloud/associating-project-permissions-gij-cloud). |

## Choose repositories

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024559/gitcloud-edit-integration-cfg-choose-repos.png?version=1&modificationDate=1648987268485&cacheVersion=1&api=v2)

The Choose repositories settings page contains configuration options to manage which repositories to connect to Jira.

Adjacent to the Search function are the search filters for which repositories are to be displayed.

On the panel highlighted in blue are selection options for which repositories to connect. Repositories inside an organization can also be included (provided that the current service user has access permissions for these).

On the Organizations section, select all or specific repositories to connect to Jira.

* * *

Click **Cancel** to return to the Manage integrations page and discard the changes made to the settings.

Click **Save** to save the changes and apply the integration settings.


