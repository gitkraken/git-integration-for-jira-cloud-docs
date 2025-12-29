---
title: Setting Project Permissions
description: Configure project permissions to control which Jira projects can access Git integration data and repository content.
taxonomy:
    category: git-integration-for-jira-cloud
---

**On this page:**
- [Understand project permissions](#understand-project-permissions)
- [Configure permissions for integrations](#configure-permissions-for-integrations)
- [Configure permissions for individual repositories](#configure-permissions-for-individual-repositories)

&nbsp;
* * *
&nbsp;

## Understand Project Permissions

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

## Configure Permissions for Integrations

Limit which Jira projects can access an integration's repositories:

1. Go to **Git** ➜ **Manage Git repositories**.

2. Add a new integration or edit an existing one.

3. Locate the **Project Permissions** setting.

4. Clear **Associate with all projects**.

5. Select one or more Jira projects from the list.

6. Click **Update** to save your changes.

&nbsp;

## Configure Permissions for Individual Repositories

Limit which Jira projects can access a specific repository:

1. Go to **Git** ➜ **Manage Git repositories**.

2. Add a new repository or edit an existing one.

3. Locate the **Project Permissions** setting.

4. Clear **Associate with all projects**.

5. Select one or more Jira projects from the list.

6. Click **Update** to save your changes.

<kbd>Last updated: December 2025</kbd>
