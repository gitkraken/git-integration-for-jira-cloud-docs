---

title: Jira Git integration development panel
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
This page applies to Jira Server, Jira Data Center and Jira Cloud.

## Permissions

|     |
| --- |
| **Jira Cloud - Development panel** |
| The **View Development Tools** _permission_ only applies to Jira Classic Projects. Next-Gen Projects don't allow to modify the permission. |
| **Create Branches and Branch Names** |
| For connected GitHub git host, this feature requires enabled `public_repo` scope permissions. |
| **Commits Ahead and Behind** |
| If the user does not have the **View Development Tools** _project permission_ for the project, the developer panel will be unavailable for that user. |

## Getting started

Git links are now available on the developer panel in the following locations:

*   Issue page

*   Search page in detailed view

*   Jira Agile screen


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025809/gitcloud-git-integration-panel.png?version=1&modificationDate=1635751417005&cacheVersion=1&api=v2&width=340&height=346)

The 23 commits refers to an existing Git Commits view, which the issue tab have now. Clicking this text link will reload the page and automatically selects the **Git Commits** tab to view the commits.

The Roll Up refers to an existing **Git Roll Up** view, which the issue tab have now. Clicking this link will reload the page and automatically selects the Git Roll Up tab to view the git code summary.

## Branches list

This section displays the list of created branches that are associated to this Jira issue. The ahead and behind counters describes how much lines of code the branch is ahead or behind.

To the right are the deep link icons: (1) opens this branch in the git host service portal, and (2) opens this branch in GitKraken git client app.

## Pull/merge Request list

This section displays the list of created pull or merge requests that are associated to this Jira issue. Click the PR/MR links to view the selected PR/MR in the git host service portal.

[« Jira issue page](/wiki/spaces/GITCLOUD/pages/1923025695/Jira+issue+page)

[Development panel locations »](/wiki/spaces/GITCLOUD/pages/1923025834/Development+panel+locations)

### More related topics about Jira developer panel

*   Page:

    [Jira Git integration development panel](/wiki/spaces/GITCLOUD/pages/1923025809/Jira+Git+integration+development+panel) (Git Integration for Jira Cloud)

*   Page:

    [Development panel locations](/wiki/spaces/GITCLOUD/pages/1923025834/Development+panel+locations) (Git Integration for Jira Cloud)

*   Page:

    [Branches (Development panel)](/wiki/spaces/GITCLOUD/pages/1923025879) (Git Integration for Jira Cloud)

*   Page:

    [Pull or merge requests (Development panel)](/wiki/spaces/GITCLOUD/pages/1923025925) (Git Integration for Jira Cloud)

*   Page:

    [Git tags](/wiki/spaces/GITCLOUD/pages/1923025983/Git+tags) (Git Integration for Jira Cloud)