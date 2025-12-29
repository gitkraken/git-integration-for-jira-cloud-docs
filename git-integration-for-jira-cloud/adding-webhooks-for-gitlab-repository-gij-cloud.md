---
title: Adding webhooks for GitLab repository
description: Configure webhooks for GitLab repositories in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

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

<kbd>Last updated: December 2025</kbd>
