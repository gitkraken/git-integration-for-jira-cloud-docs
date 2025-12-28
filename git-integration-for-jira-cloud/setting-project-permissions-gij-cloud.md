---

title: Setting Project Permissions
description: Configure project permissions to control which Jira projects can access Git integration data and repository content.
taxonomy:
    category: git-integration-for-jira-cloud

---

- [Introduction](#introduction)
- [Instructions for integrations](#instructions-for-integrations-gitlab-github-etc)
- [Instructions for individual repositories](#instructions-for-individual-repositories)

&nbsp;

## Introduction

By default, integrations (GitLab, GitHub, etc.) and individual repositories associate with all Jira projects. Jira administrators can limit which Jira projects associate with integrations or individual repositories.

**Related features**

Associating a Jira project with an integration or repository limits repository content display in:

*   Git Commits issue tab
*   Git Roll Up issue tab
*   Git Source Code issue side panel
*   View all repositories page
*   Repository Browser: Browse page
*   Repository Browser: Commits page
*   Repository Browser: Compare page
*   Create branch issue dialog
*   Create pull/merge request issue dialog

Jira users need the **View Development Tools** permission in a Jira project context to view Git Integration for Jira content.

&nbsp;

## Instructions for integrations (GitLab, GitHub, etc.)

To limit which Jira projects associate with an integration's repositories:

1.  Go to **Git** ➜ **Manage Git repositories**.

2.  Add a new integration or edit an existing integration.

3.  Find the **Project Permissions** setting.

4.  Clear **Associate with all projects**.

5.  Select one or more Jira projects.

6.  Click **Update**.

&nbsp;

## Instructions for individual repositories

To limit which Jira projects associate with individual repositories:

1.  Go to **Git** ➜ **Manage Git repositories**.

2.  Add a new repository or edit an existing repository.

3.  Find the **Project Permissions** setting.

4.  Clear **Associate with all projects**.

5.  Select one or more Jira projects.

6.  Click **Update**.

<kbd>Last updated: December 2025</kbd>
