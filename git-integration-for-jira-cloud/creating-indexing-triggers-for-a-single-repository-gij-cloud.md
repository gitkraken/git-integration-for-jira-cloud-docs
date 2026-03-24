---
title: "Creating indexing triggers for a single repository"
description: "Create indexing triggers for individual repositories using webhooks with Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Creating indexing triggers for a single repository"
content_type: "integration"
audience: "all"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "all"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "integration"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Create an indexing trigger for any individual repository. Use this with continuous integration services to trigger immediate reindexing when you need a repository-level webhook call instead of an install-level or integration-level trigger.

| Trigger level | Use when | Scope | Notes |
| :--- | :--- | :--- | :--- |
| Install-level trigger | You want one webhook URL for all configured repositories | Whole install | Simplest global setup |
| Integration-level trigger | You want one webhook URL per integration | One integration | Useful when integrations should be separated |
| Repository-level trigger | You want one webhook URL for a specific repository | Single repository | Best for CI jobs or narrowly scoped automation |

## Which headers are required for a single-repository indexing trigger

| Header | Value |
|--------|-------|
| `x-bbb-webhook-type` | `push` |
| `Content-Type` | `application/json` |

## Which headers are optional for a single-repository indexing trigger

| Header | Description |
|--------|-------------|
| `x-bbb-webhook-id` | Any string representing the request ID |

&nbsp;

## How to call a single-repository indexing trigger

**Basic request:**

```powershell
curl -H 'x-bbb-webhook-type: push' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url
```

**Request with custom ID:**

```powershell
curl -H 'x-bbb-webhook-type: push' -H 'x-bbb-webhook-id: id-string' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url
```

&nbsp;

## What payload format the single-repository trigger expects

Create a `payload.json` file with the repository origin:

```json
{
    "origin": "repository-origin"
}
```

