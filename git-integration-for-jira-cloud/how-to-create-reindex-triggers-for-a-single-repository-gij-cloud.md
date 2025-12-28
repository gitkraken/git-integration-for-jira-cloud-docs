---

title: How to Create Reindex Triggers for a Single Repository
description: Create webhook triggers to reindex a single repository in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud

---
To create a webhook that triggers the reindex of a single repository, the following requirements are required::

1. The **`git_http_url`** matches the **Repository Origin** URL from the Jira git configuration page (**Git** \> **Manage repositories** \> **Actions** \> **Edit integration settings**).

2. The **Content-Type** request header is set to **application/json**.

3\. Use the webhook secret key from the git configuration page > **Webhooks**.

The webhook is a POST request with the following JSON body:

```diff
{
  "repository":
    { "git_http_url": "https://gitlab.com/bbb-dev/bbb-testrepo.git" }
}
```

**For example:**

![](https://bigbrassband.com/images/bbb/webhook-reindex-post-api-json.png)

**Result:**

The repository enters the indexing queue in the **Git** > **Manage git repositories** configuration page.

<kbd>Last updated: December 2025</kbd>

