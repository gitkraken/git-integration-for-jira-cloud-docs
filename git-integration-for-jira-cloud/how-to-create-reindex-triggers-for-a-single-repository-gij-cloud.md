---
title: How to Create Reindex Triggers for a Single Repository
description: Create webhook triggers to reindex a single repository in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

Create a webhook that triggers reindexing for a specific repository by following these requirements.

## Requirements

Your webhook must meet these criteria:

1. The **`git_http_url`** in the request body must match the **Repository Origin** URL from your Jira git configuration (**Git** ➜ **Manage repositories** ➜ **Actions** ➜ **Edit integration settings**).

2. Set the **Content-Type** request header to **application/json**.

3. Include the webhook secret key from your git configuration page (**Webhooks** section).

## Configure the Webhook

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

## Verify the Result

After sending the webhook request, the repository enters the indexing queue. You can verify this on the **Git** ➜ **Manage git repositories** page.

<kbd>Last updated: December 2025</kbd>
