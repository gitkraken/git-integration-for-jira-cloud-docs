---
title: "Indexing triggers (formerly Webhooks)"
description: "How to configure indexing triggers for faster repository updates in Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Indexing triggers (formerly Webhooks)"
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

Indexing triggers enable immediate reindexing of your repositories from remote systems. When your git data changes, triggers send near real-time data to Jira, eliminating the wait for the regular 5-minute polling interval.

| Trigger option | Use when | Scope | Notes |
| :--- | :--- | :--- | :--- |
| Install-level trigger URL | You want one webhook URL for all configured repositories | Whole install | Simplest legacy trigger setup |
| Detailed indexing triggers guide | You need the current, fuller trigger model | Install, integration, or repository level | Prefer the main indexing triggers guide for newer workflows |
| Single-repository trigger | You need a narrowly scoped webhook endpoint | Single repository | Better for CI or repository-specific automation |

Most git providers also support account-level or organization-level webhooks. For details, see [About GitLab Webhooks](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/web_hooks/web_hooks.md).

**On this page:**
- [Enable indexing triggers](#enable-indexing-triggers)
- [Configure the webhook URL](#configure-the-webhook-url)

&nbsp;
* * *
&nbsp;

## How to enable indexing triggers in the legacy webhooks flow

1. From your Jira dashboard, go to **Apps** ➜ **Git Integration: Manage Git repositories**.

2. Click **Indexing triggers** in the sidebar.

    ![](/wp-content/uploads/gij-gitcloud-indexing-triggers-loc-new.png)

3. Set **Indexing triggers enabled** to **ON**.

    ![](/wp-content/uploads/gij-gitcloud-indexing-triggers-enable.png)

&nbsp;

## How to use the legacy webhook URL format

Use the **Webhook URL** displayed on the Indexing triggers page to configure webhooks on your remote git host.

The **Secret Key** is a secure, randomly-generated alphanumeric string created when you install Git Integration for Jira. You can generate a new secret token according to your git host's requirements.

**URL format:**

```
<JIRA_BASE_URL>/git/webhook/reindex/<SECRET_KEY>
```

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Activating this URL through <code>GET</code>, <code>POST</code>, or <code>PUT</code> triggers reindexing of all repositories when webhooks are enabled.
        <p style='margin-bottom:-10px'><code>DELETE</code> and <code>HEAD</code> methods are not supported.</p>
    </div>
    </div>
</div>

&nbsp;

## Related indexing trigger guides

- [Detailed indexing triggers guide](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud)
- [Create reindex triggers for a single repository](/git-integration-for-jira-cloud/creating-indexing-triggers-for-a-single-repository-gij-cloud)

&nbsp;
* * *

[**Prev:** Reindexing](/git-integration-for-jira-cloud/reindexing-gij-cloud/)

[**Next:** Localization support](/git-integration-for-jira-cloud/localization-support-gij-cloud/)

<p>&nbsp;</p>

