---
title: Creating indexing triggers for a single repository
description: Create indexing triggers for individual repositories using webhooks with Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

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

<kbd>Last updated: December 2025</kbd>
