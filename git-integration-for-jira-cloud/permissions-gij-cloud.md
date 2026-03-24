---
title: "Permissions"
description: "Permission requirements for viewing commit information and Git data in Jira"
product: "Git Integration for Jira Cloud"
feature: "Permissions"
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

Git Integration for Jira Cloud relies on Jira project permissions to determine who can view commit information, code diffs, and development data on issue pages. Use this page when a user cannot see Git activity in Jira Cloud and you need to verify the minimum Jira permissions required for the app features to appear.

| Action | Minimum Jira permission | Typical group or role | Notes |
| :--- | :--- | :--- | :--- |
| View commit information on issue pages | View Development Tools | Developers, administrators, or equivalent project role | Administrators must grant this permission to themselves too |
| View code diffs with the default scheme | View Development Tools plus the relevant project access | Developers group in the default permission scheme | Custom permission schemes may differ by project |

## Which permissions are required to view commit information

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

