---
title: "Administration"
description: "Administration resources for Git Integration for Jira Cloud including manager permissions, trusted users, and general settings."
product: "Git Integration for Jira Cloud"
feature: "Administration"
content_type: "security"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "security", "admin"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

The Administration hub collects the Git Integration for Jira Cloud pages Jira administrators use to delegate access, manage app-wide settings, and handle trusted-user administration. Use this page when you need to decide which admin guide applies to permissions, settings, or GitLab server API behavior.

| Administrative task | Use this page | When it applies |
| :--- | :--- | :--- |
| Delegate integration management without full Jira admin access | Configure Manager Permissions | You want selected users to manage integrations and repositories |
| Grant full Git Integration app access to invited users | Manage Trusted Users | You need users to access all app pages or invite others |
| Turn app features on or off globally | Configure General Settings | You want to control issue tabs, repository browser, beta features, or dev info behavior |
| Make a self-hosted GitLab server respond correctly to API calls | Set Up GitLab Server for API Calls | Users need correct clone links or inbound API behavior |

## How to choose the Git Integration for Jira Cloud admin guide

### [Configure Manager Permissions](/git-integration-for-jira-cloud/manager-permissions-gij-cloud)

Delegate Git Integration for Jira app management to non-admin users. Grant specific users the ability to manage integrations without requiring full Jira admin access.

### [Manage Trusted Users](/git-integration-for-jira-cloud/trusted-users-gij-cloud)

Assign the Trusted role to users who need administrative permissions for the Git Integration app. Trusted users can invite other users and access all app pages.

### [Configure General Settings](/git-integration-for-jira-cloud/general-settings-gij-cloud)

Adjust performance and feature settings for Git Integration for Jira Cloud through the App settings page.

### [Set Up GitLab Server for API Calls](/git-integration-for-jira-cloud/setup-gitlab-server-to-respond-to-incoming-network-api-calls-gij-cloud)

Configure your GitLab server to respond to incoming network API calls and provide correct repository clone links to users.
