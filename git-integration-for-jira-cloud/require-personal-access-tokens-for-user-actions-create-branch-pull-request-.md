---

title: Require Personal Access Tokens for user actions (create branch/pull request)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Background

The Git Integration for Jira app allows users of integrations (examples: GitLab, GitHub, etc) to create branches and pull requests from within the Jira issue. By default the operation will be performed by the integration user that is used for indexing.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/131137621/Screen%20Shot%202019-05-10%20at%2015.35.55.png?version=1&modificationDate=1557516971061&cacheVersion=1&api=v2&width=680&height=352)

## Objective

For teams looking to maintain user attribution - Jira administrators can require that individual Jira users provide personal access tokens to perform actions (like creating a branch or pull request in Jira using their git service account - rather than the integration account).

### Supported integrations

User attribution is supported in the following special integrations in Git Integration for Jira Cloud:

*   GitHub.com

*   GitHub Enterprise

*   GitLab.com

*   GitLab self-managed

*   Microsoft Azure DevOps

*   Microsoft Visual Studio Team Services (VSTS)

*   Microsoft Team Foundation Server (TFS)

*   AWS CodeCommit


## Instructions

To enable/disable the _Require User PAT_ setting for all repositories within an integration:

1.  Navigate to **Manage Git repositories**.

2.  Add a new integration or edit existing integration's settings.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/131137621/req-pat-gitmgr-page-actions-edit-git-settings(c).png?version=1&modificationDate=1599487860595&cacheVersion=1&api=v2)
3.  Locate the **Require User PAT** setting.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/131137621/req-pat-gitmgr-page-actions-control-cfg(c).png?version=1&modificationDate=1599488140039&cacheVersion=1&api=v2)
4.  Check the box to require PAT option.

5.  Click **Update.**


## What will Jira users see?

1.  Once the Jira administrator requires Personal Access Tokens - your Jira users will be presented with a message that setup is required.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/131137621/Screen%20Shot%202019-05-10%20at%2015.39.24.png?version=1&modificationDate=1557517178591&cacheVersion=1&api=v2)

2.  Following that link - the user is taken to a prompt in the **View all repositories** screen to enter their Personal Access Token (PAT) for the service (GitHub, GitLab, etc).
    [Instructions: Creating Personal Access Tokens](/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens)

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/131137621/Screen%20Shot%202019-05-10%20at%2015.40.18.png?version=1&modificationDate=1557517242825&cacheVersion=1&api=v2)

3.  With the Personal Access Token saved - the user will now see the following:

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/131137621/Screen%20Shot%202019-05-10%20at%2015.42.54.png?version=1&modificationDate=1557517392933&cacheVersion=1&api=v2&width=652&height=390)

PATs were introduced with TFS 2017 and newer.  TFS 2013 and TFS 2015 do not support PATs.  If the repository setting **Require User PAT** property is set to `ON`, the users will not be able to create/delete branches and pull requests.

Personal Access Tokens are saved per integration by individual Jira users app. Examples shown above are for the Create branch action; Create pull request is the same. The same token is used for Create branch and Create pull request.

Jira users must have the **View Development Tools** permission in the context of a Jira project to view content from the Git Integration for Jira app.


_1 Logo owned by_ [_GitLab Inc_](https://gitlab.com/) _used under_ [_license_](https://creativecommons.org/licenses/by-nc-sa/4.0/)