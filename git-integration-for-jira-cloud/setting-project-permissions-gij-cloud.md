---

title: Setting Project Permissions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
**What’s on this page:**
- [Introduction](#introduction)
- [Instructions for integrations (GitLab, GitHub, etc)](#instructions-for-integrations-gitlab-github-etc)
  - [Video Example 1: Setting project permissions for an existing GitLab integration](#video-example-1-setting-project-permissions-for-an-existing-gitlab-integration)
  - [Video Example 2: Setting project permissions at the repository level for an existing GitLab integration](#video-example-2-setting-project-permissions-at-the-repository-level-for-an-existing-gitlab-integration)
- [Instructions for individual repositories](#instructions-for-individual-repositories)
  - [Video Example: Setting project permissions for a repository](#video-example-setting-project-permissions-for-a-repository)

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


### Video Example 1: Setting project permissions for an existing GitLab integration

<div class='embed-container' style='padding-bottom:75.21%;'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/rnm5t639cz?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px;margin-bottom:30px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/rnm5t639cz'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

### Video Example 2: Setting project permissions at the repository level for an existing GitLab integration

<div class='embed-container' style='padding-bottom:75.0%;'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/fder2qnpgw?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px;margin-bottom:30px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/fder2qnpgw'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

## Instructions for individual repositories

To limit which Jira projects are associated for individual repositories:

1.  Navigate to menu Git ➜ **Manage Git repositories**.

2.  Add a new repository or edit existing repository's settings.

3.  Locate the **Project Permissions** setting.

4.  Uncheck **Associate with all projects**.

5.  Select one or more Jira projects (at least one must be selected).

6.  Click **Update**.


### Video Example: Setting project permissions for a repository

<div class='embed-container' style='padding-bottom:75.21%;'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/xvzj32nxou?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px;margin-bottom:30px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/xvzj32nxou'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

