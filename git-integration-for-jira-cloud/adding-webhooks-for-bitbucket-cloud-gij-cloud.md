---
title: "Adding webhooks for Bitbucket Cloud"
description: "Configure webhooks for Bitbucket Cloud repositories in Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Adding webhooks for Bitbucket Cloud"
content_type: "reference"
audience: "developer"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["Bitbucket Cloud"]
role_required: "User"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "reference", "developer", "Bitbucket Cloud"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Git Integration for Jira Cloud uses Bitbucket Cloud webhooks to trigger faster indexing updates after repository pushes and pull request activity. Use this page when a Bitbucket Cloud repository is already connected and you want webhook-driven updates instead of waiting for the default polling interval.

| Bitbucket Cloud webhook setup choice | Use when | Events to enable | Notes |
| :--- | :--- | :--- | :--- |
| Repository push only | You only need commit indexing | Repository push | Basic Bitbucket setup |
| Repository push plus pull request events | You need commit and pull request updates | Repository push, Pull request created, Pull request updated | Recommended for fuller Bitbucket coverage |
| Full trigger list selection | You want precise control over enabled events | Choose from the full trigger list | Use when the simplified trigger list is too limited |

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Supported webhook events:</b>
        <ul style='margin-bottom:0px;'>
            <li>Repository - Push</li>
            <li>Pull request - Created</li>
            <li>Pull request - Updated</li>
        </ul>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Prerequisite:</b> Enable webhooks in the Git Integration for Jira app before proceeding. See <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'><b>Indexing triggers - Getting Started</b></a>.
    </div>
    </div>
</div>

&nbsp;

## How to configure a Bitbucket Cloud webhook

1. Log in to Bitbucket and open your project.

    ![](/wp-content/uploads/gij-webhooks-bitbucket-add-shooks-c.png)

2. Go to **Repository Settings** ➜ **Webhooks** (under WORKFLOW).

3. Click **Add webhook**.

    ![](/wp-content/uploads/gij-webhooks-add-new-whook-bitbucket-dlg-w.png)

4. Configure the webhook:

    - **Title**: Enter a descriptive name for the webhook
    - **URL**: Paste the Secret URL from Git Integration for Jira ➜ **Indexing triggers** page
    
        ![](/wp-content/uploads/gij-gitcloud-gitmgr-indexing-triggers-url-link-loc-2025.png)

5. Under **Triggers**, select one of these options:

    **For commits only:**
    - Select **Repository push**

    **For commits and pull requests (recommended):**
    - Click **Choose from a full list of triggers**
    - Select **Repository** ➜ **Push**
    - Select **Pull Request** ➜ **Created** and **Updated**

6. Click **Save**.

&nbsp;

## How to enable pull request webhook events in Bitbucket Cloud

For pull request events, configure three separate triggers:

1. Repository - **Push** (required)
2. Pull Request - **Created**
3. Pull Request - **Updated**

![](/wp-content/uploads/gij-webhooks-bitbucket-sample.png)

