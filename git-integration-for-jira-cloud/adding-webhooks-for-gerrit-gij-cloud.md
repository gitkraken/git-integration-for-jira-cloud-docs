---
title: "Adding webhooks for Gerrit"
description: "Configure webhooks for Gerrit repositories in Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Adding webhooks for Gerrit"
content_type: "install"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["Gerrit"]
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "install", "admin", "Gerrit"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Gerrit does not include webhook support by default, so Git Integration for Jira Cloud requires the Gerrit webhook plugin before Gerrit can send indexing updates. Use this page when a Gerrit repository is already connected and you need plugin-based webhook delivery or a manual trigger workflow.

| Gerrit webhook setup choice | Use when | Required component | Notes |
| :--- | :--- | :--- | :--- |
| Gerrit webhook plugin | You want Gerrit to send webhook events automatically | Gerrit `webhooks` plugin | Required before standard webhook setup works |
| Remote webhook configuration | You want a Gerrit project to send webhooks to Jira Cloud | Gerrit remote configuration plus Jira webhook URL | Uses the URL from Git Integration for Jira indexing triggers |
| Manual webhook trigger | You need a custom or CI-driven push notification | HTTP request with Gerrit-specific headers | Useful for individual repositories or automation workflows |

**On this page:**
- [Install the webhook plugin](#install-the-webhook-plugin)
- [Configure webhooks](#configure-webhooks)
- [Trigger webhooks manually](#trigger-webhooks-manually)

&nbsp;
* * *
&nbsp;

## How to install the Gerrit webhook plugin

Install Gerrit with the webhook plugin from [https://gerrit.googlesource.com/plugins/webhooks/](https://gerrit.googlesource.com/plugins/webhooks/).

&nbsp;

## How to configure Gerrit webhooks

### List Projects (Repositories)

```powershell
curl http(s)://your.org.com:8080/projects/?d
```

### Check Enabled Webhooks

```powershell
curl http(s)://your.org.com:8080/config/server/webhooks~projects/MyTestRepo/remotes
```

### Add a Webhook

```powershell
curl --user username:password -H 'Content-Type: application/json' -X PUT -d @webhook.json http(s)://your.org.com:8080/a/config/server/webhooks~projects/MyTestRepo/remotes/bbb-webhook
```

Create a `webhook.json` file:

```json
{
   "url" : "https://example.com/webhook/url",
   "maxTries" : 3,
   "sslVerify": true
}
```

Replace `https://example.com/webhook/url` with your webhook URL from Git Integration for Jira ➜ **Indexing triggers**.

&nbsp;

## How to trigger Gerrit webhooks manually

Create a webhook trigger for individual repositories. Use this with continuous integration services.

### Required Headers

| Header | Value |
|--------|-------|
| `x-bbb-webhook-type` | `PUSH` |
| `Content-Type` | `application/json` |

### Optional Headers

| Header | Description |
|--------|-------------|
| `x-bbb-webhook-id` | Any string representing the request ID |

### Examples

**Basic request:**

```powershell
curl -H 'x-bbb-webhook-type: push' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url
```

**Request with ID:**

```powershell
curl -H 'x-bbb-webhook-type: push' -H 'x-bbb-webhook-id: id-string' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url
```

### Payload Format

Create a `payload.json` file:

```json
{  
    "origin": "repository-origin"
}
```

Replace `repository-origin` with your repository's origin URL.

