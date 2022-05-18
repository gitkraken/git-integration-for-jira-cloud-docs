---

title: Reindexing
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
**Permissions**
You must be a member of the **jira-developers** _group_ to start reindex.

Synchronization between the repository and app will start automatically. However, reindexing may be required to manually start the synchronization process.

## Getting started

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923026060/gitcloud-gitmgr-reindexing-sel.png?version=1&modificationDate=1636099148378&cacheVersion=1&api=v2)

There are two ways to do this:

*   To start update of all repositories, go to the **Git Integration for Jira** app git configuration page then click **Reindex All** button. Once synchronization is started, the progress will be displayed on this tab.

*   If a specific repository or integration needs to be synchronized, click the ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Actions** icon then **Reindex integration/repository**.


**Initial Synchronization**
Git log entries may not immediately appear when you open _**Git Commits**_ tab right after the app installation. You need to wait until the revision indexer job completes the initial synchronization.

## Indexing Explainer for Jira Cloud

The Git Integration for Jira Cloud app automatically indexes commits, branches, tags, and pull/merge requests.

Starting on October 28, 2019, indexing is now calculated based on per repository activity. The overall goals are to reduce the strain on git services and make the indexing service more available for the webhook triggers.

For detailed information on this Jira Cloud feature, see [Feature: Classic Indexing Explainer](/wiki/spaces/GITCLOUD/pages/183369754/Classic+Indexing+Explainer).

## Indexing errors

Indexer will show an error message on the Jira issue ➜ Git Commits tab if indexing issues are found.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923026060/git-cloud-indexing-error-sample.png?version=1&modificationDate=1630063694862&cacheVersion=1&api=v2&width=544&height=172)

[« Jira project page](/wiki/spaces/GITCLOUD/pages/1923026027/Jira+project+page)

[Indexing triggers (formerly Webhooks) »](/wiki/spaces/GITCLOUD/pages/1923026143)