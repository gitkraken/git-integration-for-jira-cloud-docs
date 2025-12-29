---
title: Manager permissions
description: Learn how to configure manager permissions in Git Integration for Jira Cloud to delegate app administration to non-admin users.
taxonomy:
    category: git-integration-for-jira-cloud
---

Manager permissions allow Jira administrators to delegate Git Integration for Jira app management to non-admin users. Designated users can manage integrations, add or remove repositories, and update settings without requiring full Jira admin access.

**On this page:**
- [Understand manager permissions](#understand-manager-permissions)
- [Set up manager permissions](#set-up-manager-permissions)
- [Understand manager access levels](#understand-manager-access-levels)

&nbsp;
* * *
&nbsp;

## Understand Manager Permissions

With manager permissions, you can:

- Share Git Integration for Jira app control with non-admin Jira users
- Allow managers to change app settings and add or update integrations
- Manage user roles through Jira Global Permissions
- Enable managers to create integrations with project mapping settings

&nbsp;

## Set Up Manager Permissions

### Step 1: Access Manager Permissions

1. Go to **Apps** ➜ **Git Integration: Manage integrations**.
2. Click **Manager permissions** in the sidebar.

![](/wp-content/uploads/gij-gitserverdc-manager-permission-access-location-2025.png)

When you first access the Manager permissions page, no active managers appear. The list populates as you add users.

![](/wp-content/uploads/gij-gitserverdc-manage-permissions-admin-groups-sel-2025.png)

### Step 2: Create a Manager Group

1. Click the **Admin > Groups** label link on the Manager permissions page.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-create-group-2025.png)

2. Click **Create group**.

3. Configure the group:

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-create-group-dlg-2025.png)

    - Enter a group name (for example, "GIJ Managers")
    - Add one or more users to this group

4. Click **Create group** to save.

Jira creates the group and displays it in the Groups list.

### Step 3: Grant Global Permission

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

### Step 4: Verify Manager Access

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

## Understand Manager Access Levels

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

<kbd>Last updated: December 2025</kbd>
