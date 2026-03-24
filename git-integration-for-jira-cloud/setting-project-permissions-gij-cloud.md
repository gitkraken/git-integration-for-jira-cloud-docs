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

Git Integration for Jira Cloud uses project permissions to control which Jira projects can see repository content, developer-panel actions, and repository-browser data. Use this page when a Jira administrator needs a concise guide to restricting Git data by project; use the longer project-association page when you need the repository-level versus integration-level distinction in detail.

| Permission target | Use when | Scope | Notes |
| :--- | :--- | :--- | :--- |
| Integration permissions | You want multiple repositories in one integration to share the same project access | Whole integration | Faster to manage but broader in scope |
| Individual repository permissions | You want one repository to be visible only in selected projects | Single repository | Better for tighter project-level access control |

**On this page:**
- [Understand project permissions](#understand-project-permissions)
- [Configure permissions for integrations](#configure-permissions-for-integrations)
- [Configure permissions for individual repositories](#configure-permissions-for-individual-repositories)

&nbsp;
* * *
&nbsp;

## How project permissions affect Git data visibility

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

