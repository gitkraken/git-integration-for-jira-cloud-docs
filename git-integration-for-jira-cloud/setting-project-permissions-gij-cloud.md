---
title: "Setting Project Permissions"
description: "Configure project permissions to control which Jira projects can access Git integration data and repository content."
product: "Git Integration for Jira Cloud"
feature: "Setting Project Permissions"
content_type: "concept"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "concept", "admin"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Project permissions determine which Jira projects can access repository data from a Git Integration for Jira Cloud integration or from an individual connected repository. Use this page when you need to limit Git visibility by Jira project instead of exposing repository data to every project in the site.

| Permission scope | What it controls | Common use case |
| :--- | :--- | :--- |
| Integration-level project permissions | Access to all repositories under an integration | Restrict one git host connection to a specific set of Jira projects |
| Repository-level project permissions | Access to one connected repository | Expose only a single repository to a smaller project subset |
| Jira project permissions | Visibility of Git data inside Jira | Confirm users can still view development information after mapping projects |

**On this page:**
- [How project permissions work in Git Integration for Jira Cloud](#how-project-permissions-work-in-git-integration-for-jira-cloud)
- [How to configure project permissions for integrations](#how-to-configure-project-permissions-for-integrations)
- [How to configure project permissions for individual repositories](#how-to-configure-project-permissions-for-individual-repositories)

&nbsp;
* * *
&nbsp;

## How project permissions work in Git Integration for Jira Cloud

By default, integrations (GitLab, GitHub, etc.) and individual repositories associate with all Jira projects. Jira administrators can limit which projects have access to specific integrations or repositories.

### Affected Features

Project associations control which projects display repository content in:

- Git Commits issue tab
- Git Roll Up issue tab
- Git Source Code issue side panel
- View all repositories page
- Repository Browser: Browse page
- Repository Browser: Commits page
- Repository Browser: Compare page
- Create branch issue dialog
- Create pull/merge request issue dialog

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Users must have the <b>View Development Tools</b> permission in a Jira project to view Git Integration for Jira content.
    </div>
    </div>
</div>

&nbsp;

## How to configure project permissions for integrations

Limit which Jira projects can access an integration's repositories:

1. Go to **Git** ➜ **Manage Git repositories**.

2. Add a new integration or edit an existing one.

3. Locate the **Project Permissions** setting.

4. Clear **Associate with all projects**.

5. Select one or more Jira projects from the list.

6. Click **Update** to save your changes.

&nbsp;

## How to configure project permissions for individual repositories

Limit which Jira projects can access a specific repository:

1. Go to **Git** ➜ **Manage Git repositories**.

2. Add a new repository or edit an existing one.

3. Locate the **Project Permissions** setting.

4. Clear **Associate with all projects**.

5. Select one or more Jira projects from the list.

6. Click **Update** to save your changes.
