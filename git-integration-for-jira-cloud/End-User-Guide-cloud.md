---

title: End User Guide - GIJ Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Introduction to GIJ
Thank you for using Git Integration for Jira! First, let’s go over how information will be displayed in Jira through our application.

## Jira Issue View

GIJ will display commits, branches, and pull/merge requests associated with a specific Jira issue. The Jira issue key must be included in the commit message, the branch name, and the pull/merge request title in order for GIJ to link the item to the respective Jira issue.

![Jira Issue View](/wp-content/uploads/Jira-Issue-Breakdown.png)
Breakdown of information provided by GIJ in Jira issues:
### Git Commits Tab
1. Git Commits tab in the activity stream, broken down by repository
2. Individual Commit, noted by Developer that made the commit
3. Commit message
4. Commit line change summary by file
5. Link to view Code diff in Jira
### Git Integration Panel
6. Commit Count
7. Option to Create a branch directly from a Jira Issue. Associated Branches with change comparison count to main repository branch
8. Option to Create a Pull/Merge request directly from a Jira Issue. Associated Pull/Merge Requests with status

Additionally, the [Git Rollup tab](https://help.gitkraken.com/git-integration-for-jira-cloud/git-roll-up-tab-gij-cloud/) allows you to see a summary of the files, lines and the developers who have made the changes associated with the Jira issue.
![Git Rollup Tab](/wp-content/uploads/gij-gitcloud-jira-issue-rollup-tab.png)

## Linking Behavior

GIJ uses the Jira issue key to determine whether or not a repository activity (Commits, Branches, Pull/Merge Requests) is linked to any Jira items. In order for the linking to occur, you need to include the Jira issue key in the commit message, the branch name, and the pull request title. It does not need to be in any specific part of the message or name as long as it is included. Please see: [Linking Git Commits to Jira Issues](https://help.gitkraken.com/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud/) for more details.

![Jira Issue Key](/wp-content/uploads/Jira-Issue-key-linking-cloud.png)

![Commit Example](/wp-content/uploads/Linking-Commit-example.png)

![Pull request Example](/wp-content/uploads/Pull-Request-Linking-Example.png)

## Creating Branches
You can [create branches](https://help.gitkraken.com/git-integration-for-jira-cloud/create-branch-gij-cloud/) directly from a Jira issue using GIJ. To do this, first open and load the ‘Git Integration’ panel from the right hand side of the Jira issue, then click the ‘Create branch’ option.

![Create Branch 1](/wp-content/uploads/Enduserguide-Cloud-Create-Branch-1.png)

Select the desired repository to create the branch in, the source branch, and the branch name. Make sure that the Jira issue key is included in the branch name.

![Create Branch 2](/wp-content/uploads/Enduserguide-Cloud-Create-Branch-2.png)

You will see a pop up after the branch is created, and you will be able to link our directly to the newly created branch.

## Creating Pull/Merge Requests
You can [create Pull/Merge Requests](https://help.gitkraken.com/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud/) directly from Jira using GIJ as well. To do this, first open and load the ‘Git Integration’ panel from the right hand side of the Jira issue, then click the ‘Create Pull Request/Merge Request’.

![Create PR 1](/wp-content/uploads/Enduserguide-Cloud-Creating-PR-1.png)
Select the repository, Source and Target branches, and make sure that the title of the pull request contains the Jira issue key, and click the ‘Create pull/merge request’ button.

![Create PR 2](/wp-content/uploads/Enduserguide-Cloud-Creating-PR-2.png)
You will see a pop up after the branch is created, and you will be able to link our directly to the newly created branch.

## GIJ User Settings
GIJ let’s you manage your Connected Apps, Default Repository, Branch, and Personal Access Tokens through the [GIJ User settings](https://help.gitkraken.com/git-integration-for-jira-cloud/user-settings-gij-cloud/) page. 

To navigate to this page, click your Jira profile picture icon, then select ‘Git Integration: User Settings’.
![User-Settings](/wp-content/uploads/GIJ-General-Settings-navigation-cloud.png)
### Connected Apps
You can enabled/disable the visbility of the the Gitkraken and Gitlens icons in Jira issues which allow you to open specific Git items in the respective application directly from the issue.

![Connected Apps](/wp-content/uploads/GIJ-Cloud-User-Settings-Connnected-Apps.png)

![Connected Apps - icons](/wp-content/uploads/GIJ-Connected-Apps-Jiraissue-icons.png)

### Default Repository
You can set a default repository on a per project basis.

![Default-repo](/wp-content/uploads/GIJ-Cloud-User-Settings-Default-Repo.png)

### Default Branch
You can set a default branch for a specific repository, set up dependent on the Jira Project.

![Default-Branch](/wp-content/uploads/GIJ-Cloud-User-Settings-Default-Branch.png)

### Personal Access Tokens
You can manage the Personal access tokens that will be used to authenticate your requests to create Branches and Pull Requests directly from Jira. You will need to provide a token for each integration. You can both provide the Personal Access Token and click the link to create a new token, which will take you directly to the token creation page for the given Git service. Please see [Creating Personal Access Tokens](https://help.gitkraken.com/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud/) for detailed instructions for creating your PAT.

![PAT](/wp-content/uploads/GIJ-Cloud-User-Settings-PAT.png)
