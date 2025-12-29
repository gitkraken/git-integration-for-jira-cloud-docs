---
title: Adding webhooks for Bitbucket Cloud
description: Configure webhooks for Bitbucket Cloud repositories in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

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

## Configure Bitbucket Cloud Webhooks

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

## Enable Pull Request Webhooks

For pull request events, configure three separate triggers:

1. Repository - **Push** (required)
2. Pull Request - **Created**
3. Pull Request - **Updated**

![](/wp-content/uploads/gij-webhooks-bitbucket-sample.png)

<kbd>Last updated: December 2025</kbd>
