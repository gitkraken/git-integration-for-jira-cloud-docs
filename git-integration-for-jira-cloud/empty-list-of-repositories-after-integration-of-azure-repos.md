---

title: Empty list of repositories after integration of Azure Repos
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Problem

After integrating Azure DevOps to Jira, the Tracked Folder/Repositories dialog displays an empty list of repositories.

## Diagnosis

The integration status is UPDATED but users will see a blank list when performing ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Actions** > **Show integration repositories** in the Git Integration app manage repository configuration list.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/421298248/azure-no-repo-view-repos-cloud.png?version=1&modificationDate=1586356225011&cacheVersion=1&api=v2&width=557&height=345)

## Solution

If the integration is using the oAuth access, switch to personal access token instead.

If the problem still persists:

1.  Follow the solutions outlined in the following articles:

    1.  [OAuth connection error or error 401 page with Azure DevOps integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-integration/)

    2.  [OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration/)

2.  Configure [Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens/)).

