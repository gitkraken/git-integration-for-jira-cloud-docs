---
title: "How to Create Reindex Triggers for a Single Repository"
description: "Create webhook triggers to reindex a single repository in Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "How to Create Reindex Triggers for a Single Repository"
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

Create a webhook that triggers reindexing for a specific repository by following these requirements.

| Requirement | Why it matters | Example |
| :--- | :--- | :--- |
| Matching `git_http_url` | Jira matches the request to the correct repository origin | `https://gitlab.com/your-org/your-repo.git` |
| `Content-Type: application/json` | Jira expects a JSON request body | `application/json` |
| Correct webhook secret | Jira validates the request against the configured secret | Secret from the webhooks section |

## What a single-repository reindex trigger requires

Your webhook must meet these criteria:

1. The **`git_http_url`** in the request body must match the **Repository Origin** URL from your Jira git configuration (**Git** ➜ **Manage repositories** ➜ **Actions** ➜ **Edit integration settings**).

2. Set the **Content-Type** request header to **application/json**.

3. Include the webhook secret key from your git configuration page (**Webhooks** section).

## How to send the single-repository reindex webhook

Send a POST request with this JSON body structure:

```json
{
  "repository": {
    "git_http_url": "https://gitlab.com/your-org/your-repo.git"
  }
}
```

Replace `https://gitlab.com/your-org/your-repo.git` with your actual repository URL.

**Example request:**

![](https://bigbrassband.com/images/bbb/webhook-reindex-post-api-json.png)

## How to verify the single-repository reindex result

After sending the webhook request, the repository enters the indexing queue. You can verify this on the **Git** ➜ **Manage git repositories** page.

