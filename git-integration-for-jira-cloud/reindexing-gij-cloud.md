---

title: Reindexing
description: How to manually reindex repositories in Git Integration for Jira Cloud
taxonomy:
    category: git-integration-for-jira-cloud

---

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

&nbsp;

## Getting Started

Synchronization between the repository and app starts automatically. However, reindexing may be required to manually start the synchronization process.

There are two ways to do this:

### Method 1

![](/wp-content/uploads/gij-gitcloud-gitmgr-reindex-integration-02.png)

1.  To start an update of all or multiple selected repositories, go to the Manage integrations page and use the checkboxes on the left of the list to mark integrations for reindex.

2.  With the selected integrations, click ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Reindex selected**. Once synchronization starts, the progress displays on this tab.

### Method 2

![](/wp-content/uploads/gij-gitcloud-gitmgr-reindex-integration-01.png)

If a specific repository or integration needs to be synchronized, click ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Reindex integration**.

Git log entries may not immediately appear when you open the <i><b>Git Commits</b></i> tab right after app installation. Wait until the revision indexer job completes the initial synchronization.

&nbsp;

## Indexing Explainer for Jira Cloud

Git Integration for Jira Cloud automatically indexes commits, branches, tags, and pull/merge requests.

Starting October 28, 2019, indexing is calculated based on per-repository activity. The overall goals are to reduce the strain on git services and make the indexing service more available for webhook triggers.

For detailed information on this Jira Cloud feature, see [Feature: Classic Indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud).

&nbsp;

## Indexing Errors

The indexer shows an error message on the Jira issue ➜ Git Commits tab if indexing issues are found.

<img src='/wp-content/uploads/gij-git-cloud-indexing-error-sample.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;
* * *

[**Prev:** Jira project page](/git-integration-for-jira-cloud/jira-project-page-gij-cloud/)

[**Next:** Indexing triggers (formerly Webhooks)](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
