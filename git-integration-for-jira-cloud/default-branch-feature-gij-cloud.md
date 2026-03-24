---
title: "Default branch feature"
description: "Learn how to configure default branches for repositories when creating new branches from Jira issues."
product: "Git Integration for Jira Cloud"
feature: "Default branch feature"
content_type: "integration"
audience: "all"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "all"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "integration"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Git Integration for Jira Cloud lets Jira users preselect a default branch for each repository when they create branches from Jira issues. Use this setting when different projects need different starting branches in the same repository, or when users should not choose the source branch manually each time.

**Requirements**

- Jira Cloud with Git Integration for Jira Cloud installed
- Access to create branches from Jira issues
- A connected repository with the branches you want to use as defaults

![](/wp-content/uploads/gij-gitcloud-user-settings-default-branches.png)

## How to add a default branch for a repository

Configure a default branch for a repository when creating new branches. Git Integration for Jira Cloud automatically selects your configured default branch each time you create a new branch from a Jira issue.

Click **+ Add default branch** to set up a default branch for the selected repository. The following dialog appears:

<img src='/wp-content/uploads/gij-gitcloud-user-settings-create-def-branch-dlg.png' style='margin:25px auto;max-width:100%;display:block;' />

## When to use different default branches by project

You can use different default branches from one repository for different projects. For example, if you have 3 projects and a repository with 3 branches:

<img src='/wp-content/uploads/gij-gitcloud-default-branch-flow.png' style='margin:25px auto;max-width:100%;display:block;' />

## How to edit or remove an existing default branch

Assign a branch for the selected repository using this interface:

![](/wp-content/uploads/gij-gitcloud-user-settings-default-branch-add-sel.png)

1.  Click **Edit** or **Delete** to modify the default branch configuration for the selected repository.

2.  Click **+ Add default branch** to add additional default branch configurations for the selected repository.

&nbsp;
* * *

[**Prev:** Connected apps](/git-integration-for-jira-cloud/connected-apps-gij-cloud)

[**Next:** Default repository feature](/git-integration-for-jira-cloud/default-repository-feature-gij-cloud)

