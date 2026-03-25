---
title: "Using the Git service integration wizard"
description: "How to use the Git service integration wizard to connect repositories"
product: "Git Integration for Jira Cloud"
feature: "Using the Git service integration wizard"
content_type: "integration"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "integration", "admin"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

The Git service integration (formerly full feature integration panel) contains special integration for specific git hosts, supports multiple connected repositories, and automates git integration.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        We highly recommend this feature for multiple repository configuration.
    </div>
    </div>
</div>
<br>

## Step 1

On the Manage integrations page, click **Add integration** to start connecting git repositories from your git host service.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## Step 2

Click a git service from the list, then set up the **OAuth** or **PAT** integration type. Click **Connect...** to proceed.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-sel-git-host-service-page-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## Step 3

After the scan completes, select one or more repositories to connect to Jira, then click **Connect repositories**.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-bitbucket-repo-sel-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## Completed Integration

The integration is added to the git integration configuration list.

<img src='/wp-content/uploads/gij-gitcloud-gitmgr-add-new-integration-complete-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## Other Integration Setup

For more detailed information on specific integration steps for supported git host services, see our [Integration Guides](/git-integration-for-jira-cloud/integration-guide-gij-cloud).

&nbsp;
* * *

[**Prev:** Git integration configuration page](/git-integration-for-jira-cloud/git-integration-configuration-page-gij-cloud)

[**Next:** Using the Webhook indexing integration wizard](/git-integration-for-jira-cloud/webhook-indexing-integration-gij-cloud)

<p>&nbsp;</p>
