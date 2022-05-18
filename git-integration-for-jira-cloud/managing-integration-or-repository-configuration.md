---

title: Managing integration or repository configuration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
After successfully integrating the git host service or connecting the git repositories via Git Integration for Jira app, modify integration or repository settings depending on the connection protocol of the repository or integration.

## Getting started

On the git integration configuration page, you can manage connected integrations such as adding, editing, or updating integration/repository settings or disconnect integrations/repositories.

## Manage integrations page

The Manage integrations page allows administrators to integrate and manage supported git host services in Jira.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024455/gitcloud-managed-ui-git-integration-list.png?version=1&modificationDate=1648189077493&cacheVersion=1&api=v2)

|     |     |
| --- | --- |
| **Column** | **Description** |
| **Integration** | Displays the integration display name or integration URL.<br><br>Click the integration name on the list to open the integration connection settings for the selected integration. |
| **Type** | Displays the type of integration for the connected git host service.<br><br>*   Git service – full feature integration<br>    <br>*   Webhook indexing – limited integration via webhooks |
| **Status** | Shows the index status of the integration.<br><br>*   It shows INDEXED if _Repository Root_ is configured correctly and the Jira instance can access it.<br>    <br>*   It shows RUNNING during reindexing of the connected integration.<br>    <br>*   A similar ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) icon appears before the status indicator to indicate that it is being queued for indexing.<br>    <br>*   It shows ERROR if the connected integration has connection issues with the configured git host service. |
| **Last indexed** | Shows the date and time the indexing service has checked if the integration repositories should be examined for changes.<br><br>For more information on Jira Cloud indexer, see [Jira Cloud: Classic indexing Explainer](#). |
| **Repositories** | Shows the counter for the number of repositories the connected integration has. |
| **Features** | ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) – The integration has a project association (solid) or not (hollow).<br><br>![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) – The integration has smart commits enabled (solid) or disabled (hollow).<br><br>![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) – The integration has enabled indexing triggers (solid) or not (hollow). |
| **Actions** | To the right of the **Features** column are actions that can be performed for the selected connected integration.<br><br>Clicking the Actions ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) icon will open a context menu with a set of functions for managing integrations. The Actions sub-menu functions will depend on the type of integration you were working on.<br><br>For more information, see [Managing integrations via Actions](#). |

## Manage repositories page

The Manage repositories page displays connected git repositories in Jira. All integration repositories are displayed here.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024455/gitcloud-managed-ui-git-repo-list.png?version=1&modificationDate=1648189296736&cacheVersion=1&api=v2)

|     |     |
| --- | --- |
| **Column** | **Description** |
| **Repository** | Displays the repository display name or repository URL.<br><br>Click the repository name on the list to open the repository settings for the selected repository. |
| **Integration** | This column displays the name of the git host service the repository belongs to. |
| **Status** | Shows the index status of the integration.<br><br>*   It shows INDEXED if _Repository Root_ is configured correctly and the Jira instance can access it.<br>    <br>*   It shows RUNNING during reindexing of the connected integration.<br>    <br>*   A similar ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) icon appears before the status indicator to indicate that it is being queued for indexing.<br>    <br>*   It shows ERROR if the connected integration has connection issues with the configured git host service. |
| **Last indexed** | Shows the date and time the indexing service has checked if the repository should be examined for changes.<br><br>For more information on Jira Cloud indexer, see [Jira Cloud: Classic indexing Explainer](#). |
| **Branch,**  <br>**Commits,**  <br>**Pull/merge request** | The counters for the number of branches, commits and pull/merge requests are displayed for the connected repository, respectively. |
| **Features** | ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) – The repository has a project association (solid) or not (hollow).<br><br>![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) – The repository has smart commits enabled (solid) or disabled (hollow).<br><br>![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) – The repository has enabled indexing triggers (solid) or not (hollow). |
| **Actions** | To the right of the **Features** column are actions that can be performed for the selected connected repository.<br><br>Clicking the Actions ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) icon will open a context menu with a set of functions for managing repositories. The Actions sub-menu functions will depend on the connection type of the repository you were working on.<br><br>For more information, see [Managing integrations via Actions](#). |

## Introduction to Action commands

Manage connected integration or repositories via the ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Actions** commands on the git configuration page. To learn more about these functions, proceed to the next page.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024455/gitcloud-managed-ui-manage-integrations-actions-sel.png?version=1&modificationDate=1648187125452&cacheVersion=1&api=v2)

##

[« Self-signed HTTPS integration](/wiki/spaces/GITCLOUD/pages/1923024386/Self-signed+HTTPS+integration)

[Managing integration via Actions »](/wiki/spaces/GITCLOUD/pages/1923024517)

### More topics about managing repository/integration configuration

*   Page:

    [Managing integration or repository configuration](/wiki/spaces/GITCLOUD/pages/1923024455/Managing+integration+or+repository+configuration) (Git Integration for Jira Cloud)

*   Page:

    [Managing integrations via Actions (Jira Cloud)](/wiki/spaces/GITCLOUD/pages/1923024517) (Git Integration for Jira Cloud)

*   Page:

    [Edit integration](/git-integration-for-jira-cloud/Edit-integration) (Git Integration for Jira Cloud)

*   Page:

    [SSL Verify](/git-integration-for-jira-cloud/SSL-Verify) (Git Integration for Jira Cloud)

*   Page:

    [Viewing indexing properties (Jira Cloud)](/wiki/spaces/GITCLOUD/pages/1923024741) (Git Integration for Jira Cloud)

*   Page:

    [Removing integration or repository configuration](/wiki/spaces/GITCLOUD/pages/1923024762/Removing+integration+or+repository+configuration) (Git Integration for Jira Cloud)

*   Page:

    [Associating project permissions](/wiki/spaces/GITCLOUD/pages/1923024786/Associating+project+permissions) (Git Integration for Jira Cloud)

*   Page:

    [Edit repository](/git-integration-for-jira-cloud/Edit-repository) (Git Integration for Jira Cloud)

*   Page:

    [View repository indexing logs](/wiki/spaces/GITCLOUD/pages/2013626625/View+repository+indexing+logs) (Git Integration for Jira Cloud)