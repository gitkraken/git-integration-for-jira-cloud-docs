---
title: "Adding webhooks for GitLab repository"
description: "Configure webhooks for GitLab repositories in Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Adding webhooks for GitLab repository"
content_type: "how-to"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["GitLab"]
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "reference", "admin", "GitLab"]
llms_include: true
taxonomy:
    category: git-integration-for-jira-cloud
custom_fields:
    nav_category: "how-to-articles-gij-cloud"
    nav_label: "Adding Indexing Triggers for GitLab repository"
    nav_order: 20
    nav_parent: "indexing-triggers-gij-cloud"
    page_type: "content"
---
<kbd>Last updated: March 2026</kbd>

> **Tip:** **Supported webhook events:**
>
> - Push events
> - Merge request events

> **Tip:** **GitLab System Hooks:** For self-hosted GitLab instances, use System Hooks (Admin Area ➜ System Hooks ➜ Merge Request events) to reduce configuration time.

> **Warning:** **Prerequisite:** Enable webhooks in the Git Integration for Jira app before proceeding. See [**Indexing Triggers - Getting Started**](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud).

&nbsp;

## Configure GitLab Webhooks

1. Log in to your GitLab account and select a repository.

    ![](/wp-content/uploads/gij-web-hooks-gitlab-settings-c.png)

2. Go to **Settings** ➜ **Webhooks** (sidebar).

    ![](/wp-content/uploads/gij-web-hooks-gitlab-settings-add-c.png)

3. Configure the webhook:

    - **URL**: Paste the Secret URL from Git Integration for Jira ➜ **Webhooks** page
    
        ![](/wp-content/uploads/gij-gitcloud-gitmgr-indexing-triggers-url-link-loc-2025.png)

4. Under **Trigger**, select **Push events** (default option).

5. Click **Add webhook**.

&nbsp;

## Enable Merge Request Webhooks

To receive both push and merge request events:

1. Go to your repository's **Settings** ➜ **Webhooks**.

2. Edit your existing webhook or create a new one.

3. Select both triggers:
    - **Push events**
    - **Merge request events**

    ![](/wp-content/uploads/gij-gitlab-merge-request-event-trigger-webhook.png)

4. Click **Add webhook** or **Save changes**.
