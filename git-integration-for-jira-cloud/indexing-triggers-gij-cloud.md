---
title: Indexing Triggers
description: Configure indexing triggers (webhooks) to enable real-time repository updates in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

**On this page:**
- [Understand indexing triggers](#understand-indexing-triggers)
- [Enable indexing triggers](#enable-indexing-triggers)
- [Find the webhook URL](#find-the-webhook-url)
- [Choose a webhook URL level](#choose-a-webhook-url-level)

&nbsp;
* * *
&nbsp;

## Understand Indexing Triggers

Indexing triggers (webhooks) activate immediate reindexing of your repositories from remote systems. Your git server sends near real-time data to Jira when git data changes, providing much faster updates than the default 5-minute polling interval.

### Common trigger events

Configure webhooks to execute when:

- A new commit is pushed
- A pull request is opened
- A branch is merged

You can create indexing triggers for individual repositories, and most git providers support account-level or organization-level webhooks.

### Why use indexing triggers?

Without indexing triggers, Jira relies on default polling (usually 5 minutes). Users must wait for the next interval to see new commits or pull requests. With indexing triggers, Jira receives updates immediately.

&nbsp;

## Enable Indexing Triggers

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        You must enable indexing triggers before using this feature.
    </div>
    </div>
</div>

1. From your Jira Cloud dashboard, go to **Apps** ➜ **Git Integration: Repository browser**.

2. Click **Indexing triggers** in the sidebar.

    ![](/wp-content/uploads/gij-gitcloud-new-webhooks-settings-page-c-2025.png)

3. Click the **Indexing triggers enabled** toggle to enable or disable the feature.

&nbsp;

## Find the Webhook URL

Access the webhook URL from these locations:

### From the Indexing Triggers Page

Go to **Apps** ➜ **Git Integration for Jira** ➜ **Settings** ➜ **Indexing triggers**.

![](/wp-content/uploads/gij-gitcloud-indexing-triggers-loc-01c-2025.png)

### From the Repository List

1. Go to the **Manage repository** page.
2. Click a repository or integration.
3. Find the **Webhook URL** field.

![](/wp-content/uploads/gij-git-cloud-webhook-url-repo-list-loc-c.-01-2025.png)

![](/wp-content/uploads/gij-git-cloud-webhook-url-repo-list-loc-c.-02-2025.png)

### From Repository Settings

1. Go to the git configuration page.
2. Click ![](/wp-content/uploads/actions-icon.png) **Actions** ➜ **Show integration repositories**.

![](/wp-content/uploads/gij-git-cloud-webhook-url-repo-cfg-tracked-repos-c-2025.png)

![](/wp-content/uploads/gij-jira-cloud-repo-cfg-view-tracked-repo-dlg-c-2025.png)

### URL format

```
https://[your-cloud-domain-url]/api/1/webhook/reindex/install/<INSTANCE_ID>/<SECRET_KEY>
```

**Example:**

```
https://gitforjiracloud.bigbrassband.com/api/1/webhook/reindex/install/x5chdqpqln0j04xcgv02zy7h9/vfTmXtqIFyqeCYYS3WjLIn2RRz5rHSDO
```

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Click the copy icon next to the Webhook URL to copy it to your clipboard.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Supported HTTP methods:</b> <code>GET</code>, <code>POST</code>, <code>PUT</code><br>
        <b>Not supported:</b> <code>DELETE</code>, <code>HEAD</code>
    </div>
    </div>
</div>

&nbsp;

## Choose a Webhook URL Level

Three webhook URL levels are available:

| Level | Scope | Use Case |
|-------|-------|----------|
| Install level | All configured repositories | Simplest setup; recommended for most users |
| Integration level | Repositories within one integration | When you need separate triggers per integration |
| Repository level | Single repository only | Granular control for specific repositories |

### Install Level (Recommended)

This default webhook URL triggers events for all configured repositories. It's the easiest to configure.

**Access location:** Git Integration sidebar ➜ **Indexing triggers**

![](/wp-content/uploads/gij-gitcloud-indexing-triggers-loc-01c-2025.png)

### Integration Level

This webhook URL triggers events only for repositories within a specific integration.

**Access location:** Manage integrations page ➜ ![](/wp-content/uploads/actions-icon.png) **Actions** ➜ **Edit integration** ➜ **Feature Settings**

![](/wp-content/uploads/gij-gitcloud-indexing-trigger-webhook-url-level-1-2025.png)

Or: Manage integrations page ➜ click an integration ➜ **Feature Settings**

![](/wp-content/uploads/gij-gitcloud-indexing-triggers-integration-level-02-2025.png)

### Repository Level

This webhook URL triggers events only for a single repository.

**Access location:** Manage repository page ➜ click a repository ➜ **Webhook URL** field

![](/wp-content/uploads/gij-git-cloud-webhook-url-repo-list-loc-c.-01-2025.png)

![](/wp-content/uploads/gij-git-cloud-webhook-url-repo-list-loc-c.-02-2025.png)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Repository IDs are extracted from all webhook types (including install level). Only repositories specified in the webhook are indexed, preventing unnecessary indexing of all repositories in large integrations.
    </div>
    </div>
</div>

<kbd>Last updated: December 2025</kbd>
