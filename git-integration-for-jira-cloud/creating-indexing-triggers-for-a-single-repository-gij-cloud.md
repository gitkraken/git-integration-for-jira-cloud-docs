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

Create an indexing trigger for any individual repository. Use this with continuous integration services to trigger immediate reindexing.

## Required Headers

| Header | Value |
|--------|-------|
| `x-bbb-webhook-type` | `push` |
| `Content-Type` | `application/json` |

## Optional Headers

| Header | Description |
|--------|-------------|
| `x-bbb-webhook-id` | Any string representing the request ID |

&nbsp;

## Usage Examples

**Basic request:**

```powershell
curl -H 'x-bbb-webhook-type: push' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url
```

**Request with custom ID:**

```powershell
curl -H 'x-bbb-webhook-type: push' -H 'x-bbb-webhook-id: id-string' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url
```

&nbsp;

## Payload Format

Create a `payload.json` file with the repository origin:

```json
{
    "origin": "repository-origin"
}
```
