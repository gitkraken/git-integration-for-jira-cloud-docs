---

title: Jira Git integration development panel
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This page applies to Jira Server, Jira Data Center and Jira Cloud.

## Permissions

**Jira Cloud - Development panel**<br>
The **View Development Tools** _permission_ only applies to Jira Classic Projects. Next-Gen Projects don't allow to modify the permission.

**Create Branches and Branch Names**<br>
For connected GitHub git host, this feature requires enabled `public_repo` scope permissions.

**Commits Ahead and Behind**<br>
If the user does not have the **View Development Tools** _project permission_ for the project, the developer panel will be unavailable for that user.

## Getting started

Git links are now available on the developer panel in the following locations:

*   Issue page

*   Search page in detailed view

*   Jira Agile screen


<img src='/wp-content/uploads/gij-gitcloud-git-integration-panel.png' style='margin:25px auto;max-width:100%;display:block;' />

The 24 commits counter refers to an existing Git Commits view, which the issue tab have now.

### Branches list

This section displays the list of created branches that are associated to this Jira issue. The ahead and behind counters describes how much lines of code the branch is ahead or behind.

To the right are the deep link icons: (1) opens this branch in the git host service portal, (2) opens this branch in GitKraken git client app, and (3) opens this branch in GitLens VSCode extension.

### Pull/merge Request list

This section displays the list of created pull or merge requests that are associated to this Jira issue. Click the PR/MR links to view the selected PR/MR in the git host service portal.

&nbsp;
* * *

[**Prev:** Jira issue page](/git-integration-for-jira-cloud/jira-issue-page-gij-cloud)

[**Next:** Development panel locations](/git-integration-for-jira-cloud/development-panel-locations-gij-cloud)

