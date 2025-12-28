---

title: Setting Project Permissions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
**What’s on this page:**
- [Introduction](#introduction)
- [Instructions for integrations (GitLab, GitHub, etc)](#instructions-for-integrations-gitlab-github-etc)
(#video-example-2-setting-project-permissions-at-the-repository-level-for-an-existing-gitlab-integration)
- [Instructions for individual repositories](#instructions-for-individual-repositories)

<p>&nbsp;</p>
* * *
<p>&nbsp;</p>

## Introduction

By default - integrations (GitLab, GitHub, etc) and individual repositories are associated with all Jira projects. Jira administrators can limit which Jira projects are associated to integrations or individual repositories.

**Related Features**
Associating a Jira project with an integration or repository will limit repository content displaying in:

*   **Git Commits** issue tab

*   **Git Roll Up** issue tab

*   **Git Source Code** issue side panel

*   **View all repositories** page

*   **Repository Browser: Browse** page

*   **Repository Browser: Commits** page

*   **Repository Browser: Compare** page

*   **Create branch issue** dialog

*   **Create pull/merge request** issue dialog


Jira users must have the **View Development Tools** permission in the context of a Jira project to view content from the Git Integration for Jira app.

## Instructions for integrations (GitLab, GitHub, etc)

To limit which Jira projects are associated with an integration's repositories:

1.  Navigate to menu Git ➜ **Manage Git repositories**.

2.  Add a new integration or edit existing integration's settings.

3.  Locate the **Project Permissions** setting.

4.  Uncheck **Associate with all projects**.

5.  Select one or more Jira projects (at least one must be selected).

6.  Click **Update**.

## Instructions for individual repositories

To limit which Jira projects are associated for individual repositories:

1.  Navigate to menu Git ➜ **Manage Git repositories**.

2.  Add a new repository or edit existing repository's settings.

3.  Locate the **Project Permissions** setting.

4.  Uncheck **Associate with all projects**.

5.  Select one or more Jira projects (at least one must be selected).

6.  Click **Update**.


