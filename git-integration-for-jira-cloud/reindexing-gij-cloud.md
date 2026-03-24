---
title: "Reindexing"
description: "How to manually reindex repositories in Git Integration for Jira Cloud"
product: "Git Integration for Jira Cloud"
feature: "Reindexing"
content_type: "install"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "install", "admin"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Git Integration for Jira Cloud reindexes repositories to refresh commits, branches, tags, and pull or merge request data when automatic synchronization is not enough. Use this page when you need to manually force synchronization; use indexing triggers instead when you want near-real-time updates after repository activity.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        You must be a member of the <b>jira-developers</b> <i>group</i> to start reindex.
    </div>
    </div>
</div>

| Reindex option | Use when | Scope | Notes |
| :--- | :--- | :--- | :--- |
| Reindex selected | You need to refresh multiple integrations or repositories at once | Multiple selected items | Use the Manage integrations list and bulk actions |
| Reindex integration | You need to refresh one specific integration or repository | Single integration or repository | Best for targeted manual synchronization |
| Indexing triggers | You want updates after repository activity without manual action | Existing integrations | Better for ongoing near-real-time updates |

&nbsp;

## How to start manual reindexing

Synchronization between the repository and app starts automatically. However, reindexing may be required to manually start the synchronization process.

There are two ways to do this:

### How to reindex selected integrations or repositories

![](/wp-content/uploads/gij-gitcloud-gitmgr-reindex-integration-02.png)

1.  To start an update of all or multiple selected repositories, go to the Manage integrations page and use the checkboxes on the left of the list to mark integrations for reindex.

2.  With the selected integrations, click ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Reindex selected**. Once synchronization starts, the progress displays on this tab.

### How to reindex one specific integration

![](/wp-content/uploads/gij-gitcloud-gitmgr-reindex-integration-01.png)

If a specific repository or integration needs to be synchronized, click ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Reindex integration**.

Git log entries may not immediately appear when you open the <i><b>Git Commits</b></i> tab right after app installation. Wait until the revision indexer job completes the initial synchronization.

&nbsp;

## How reindexing works in Jira Cloud

Git Integration for Jira Cloud automatically indexes commits, branches, tags, and pull/merge requests.

Starting October 28, 2019, indexing is calculated based on per-repository activity. The overall goals are to reduce the strain on git services and make the indexing service more available for webhook triggers.

For detailed information on this Jira Cloud feature, see [Feature: Classic Indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud).

&nbsp;

## How to identify indexing errors

The indexer shows an error message on the Jira issue ➜ Git Commits tab if indexing issues are found.

<img src='/wp-content/uploads/gij-git-cloud-indexing-error-sample.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;
* * *

[**Prev:** Jira project page](/git-integration-for-jira-cloud/jira-project-page-gij-cloud/)

[**Next:** Indexing triggers (formerly Webhooks)](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud)

<p>&nbsp;</p>

