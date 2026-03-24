---
title: "Manager permissions"
description: "Learn how to configure manager permissions in Git Integration for Jira Cloud to delegate app administration to non-admin users."
product: "Git Integration for Jira Cloud"
feature: "Manager permissions"
content_type: "admin"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "admin"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Manager permissions allow Jira administrators to delegate Git Integration for Jira app management to non-admin users. Designated users can manage integrations, add or remove repositories, and update settings without requiring full Jira admin access.

| Access level | Use when | Can do | Cannot do |
| :--- | :--- | :--- | :--- |
| Jira Administrator | You need full control over app configuration and permissions | Manage integrations, settings, and permission assignment | N/A |
| GIJ Manager group member | You want to delegate day-to-day app management to non-admin users | Manage integrations, repositories, and app settings | Cannot change permissions or access the Manager permissions page |
| Regular non-manager user | You only need to use Jira and view Git data | Standard end-user Git Integration features | Cannot manage integrations or manager settings |

**On this page:**
- [Understand manager permissions](#understand-manager-permissions)
- [Set up manager permissions](#set-up-manager-permissions)
- [Understand manager access levels](#understand-manager-access-levels)

&nbsp;
* * *
&nbsp;

## How manager permissions work

With manager permissions, you can:

- Share Git Integration for Jira app control with non-admin Jira users
- Allow managers to change app settings and add or update integrations
- Manage user roles through Jira Global Permissions
- Enable managers to create integrations with project mapping settings

&nbsp;

## How to set up manager permissions

### How to open the Manager permissions page

1. Go to **Apps** ➜ **Git Integration: Manage integrations**.
2. Click **Manager permissions** in the sidebar.

![](/wp-content/uploads/gij-gitserverdc-manager-permission-access-location-2025.png)

When you first access the Manager permissions page, no active managers appear. The list populates as you add users.

![](/wp-content/uploads/gij-gitserverdc-manage-permissions-admin-groups-sel-2025.png)

### How to create a manager group

1. Click the **Admin > Groups** label link on the Manager permissions page.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-create-group-2025.png)

2. Click **Create group**.

3. Configure the group:

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-create-group-dlg-2025.png)

    - Enter a group name (for example, "GIJ Managers")
    - Add one or more users to this group

4. Click **Create group** to save.

Jira creates the group and displays it in the Groups list.

### How to grant the global permission for Git Integration management

1. Return to the Manager permissions page (browser tab).

2. Click **System > Global permissions**.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-sys-global-acl-2025.png)

3. The page scrolls to the **Grant Permission** section.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-global-grant-permission-2025.png)

4. Select **Manage Git Integration for Jira by GitKraken** from the permission dropdown.

5. Select the group you created (for example, "GIJ Managers").

6. Click **Add**.

The **Manage Git Integration for Jira by GitKraken** permission section displays the assigned roles:

![](/wp-content/uploads/gij-gitserverdc-manager-permission-role-display-2025.png)

### How to verify manager access

Return to the **Manager permission** page to view the active managers list:

![](/wp-content/uploads/gij-gitserverdc-manager-permission-active-user-list-2025.png)

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The active managers list updates automatically when you add users to the GIJ Manager group.
    </div>
    </div>
</div>

&nbsp;

## What each manager access level allows

### What Managers Can Do

Users in the GIJ Managers group have full access to Git Integration for Jira app configuration:

- Change app settings
- Add, update, or remove integrations
- Manage repositories

### What Managers Cannot Do

GIJ Managers **cannot**:

- Modify permissions
- View the Manager permissions page

Only Jira administrators have access to permission management.

### What Non-Manager Users See

Non-admin users who are not in the GIJ Managers group cannot see or access:

- Git Integration for Jira app configuration
- Manager permissions pages

