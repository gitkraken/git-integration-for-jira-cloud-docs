---
title: Indexing triggers (formerly Webhooks)
description: How to configure indexing triggers for faster repository updates in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

Indexing triggers enable immediate reindexing of your repositories from remote systems. When your git data changes, triggers send near real-time data to Jira, eliminating the wait for the regular 5-minute polling interval.

Most git providers also support account-level or organization-level webhooks. For details, see [About GitLab Webhooks](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/web_hooks/web_hooks.md).

**On this page:**
- [Enable indexing triggers](#enable-indexing-triggers)
- [Configure the webhook URL](#configure-the-webhook-url)

&nbsp;
* * *
&nbsp;

## Enable Indexing Triggers

1. From your Jira dashboard, go to **Apps** ➜ **Git Integration: Manage Git repositories**.

2. Click **Indexing triggers** in the sidebar.

    ![](/wp-content/uploads/gij-gitcloud-indexing-triggers-loc-new.png)

3. Set **Indexing triggers enabled** to **ON**.

    ![](/wp-content/uploads/gij-gitcloud-indexing-triggers-enable.png)

&nbsp;

## Configure the Webhook URL

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

## More Information

- [Detailed indexing triggers guide](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud)
- [Create reindex triggers for a single repository](/git-integration-for-jira-cloud/creating-indexing-triggers-for-a-single-repository-gij-cloud)

&nbsp;
* * *

[**Prev:** Reindexing](/git-integration-for-jira-cloud/reindexing-gij-cloud/)

[**Next:** Localization support](/git-integration-for-jira-cloud/localization-support-gij-cloud/)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
