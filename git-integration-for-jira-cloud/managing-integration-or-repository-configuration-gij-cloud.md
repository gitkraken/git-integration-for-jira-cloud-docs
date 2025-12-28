---

title: Managing integration or repository configuration
description: How to manage Git integrations and repositories in Jira Cloud
taxonomy:
    category: git-integration-for-jira-cloud

---

After successfully integrating a git host service or connecting git repositories via Git Integration for Jira, you can modify integration or repository settings depending on the connection protocol.

## Getting Started

On the git integration configuration page, you can manage connected integrations by adding, editing, updating settings, or disconnecting integrations and repositories.

## Manage Integrations Page

The Manage integrations page allows administrators to integrate and manage supported git host services in Jira.

![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-list-2025.png)

<br>

| Column | Description |
| :--- | :--- |
| **Integration** | Displays the integration display name or URL.<br><br>Click the integration name to open the integration connection settings. |
| **Type** | Displays the type of integration for the connected git host service.<br><ul><li><b>Git service</b> – full feature integration</li><li><b>Webhook indexing</b> – limited integration via webhooks</li></ul> |
| **Status** | Shows the index status of the integration.<br><ul><li><b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>INDEXED</b> – Repository Root is configured correctly and the Jira instance can access it.</li><li><b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>RUNNING</b> – The connected integration is being reindexed.</li><li>A <img src='/wp-content/uploads/gij-clock-icon.png' height=14 width=13 /> icon before the status indicator means it is queued for indexing.</li><li><b style='background-color:#FFEBE6; padding:1px 5px; color:#C02909; border-radius:3px; margin: 0 5px; font-size: small;'>ERROR</b> – The connected integration has connection issues with the configured git host service.</li></ul> |
| **Last indexed** | Shows the date and time the indexing service last checked if the integration repositories should be examined for changes.<br><br>For more information, see [Jira Cloud: Classic indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud). |
| **Repositories** | Shows the number of repositories in the connected integration. |
| **Features** | <img src='/wp-content/uploads/features-indicator-proj-permissions.png' height=12 width=16 /> – The integration has a project association (solid) or not (hollow).<br><img src='/wp-content/uploads/features-indicator-smart-commits.png' height=16 width=16 /> – The integration has smart commits enabled (solid) or disabled (hollow).<br><img src='/wp-content/uploads/features-indicator-indexing.png' height=16 width=10 /> – The integration has indexing triggers enabled (solid) or not (hollow). |
| **Actions** | To the right of the **Features** column are actions for the selected integration.<br><br>Click the <img src='/wp-content/uploads/actions-icon.png' /> Actions icon to open a context menu with functions for managing integrations. The available functions depend on the integration type.<br><br>For more information, see [Managing integrations via Actions](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud). |

## Manage Repositories Page

The Manage repositories page displays connected git repositories in Jira. All integration repositories appear here.

![](/wp-content/uploads/gitcloud-managed-ui-git-repo-list.png)

<br>

| Column | Description |
| :--- | :--- |
| **Repository** | Displays the repository display name or URL.<br><br>Click the repository name to open the repository settings. |
| **Integration** | Displays the name of the git host service the repository belongs to. |
| **Status** | Shows the index status of the repository.<br><ul><li><b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>INDEXED</b> – Repository Root is configured correctly and the Jira instance can access it.</li><li><b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>RUNNING</b> – The connected repository is being reindexed.</li><li>A <img src='/wp-content/uploads/gij-clock-icon.png' height=14 width=13 /> icon before the status indicator means it is queued for indexing.</li><li><b style='background-color:#FFEBE6; padding:1px 5px; color:#C02909; border-radius:3px; margin: 0 5px; font-size: small;'>ERROR</b> – The repository has connection issues with the configured git host service.</li></ul> |
| **Last indexed** | Shows the date and time the indexing service last checked if the repository should be examined for changes.<br><br>For more information, see [Jira Cloud: Classic indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud). |
| **Branch,**  <br>**Commits,**  <br>**Pull/merge request** | The counters for branches, commits, and pull/merge requests for the connected repository. |
| **Features** | <img src='/wp-content/uploads/features-indicator-proj-permissions.png' height=12 width=16 /> – The repository has a project association (solid) or not (hollow).<br><img src='/wp-content/uploads/features-indicator-smart-commits.png' height=16 width=16 /> – The repository has smart commits enabled (solid) or disabled (hollow).<br><img src='/wp-content/uploads/features-indicator-indexing.png' height=16 width=10 /> – The repository has indexing triggers enabled (solid) or not (hollow). |
| **Actions** | To the right of the **Features** column are actions for the selected repository.<br><br>Click the <img src='/wp-content/uploads/actions-icon.png' /> Actions icon to open a context menu with functions for managing repositories. The available functions depend on the repository connection type.<br><br>For more information, see [Managing integrations via Actions](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud). |

## Introduction to Action Commands

Manage connected integrations or repositories using the <img src='/wp-content/uploads/actions-icon.png' /> **Actions** commands on the git configuration page. To learn more about these functions, proceed to the next page.

![](/wp-content/uploads/gij-gitcloud-managed-ui-manage-integrations-actions-sel-2025.png)

&nbsp;
* * *

[**Prev:** Self-signed HTTPS integration](/git-integration-for-jira-cloud/self-signed-https-integration-gij-cloud/)

[**Next:** Managing integrations via Actions (Jira Cloud)](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud/)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
