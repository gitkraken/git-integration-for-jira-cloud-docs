---

title: Classic Indexing Explainer
description: Learn how Git Integration for Jira Cloud indexes commits, branches, tags, and pull requests using classic indexing.
taxonomy:
    category: git-integration-for-jira-cloud

---

**What's on this page:**
- [How is git data indexed?](#how-is-git-data-indexed)
- [Automatic indexing](#automatic-indexing)
  - [Indexing repositories](#indexing-repositories)
  - [Indexing integrations](#indexing-integrations)
  - [Triggering automatic reindexes via webhooks](#triggering-automatic-reindexes-via-webhooks)
  - [Automatic indexing period limits](#automatic-indexing-period-limits)
- [Manual indexing](#manual-indexing)
  - [Reindex all](#reindex-all)
  - [Repositories](#repositories)
  - [Integrations](#integrations)
  - [Indexing statuses](#indexing-statuses)
- [Indexing definitions](#indexing-definitions)
  - [Definitions](#definitions)
  - [Indexing errors](#indexing-errors)
- [Branch and pull/merge request name index triggers](#branch-and-pullmerge-request-name-index-triggers)

&nbsp;
* * *
&nbsp;

The [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud) app automatically indexes commits, branches, tags, and pull/merge requests. Previously, the system updated all repositories and integrations on a strict schedule – approximately every 8 minutes after the last indexing process finished for an account. This worked for small accounts and provided consistency but was inefficient for large accounts with repositories that rarely change.

Starting on October 28, 2019, the system calculates indexing based on per-repository activity. The overall goals are to reduce the strain on git services and make the indexing service more available for webhook triggers.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Note</b><br>
        The system only indexes pull/merge requests for repositories connected using the Full feature integrations panel in <b>Manage Git Repositories</b>. You can access them via the Jira Developer Panel on the right sidebar of a Jira issue. Git repositories added individually via SSH or HTTPS credentials do not show pull/merge requests.
    </div>
    </div>
</div>

&nbsp;

## How is git data indexed?

Git Integration for Jira Cloud indexes a variety of Git and Git-related data once a Jira administrator connects it. The table below describes how the system accesses each data type. All data remains stored until a Jira administrator removes the integration or the subscription is cancelled or expires.

See our [Privacy Policy](https://www.gitkraken.com/privacy-gij) and [Data Deletion Policy](https://bigbrassband.com/security-and-trust.html).

| Data Type | Method |
| :--- | :--- |
| Commits | Git clone |
| Branches | Git clone |
| Tags | Git clone |
| Pull requests | API |
| Merge requests | API |
| List of repositories | API |

&nbsp;

## Automatic indexing

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The system does not run indexing on disabled integrations/repositories.
    </div>
    </div>
</div>

### Indexing repositories

An internal process runs approximately every 8 minutes to review repositories eligible for change checking. The system checks all repositories for changes at least once daily. A repository change (commit, branch, tag) causes the system to calculate the _Next repository check_ as: a quarter of the time since the last repository update was detected.

For example, if the last commit was detected 4 hours ago, the system schedules the _Next repository check_ in 1 hour.

The system recalculates _Next repository check_ times on each indexer check.

### Indexing integrations

An internal process runs approximately every 8 minutes to review integrations eligible for change checking. The system checks integrations (for example, GitLab, GitHub, etc) during each _Next indexer check_ via the git service's API for available repositories.

The system checks all repositories for changes at least once daily. A repository change (commit, branch, tag) causes the system to calculate the _Next repository check_ as: a quarter of the time since the last repository update was detected.

For example, if the last commit was detected 4 hours ago, the system schedules the _Next repository check_ in 1 hour.

The system recalculates _Next repository check_ times on each indexer check.

### Triggering automatic reindexes via webhooks

Automatic indexing records changes in a timely manner for all types of repositories, but ideally, changes should be indexed immediately. Configure webhooks to trigger automatic reindexing for immediate reindex times.

When the indexing service receives webhooks, it reduces automatic indexing to once hourly.

For more information on configuring webhooks, see: [Indexing triggers](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud).

### Automatic indexing period limits

The table below describes the automatic indexing period limits:

| Action | Conditions | Min. period | Max. period |
| :--- | :--- | :--- | :--- |
| Check a repository | No webhook (PR or push) arrives for the repository | 450 secs | 24 hr |
| Check a repository | Webhooks (PR or push) arrives for the repository | 1 hr | 24 hr |
| Check an integration | Regardless of arriving webhooks | 19.2 hrs | 24 hr |

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If a user or webhook requests indexing, the system executes it immediately – regardless of any skipping settings.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        There can be an additional delay with repository indexer checking due to fetch delay.
    </div>
    </div>
</div>
<br>

## Manual indexing

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The system does not run indexing on disabled integrations/repositories.
    </div>
    </div>
</div>

### Reindex all

You can update all repositories and integrations manually via the Manage Git repositories screen by selecting the **Reindex All** button:

![Git Cloud manage git repositories page highlighting Reindex All](/wp-content/uploads/gij-gitcloud-gitmgr-reindex-integration-02-2025.png)

<br>

### Repositories

You can update repositories manually via the Manage git repositories screen by opening the <img src='/wp-content/uploads/actions-icon.png' /> Actions menu and selecting **Reindex repository**:

![Git Cloud manage git repositories page highlighting Reindex repository action](/wp-content/uploads/gij-gitcloud-gitmgr-actions-reindex-repo-2025.png)

<br>

### Integrations

You can update integrations manually via the Manage git repositories screen by opening the <img src='/wp-content/uploads/actions-icon.png' /> Actions menu and selecting **Reindex integration**:

![Git Cloud manage git repositories page highlighting Reindex integration action](/wp-content/uploads/gij-gitcloud-gitmgr-reindex-integration-01-2025.png)

<br>

### Indexing statuses

| Status | Description |
| :--- | :--- |
| <b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>INDEXED</b> | The integration or repository has been indexed and no errors were detected. |
| <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>QUEUED</b> | The integration or repository is actively queued for indexing. |
| <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>INDEXING</b> | The indexer is actively checking the integration or repository for changes. |
| <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>ERROR</b> | The integration has at least one repository in an error state (and not updating) and at least one repository was successfully updated. |
| <b style='background-color:#FFEBE6; padding:1px 5px; color:#C02909; border-radius:3px; margin: 0 5px; font-size: small;'>ERROR</b> | The integration or all repositories are in an error state and are not updating. |

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The upper limit of the indexer checking frequency is daily (24 hours / 86400 seconds). The integration and repository indexer checking upper limit follows the same value.
    </div>
    </div>
</div>
<br>

### Indexing errors

![Git commits tab in Jira issue showing indexing error messages](/wp-content/uploads/gij-gitcloud-git-commits-tab-indexing-error-msgs.png)

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Indexing Errors</b><br>
        A notification about indexing errors appears in the Git Commits tab so Jira administrators receive immediate alerts.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If you still have a question, reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'><b>Support Desk</b></a> or email us at <a href='mailto:support@gitkraken.com'>support@gitkraken.com</a>.
    </div>
    </div>
</div>
<br>

## Branch and pull/merge request name index triggers

Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.

<kbd>Last updated: December 2025</kbd>
