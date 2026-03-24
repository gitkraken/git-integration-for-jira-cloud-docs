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

Git Integration for Jira Cloud uses the Git service integration wizard to connect supported git hosts and import multiple repositories into Jira Cloud. Use this wizard when you want the main multi-repository setup path for GitHub, GitLab, Bitbucket, Azure DevOps, AWS CodeCommit, or Gerrit instead of manual single-repository setup or webhook indexing.

**Requirements**

- Jira Cloud with Git Integration for Jira Cloud installed
- Jira Administrator access to Manage integrations
- Credentials for the git host you want to connect, such as OAuth access or a personal access token

| Setup path | Repository scope | Best for | Notes |
| :--- | :--- | :--- | :--- |
| Git service integration wizard | Multiple repositories | Supported git hosts where you want the main automated setup path | Recommended for multi-repository configuration |
| Single git integration wizard | Single repository | One SSH or HTTP(S) repository | Manual repository-by-repository setup |
| Webhook indexing integration | Multiple repositories | Git servers behind a firewall that can send outbound webhooks | Limited features compared with Git service integration |

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

## How to start the Git service integration wizard

On the Manage integrations page, click **Add integration** to start connecting git repositories from your git host service.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## How to choose the git host and authentication method

Click a git service from the list, then set up the **OAuth** or **PAT** integration type. Click **Connect...** to proceed.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-sel-git-host-service-page-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## How to select repositories to connect

After the scan completes, select one or more repositories to connect to Jira, then click **Connect repositories**.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-bitbucket-repo-sel-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## What happens after the integration is created

The integration is added to the git integration configuration list.

<img src='/wp-content/uploads/gij-gitcloud-gitmgr-add-new-integration-complete-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## When to use another integration setup path

For more detailed information on specific integration steps for supported git host services, see our [Integration Guides](/git-integration-for-jira-cloud/integration-guide-gij-cloud).

&nbsp;
* * *

[**Prev:** Git integration configuration page](/git-integration-for-jira-cloud/git-integration-configuration-page-gij-cloud)

[**Next:** Using the Webhook indexing integration wizard](/git-integration-for-jira-cloud/webhook-indexing-integration-gij-cloud)

<p>&nbsp;</p>

