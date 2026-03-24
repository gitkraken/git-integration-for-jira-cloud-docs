---
title: "Adding webhooks for Azure DevOps Server | TFS"
description: "Configure webhooks for Azure DevOps Server (TFS) in Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Adding webhooks for Azure DevOps Server | TFS"
content_type: "reference"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["Azure DevOps Server"]
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "reference", "admin", "Azure DevOps Server"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Git Integration for Jira Cloud uses Azure DevOps Server or TFS service hooks to trigger faster indexing updates after pushes and pull request activity. Use this page when an Azure DevOps Server or TFS project is already connected and you want webhook-driven updates instead of relying only on polling.

| Azure DevOps Server or TFS webhook setup choice | Use when | Events to enable | Notes |
| :--- | :--- | :--- | :--- |
| Code pushed only | You only need commit indexing | Code pushed | Basic server-side setup |
| Code pushed plus pull request events | You need commit and pull request updates | Code pushed, Pull request created, Pull request updated | Recommended for fuller coverage |
| Service hook test before finish | You want to validate the endpoint before saving | Same event as the current hook | Use the built-in Test action before Finish |

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Supported webhook events:</b>
        <ul style='margin-bottom:0px;'>
            <li>Code pushed</li>
            <li>Pull request created</li>
            <li>Pull request updated</li>
            <li>Pull request merge attempted</li>
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

## How to configure an Azure DevOps Server or TFS webhook

1. Log in to your Azure DevOps Server/TFS account and open a project.

    ![](/wp-content/uploads/gij-webhooks-azure-devops-sel-proj-c.png)

2. Go to **Project Settings** ➜ **Service Hooks** (sidebar).

    ![](/wp-content/uploads/gij-cloud-TFS-create-add-new-subscription-c.png)

3. Click **Create subscription**.

4. Scroll down and select **Web Hooks**, then click **Next**.

    ![](/wp-content/uploads/gij-webhooks-azure-devops-triggers-cfg-c.png)

5. Configure the trigger:

    a. Set **Trigger on this type of event** to **Code pushed**
    
    b. Set all **FILTERS** to **Any**
    
    c. Click **Next**

    ![](/wp-content/uploads/gij-webhooks-azure-devops-action-cfg-c.png)

6. Get the webhook URL from Jira:

    - Go to **Apps** ➜ **Git Integration: Manage integrations** ➜ **Indexing triggers**
    
        ![](/wp-content/uploads/gij-gitcloud-gitmgr-indexing-triggers-url-link-loc-2025.png)
    
    - Click the copy icon to copy the complete webhook URL

7. Configure the action settings:

    ![](/wp-content/uploads/gij-cloud-TFS-action-settings-header-etc-c.png)

    | Setting | Value |
    |---------|-------|
    | URL | Paste the webhook URL from step 6 |
    | HTTP header | `X-GIJ-Microsoft-Event:1` |
    | Resource details to send | All |
    | Messages to send | None |
    | Detailed messages to send | None |

    <div class="bbb-callout bbb--tip">
        <div class="irow">
        <div class="ilogobox">
            <span class="logoimg"></span>
        </div>
        <div class="imsgbox">
            Setting Messages and Detailed messages to <b>None</b> limits data transfer and prevents performance degradation from excessive webhook traffic.
        </div>
        </div>
    </div>

8. Click **Test** to verify the webhook configuration.

    ![](/wp-content/uploads/gij-cloud-TFS-webook-test-verify-c.png)

9. Click **Finish**.

&nbsp;

## How to enable pull request webhook events in Azure DevOps Server or TFS

Create separate service hooks for each pull request event:

1. **Code pushed** (configured above)
2. **Pull request created**
3. **Pull request updated**

Repeat steps 3-9 for each event type, changing only the trigger event in step 5a.

![](/wp-content/uploads/gij-cloud-TFS-webhook-service-hook-list-c.png)

