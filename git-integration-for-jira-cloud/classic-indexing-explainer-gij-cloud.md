---

title: Classic Indexing Explainer
description:
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

* * *

The [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/4984) app automatically indexes commits, branches, tags, and pull/merge requests. Previously, all repositories and integrations were updated on a strict schedule – which is approximately every 8 minutes after the last indexing process has finished for an account. This worked for small accounts and provided consistency but was inefficient with large accounts (many with repositories that rarely change).

Starting on October 28, 2019, indexing is now calculated based on per repository activity. The overall goals are to reduce the strain on git services and make the indexing service more available for the webhook triggers.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Note</b><br>
        Pull/merge requests are only indexed for repositories connected using the Full feature integrations panel in <b>Manage Git Repositories</b>. They can be accessed via the Jira Developer Panel on the right sidebar of a Jira issue. Git repositories added individually via SSH or HTTPS credentials will not show pull/merge requests.
    </div>
    </div>
</div>
<br>

## How is git data indexed?

Git Integration for Jira Cloud indexes a variety of Git and Git related data once connected by a Jira administrator. The table below describes how each data type is accessed. All data is stored until a Jira administrator removes the integration or the subscription is cancelled or expires.

See our [Privacy Policy](https://www.gitkraken.com/privacy-gij) and [Data Deletion Policy](https://bigbrassband.com/security-and-trust.html).

| **Data Type** | **Method** |
| :--- | :--- |
| Commits | Git clone |
| Branches | Git clone |
| Tags | Git clone |
| Pull requests | API |
| Merge requests | API |
| List of repositories | API |

## Automatic indexing

### Indexing repositories

An internal process runs approximately every 8 minutes to review repositories eligible to be checked for changes. All repositories are checked for changes at least once daily. A repository change (commit, branch, tag) will cause the _Next repository check_ to be calculated next: in a quarter of the time since the last repository update was detected.

For example, if the last commit was detected 4 hours ago then the _Next repository check_ will be scheduled in 1 hour.

The time for _Next repository check_ are re-calculated on each indexer check.

### Indexing integrations

An internal process runs approximately every 8 minutes to review integrations eligible to be checked for changes. Integrations (for example, GitLab, GitHub, etc) are checked during each _Next indexer check_ via the git service's API for available repositories. 

All repositories are checked for changes at least once daily. A repository change (commit, branch, tag) will cause the _Next repository check_ to be calculated next: in a quarter of the time since the last repository update was detected.

For example, if the last commit was detected 4 hours ago then the _Next repository check_ will be scheduled in 1 hour.

_Next repository check_ times are re-calculated on each indexer check.

### Triggering automatic reindexes via webhooks

Automatic indexing is designed to record changes in a timely manner for all types of repositories, but ideally, changes should be indexed immediately. Configuring webhooks to trigger automatic reindexing will result in immediate reindex times.

When webhooks are received by the indexing service, the indexing service will reduce the automatic indexing to once - hourly.

For more information on configuring webhooks, see: [Indexing triggers](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud/).

### Automatic indexing period limits

The table below describes the automatic indexing period limits:

| **Action** | **Conditions** | **Min. period** | **Max. period** |
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
        If the indexing has been requested by a user or a webhook, it will be executed immediately – regardless of any skipping settings.
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

### Reindex all

All repositories and integrations can be updated manually via the Manage Git repositories screen by selecting the **Reindex All** button:

![Git Cloud manage git repositories page highlighting Reindex All](https://bigbrassband.atlassian.net/wiki/download/attachments/183369754/gitcloud-reindex-all-iex.png?version=1&modificationDate=1598591995427&cacheVersion=1&api=v2)

<br>

### Repositories

Repositories can be updated manually via the Manage git repositories screen by opening the <img src='/wp-content/uploads/actions-icon.png' valign=middle> Actions menu and selecting **Reindex repository**:

![Git Cloud manage git repositories page highlighting Reindex repository action](https://bigbrassband.atlassian.net/wiki/download/attachments/183369754/gitcloud-reindex-repo-iex.png?version=1&modificationDate=1598591995919&cacheVersion=1&api=v2)

<br>

### Integrations

Integrations can be updated manually via the Manage git repositories screen by opening the <img src='/wp-content/uploads/actions-icon.png' valign=middle> Actions menu and selecting **Reindex integration**:

![Git Cloud manage git repositories page highlighting Reindex integration action](https://bigbrassband.atlassian.net/wiki/download/attachments/183369754/gitcloud-reindex-integration-iex.png?version=1&modificationDate=1598591996399&cacheVersion=1&api=v2)

<br>

### Indexing statuses

| **Status** | **Description** |
| :--- | :--- |
| INDEXED | Integration or repository has been indexed and no errors were detected. |
| QUEUED | Integration or repository is actively queued for indexing. |
| INDEXING | Indexer is actively checking integration or repository for changes. |
| ERROR | Integration has at least one repository in an error state (and not updating) and at least one repository was successfully updated. |
| ERROR | Integration or all repositories are in an error state and are not updating. |

## Indexing definitions

The [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) app now has new indexing date/times to indicate the variety of repository checks:

![Show tracked repos action dialog showcasing indexing definitions](https://bigbrassband.atlassian.net/wiki/download/attachments/183369754/gitcloud-indexing-defs.png?version=1&modificationDate=1598591997067&cacheVersion=1&api=v2)

<br>

### Definitions

| **Information Label** | **Description** |
| :--- | :--- |
| _Last indexer check_ | Date and time the indexing service has checked if the repository should be examined for changes. |
| _Next indexer check_ | Date and time the indexing service will next check if the repository should be examined for changes (commits, tags, branches) |
| _Last repository check_ | Date and time the indexing service has last checked the repository for changes (commits, tags, branches) |
| _Last repository change_ | Date and time the indexing service last detected a change (commits, tags, branches) in the repository. This time is accurate only as of the release of the new indexing service on October 27, 2019 or when the repository was first integrated with Git Integration for Jira Cloud. |
| _Next repository check_ | Date and time the indexing service will check the repository for changes (commits, tags, branches). |
| _Commit webhooks detected_ | Indexing service has received a commit webhook trigger for this repository. Thus, automatic indexing for this repository is reduced to once daily. |
| _Last pull request check_ | Date and time the indexing service last checked the repository for pull request changes (new pull/merge requests or status changes). |
| _Last pull request change_ | Date and time the indexing service last detected a change (new pull/merge requests or status changes) in the repository. This time is accurate only as of the release of the new indexing service on October 27, 2019. |
| _Next pull request check_ | Date and time the indexing service will check repository for new pull/merge requests or status changes. |
| _Pull request webhooks detected_ | Indexing service has received a pull/merge request webhook trigger for this repository. Thus, automatic indexing for this repository is reduced to once hourly. |

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

![Git commits tab in Jira issue showing indexing error messages](https://bigbrassband.atlassian.net/wiki/download/attachments/183369754/image-20200828-050318.png?version=1&modificationDate=1598591997511&cacheVersion=1&api=v2)

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Indexing Errors</b><br>
        A notification about indexing error is displayed in the Git Commits tab so that Jira administrators can be alerted immediately.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If you still have a question – reach out to our <a href='https://bigbrassband.atlassian.net/servicedesk/customer/portals'><b>Support Desk</b> or email us at <a href='mailto:support@bigbrassband.com'>support@bigbrassband.com</a>.
    </div>
    </div>
</div>
<br>

## Branch and pull/merge request name index triggers

Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.

