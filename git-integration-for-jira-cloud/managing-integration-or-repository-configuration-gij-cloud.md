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

<br>

| Column | Description |
| :--- | :--- |
| **Integration** | Displays the integration display name or integration URL.<br><br>Click the integration name on the list to open the integration connection settings for the selected integration. |
| **Type** | Displays the type of integration for the connected git host service.<br><ul><li><b>Git service</b> – full feature integration</li><li><b>Webhook indexing</b> – limited integration via webhooks</li></ul> |
| **Status** | Shows the index status of the integration.<br><ul><li>It shows <b>INDEXED</b> if <i>Repository Root</i> is configured correctly and the Jira instance can access it.</li><li>It shows <b style='color: #FDDB53'>RUNNING</b> during reindexing of the connected integration.</li><li>A similar icon appears before the status indicator to indicate that it is being queued for indexing.</li><li>It shows <b style='color: #FF7A7A'>ERROR</b> if the connected integration has connection issues with the configured git host service.</li></ul> |
| **Last indexed** | Shows the date and time the indexing service has checked if the integration repositories should be examined for changes.<br><br>For more information on Jira Cloud indexer, see [Jira Cloud: Classic indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud). |
| **Repositories** | Shows the counter for the number of repositories the connected integration has. |
| **Features** | <img src='/wp-content/uploads/features-indicator-proj-permissions.png' height=12 width=16 /> - The integration has a project association (solid) or not (hollow).<br><img src='/wp-content/uploads/features-indicator-smart-commits.png' height=16 width=16 /> - The integration has smart commits enabled (solid) or disabled (hollow).<br><img src='/wp-content/uploads/features-indicator-indexing.png' height=16 width=10 /> - The integration has enabled indexing triggers (solid) or not (hollow). |
| **Actions** | To the right of the **Features** column are actions that can be performed for the selected connected integration.<br><br>Clicking the &nbsp;<img src='/wp-content/uploads/actions-icon.png' /> Actions icon will open a context menu with a set of functions for managing integrations. The Actions sub-menu functions will depend on the type of integration you were working on.<br><br>For more information, see [Managing integrations via Actions](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud). |

## Manage repositories page

The Manage repositories page displays connected git repositories in Jira. All integration repositories are displayed here.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024455/gitcloud-managed-ui-git-repo-list.png?version=1&modificationDate=1648189296736&cacheVersion=1&api=v2)

<br>

| Column | Description |
| :--- | :--- |
| **Repository** | Displays the repository display name or repository URL.<br><br>Click the repository name on the list to open the repository settings for the selected repository. |
| **Integration** | This column displays the name of the git host service the repository belongs to. |
| **Status** | Shows the index status of the integration.<br><ul><li>It shows <b>INDEXED</b> if <i>Repository Root</i> is configured correctly and the Jira instance can access it.</li><li>It shows <b style='color: #FDDB53'>RUNNING</b> during reindexing of the connected integration.</li><li>A similar icon appears before the status indicator to indicate that it is being queued for indexing.</li><li>It shows <b style='color: #FF7A7A'>ERROR</b> if the connected integration has connection issues with the configured git host service.</li></ul> |
| **Last indexed** | Shows the date and time the indexing service has checked if the repository should be examined for changes.<br><br>For more information on Jira Cloud indexer, see [Jira Cloud: Classic indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud). |
| **Branch,**  <br>**Commits,**  <br>**Pull/merge request** | The counters for the number of branches, commits and pull/merge requests are displayed for the connected repository, respectively. |
| **Features** | <img src='/wp-content/uploads/features-indicator-proj-permissions.png' height=12 width=16 /> – The repository has a project association (solid) or not (hollow).<br><img src='/wp-content/uploads/features-indicator-smart-commits.png' height=16 width=16 /> – The repository has smart commits enabled (solid) or disabled (hollow).<br><img src='/wp-content/uploads/features-indicator-indexing.png' height=16 width=10 /> – The repository has enabled indexing triggers (solid) or not (hollow). |
| **Actions** | To the right of the **Features** column are actions that can be performed for the selected connected repository.<br><br>Clicking the &nbsp;<img src='/wp-content/uploads/actions-icon.png' /> Actions icon will open a context menu with a set of functions for managing repositories. The Actions sub-menu functions will depend on the connection type of the repository you were working on.<br><br>For more information, see [Managing integrations via Actions](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud). |

## Introduction to Action commands

Manage connected integration or repositories via the &nbsp;<img src='/wp-content/uploads/actions-icon.png' /> **Actions** commands on the git configuration page. To learn more about these functions, proceed to the next page.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024455/gitcloud-managed-ui-manage-integrations-actions-sel.png?version=1&modificationDate=1648187125452&cacheVersion=1&api=v2)

