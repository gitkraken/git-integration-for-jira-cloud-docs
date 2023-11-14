---

title: Manager permissions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class='embed-container embed-container--16-9'>
        <iframe width='709' height='382' src='https://www.youtube.com/watch?v=2tmWvRxj9Ls' frameborder='0' allowfullscreen ></iframe>
    </div>

<div align='center' stye='margin-top:12px;margin-ottom:40px;'>
    <i>Right click <a href='https://www.youtube.com/watch?v=2tmWvRxj9Ls'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

This feature is intended for Jira admins because it offloads work off from them. This will give assigned users the ability to administer the Git Integration for Jira app without giving full JIra admin role to them.

Before, the only people that can manage Git Integration for Jira app are Jira admins. And now with this new feature, it allows Jira admins to select other Jira users (that are not Jira admins) and get them permissions to Manage integrations, add/remove/update, manage apps etc.

With Manager permissions:

*   Share Git Integration for Jira app control with other (non-admin) Jira users

*   Change app settings, add/update integrations

*   Manage user roles through Jira Global Permissions

&nbsp;

### Getting started

A new item called **Manager permissions** is introduced on the Git Integration for Jira sidebar menu.

![](/wp-content/uploads/gij-gitserverdc-manager-permission-access-location.png)

1.  On your Jira dashboard menu, go to Apps ➜ Git Integration: Manage integrations ➜ **Manager permissions**. (As an admin)

    The first time you are accessing the Manager permissions page, there will be no active managers displayed yet. But once you add more users, you will start to see this list populate.

    ![](/wp-content/uploads/gij-gitserverdc-manage-permissions-admin-groups-sel.png)

    &nbsp;

2.  Click on the **Admin \> Groups** label link on the Manager permissions page to take you to the Groups page.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-create-group.png)

    &nbsp;

3.  You can create a new group or use an existing group. For this guide, click **Create group**. The following dialog is displayed.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-create-group-dlg.png)

    *   Enter Group's name as required. For this guide, enter "GIJ Managers".

    *   For Group's members, start adding one or more users to this group.

    This creates the specified group and displays it in the Groups list.

    &nbsp;

4.  Switch to the Manager permissions page (browser tab) then click **System \> Global permissions**.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-sys-global-acl.png)
    
    &nbsp;

5.  On the Global permissions screen, the page is automatically scrolled to the **Grant Permission** section.

    ![](/wp-content/uploads/gij-gitserverdc-manager-permission-global-grant-permission.png)

    *   Select a permission --> Manage Git Integration for Jira by GitKraken.

    *   Select a group --> choose the group that you created previously.

    &nbsp;

6.  Click **Add** to continue.

Looking at the **Manage Git Integration for Jira by GitKraken** permission section, you will see the roles that were assigned to this permission.

![](/wp-content/uploads/gij-gitserverdc-manager-permission-role-display.png)

&nbsp;

Switch back to the **Manager permission** page to see the recently active managers list.

![](/wp-content/uploads/gij-gitserverdc-manager-permission-active-user-list.png)

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Recent active managers gets populated for every user that is added to the GIJ Manager group.
    </div>
    </div>
</div>

&nbsp;

### What do users with the manager role have access to?

Every user that you add in the GIJ Managers group will have full access to the Git Integration for Jira app configuration, including changing settings and adding/managing integrations.

**GIJ Managers** cannot modify permissions nor view the Manager permissions page. Only Jira admins remain the only role with this level of access.

![](/wp-content/uploads/gij-gitserverdc-users-gij-manager-view-access.png)

&nbsp;

### What will the non-admin users see when trying to access Git Integration for Jira app?

Non-admin users will not be able to see or access the Git Integration for Jira app configuration or the Manger permissions pages.

![](/wp-content/uploads/gij-gtiserverdc-users-global-plain-user.png)


