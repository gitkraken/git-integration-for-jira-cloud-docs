---

title: Permissions
description: Permission requirements for viewing commit information and Git data in Jira
taxonomy:
    category: git-integration-for-jira-cloud

---

## Permissions Required to View Commit Information

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Users must have the <b>View Development Tools</b> permission to view commit information on issue pages.
        <p style='margin-bottom:-10px'>Administrators must also grant themselves this permission to view commit information.</p>
    </div>
    </div>
</div>

Users must belong to the developers group to view code diffs when using the default permission scheme.

![](/wp-content/uploads/gij-gitcloud-jira-view-dev-tools-project-acl.png)

When setting permissions, keep the following in mind:

- Permission names may differ depending on your Jira version.
- Configure project permissions on the project administration page. Different projects may have different permissions.
- The default permission scheme grants access to the app for all members of the **administrators** and **developers** groups. No additional configuration is required in this case.

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
