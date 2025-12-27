---

title: Manager permissions
description: Learn how to configure manager permissions in Git Integration for Jira Cloud to delegate app administration to non-admin users.
taxonomy:
    category: git-integration-for-jira-cloud

---

Manager permissions allow Jira administrators to delegate Git Integration for Jira app management to non-admin users. This feature reduces the administrative burden on Jira admins while giving designated users the ability to manage integrations without requiring full Jira admin access.

Previously, only Jira administrators could manage the Git Integration for Jira app. With manager permissions, Jira admins can grant other Jira users (who are not Jira admins) the ability to manage integrations, add or remove repositories, update settings, and more.

With manager permissions, you can:

- Share Git Integration for Jira app control with non-admin Jira users
- Allow managers to change app settings and add or update integrations
- Manage user roles through Jira Global Permissions
- Enable managers to create integrations with project mapping settings

&nbsp;

## Getting started

A new item called **Manager permissions** appears on the Git Integration for Jira sidebar menu.

![](/wp-content/uploads/gij-gitserverdc-manager-permission-access-location-2025.png)

1. On your Jira dashboard menu, go to Apps ➜ Git Integration: Manage integrations ➜ **Manager permissions** (as an admin).

    When you first access the Manager permissions page, no active managers appear. The list populates as you add users.

    ![](/wp-content/uploads/gij-gitserverdc-manage-permissions-admin-groups-sel-2025.png)

    &nbsp;

2. Click the **Admin \> Groups** label link on the Manager permissions page to open the Groups page.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-create-group-2025.png)

    &nbsp;

3. Create a new group or use an existing group. For this guide, click **Create group**. The following dialog appears:

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-create-group-dlg-2025.png)

    - Enter a group name. For this guide, enter "GIJ Managers".
    - Add one or more users to this group.

    Jira creates the specified group and displays it in the Groups list.

    &nbsp;

4. Switch to the Manager permissions page (browser tab), then click **System \> Global permissions**.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-sys-global-acl-2025.png)
    
    &nbsp;

5. On the Global permissions screen, the page automatically scrolls to the **Grant Permission** section.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-global-grant-permission-2025.png)

    - This feature adds a new global permission to your Jira instance. Select **Manage Git Integration for Jira by GitKraken** for this step.
    - Select the group you created previously.
    
6. Click **Add** to continue.

The **Manage Git Integration for Jira by GitKraken** permission section displays the roles assigned to this permission.

![](/wp-content/uploads/gij-gitserverdc-manager-permission-role-display-2025.png)

&nbsp;

Switch back to the **Manager permission** page to see the recently active managers list.

![](/wp-content/uploads/gij-gitserverdc-manager-permission-active-user-list-2025.png)

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The recent active managers list populates for every user added to the GIJ Manager group.
    </div>
    </div>
</div>

&nbsp;

## What do users with the manager role have access to?

Users in the GIJ Managers group have full access to the Git Integration for Jira app configuration, including changing settings and adding or managing integrations.

**GIJ Managers** cannot modify permissions or view the Manager permissions page. Only Jira admins have this level of access.

&nbsp;

## What do non-admin users see when accessing Git Integration for Jira?

Non-admin users who are not in the GIJ Managers group cannot see or access the Git Integration for Jira app configuration or the Manager permissions pages.

<kbd>Last updated: December 2025</kbd>
