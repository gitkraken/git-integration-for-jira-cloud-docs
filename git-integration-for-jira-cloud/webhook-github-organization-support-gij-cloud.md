---
title: "Webhook GitHub Organization support"
description: "Configure organization-level webhooks in GitHub to automatically register webhooks for all repositories."
product: "Git Integration for Jira Cloud"
feature: "Webhook GitHub Organization support"
content_type: "reference"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["GitHub"]
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "reference", "admin", "GitHub"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Git Integration for Jira supports GitHub Organization webhooks. Configure webhooks at the organization level to automatically register webhooks for all repositories, eliminating the need to create individual webhooks for each repository.

![](/wp-content/uploads/gij-new-github-org-webhook-settings-page.png)

&nbsp;

## Configure GitHub Organization Webhooks

1. Log in to GitHub and open your organization.

2. Go to **Settings** ➜ **Webhooks** (under Organization Settings).

3. Click **Add webhook**.

4. Get the webhook URL from Jira:

    - Go to **Apps** ➜ **Git Integration: Manage integrations** ➜ **Indexing triggers**
    
    ![](/wp-content/uploads/gij-gitcloud-indexing-trigger-webhook-url-level-1-2025.png)

5. Paste the webhook URL into the **Payload URL** field.

6. Set **Content type** to **application/json**.

7. Select **Let me select individual events** and enable:

    - Branch or tag deletion
    - Branch or tag creation
    - Pull requests
    - Pushes

8. Click **Add webhook**.

All repositories in the organization will now send webhook events to Git Integration for Jira.
