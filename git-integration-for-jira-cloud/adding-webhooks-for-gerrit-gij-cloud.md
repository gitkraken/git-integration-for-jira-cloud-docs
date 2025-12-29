---
title: Adding webhooks for Gerrit
description: Configure webhooks for Gerrit repositories in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

Webhooks are not built into Gerrit by default. You must install and configure the Gerrit webhook plugin before using webhooks with Git Integration for Jira Cloud.

**On this page:**
- [Install the webhook plugin](#install-the-webhook-plugin)
- [Configure webhooks](#configure-webhooks)
- [Trigger webhooks manually](#trigger-webhooks-manually)

&nbsp;
* * *
&nbsp;

## Install the Webhook Plugin

Install Gerrit with the webhook plugin from [https://gerrit.googlesource.com/plugins/webhooks/](https://gerrit.googlesource.com/plugins/webhooks/).

&nbsp;

## Configure Webhooks

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

## Trigger Webhooks Manually

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

<kbd>Last updated: December 2025</kbd>
