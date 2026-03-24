---
title: "Adding webhooks for GitLab repository"
description: "Configure webhooks for GitLab repositories in Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Adding webhooks for GitLab repository"
content_type: "reference"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["GitLab"]
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "reference", "admin", "GitLab"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Git Integration for Jira Cloud uses GitLab webhooks to trigger faster indexing updates after push and merge request activity. Use this page when a GitLab repository is already connected and you want GitLab to send webhook notifications to Jira Cloud instead of relying only on polling.

| GitLab webhook setup choice | Use when | Events to enable | Notes |
| :--- | :--- | :--- | :--- |
| Push-only webhook | You only need commit indexing | Push events | Basic GitLab webhook setup |
| Push plus merge request webhook | You need commit and merge request updates | Push events, Merge request events | Recommended for fuller GitLab coverage |
| System hooks | You manage a self-hosted GitLab instance centrally | Merge request and project-level events | Reduces per-project configuration time on self-hosted GitLab |

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Supported webhook events:</b>
        <ul style='margin-bottom:0px !important'>
            <li>Push events</li>
            <li>Merge request events</li>
        </ul>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>GitLab System Hooks:</b> For self-hosted GitLab instances, use System Hooks (Admin Area ➜ System Hooks ➜ Merge Request events) to reduce configuration time.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Prerequisite:</b> Enable webhooks in the Git Integration for Jira app before proceeding. See <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'><b>Indexing Triggers - Getting Started</b></a>.
    </div>
    </div>
</div>

&nbsp;

## How to configure a GitLab webhook for push events

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

## How to enable merge request webhook events in GitLab

To receive both push and merge request events:

1. Go to your repository's **Settings** ➜ **Webhooks**.

2. Edit your existing webhook or create a new one.

3. Select both triggers:
    - **Push events**
    - **Merge request events**

    ![](/wp-content/uploads/gij-gitlab-merge-request-event-trigger-webhook.png)

4. Click **Add webhook** or **Save changes**.

