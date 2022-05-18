---

title: Empty list of repositories after integration of Azure Repos
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Problem

After integrating Azure DevOps to Jira, the Tracked Folder/Repositories dialog displays an empty list of repositories.

## Diagnosis

The integration status is UPDATED but users will see a blank list when performing ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Actions** > **Show integration repositories** in the Git Integration app manage repository configuration list.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/421298248/azure-no-repo-view-repos-cloud.png?version=1&modificationDate=1586356225011&cacheVersion=1&api=v2&width=557&height=345)

## Solution

If the integration is using the oAuth access, switch to personal access token instead.

If the problem still persists:

1.  Follow the solutions outlined in the following articles:

    1.  [OAuth connection error or error 401 page with Azure DevOps integration](/wiki/spaces/GITCLOUD/pages/420282493/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+integration)

    2.  [OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/wiki/spaces/GITCLOUD/pages/421527629/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+with+Active+Directory+integration)

2.  Configure [Creating Personal Access Tokens](/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens#CreatingPersonalAccessTokens-AzureDevOps|VisualStudioTeamServices(VSTS)).


## Related articles

*   Page:

    [Why don't I see commits? (Git Integration for Cloud)](/wiki/spaces/GITCLOUD/pages/110755841) (Git Integration for Jira Cloud)

*   Page:

    [Repositories missing from Azure DevOps (or VSTS) integration](/wiki/spaces/GITCLOUD/pages/421462017/Repositories+missing+from+Azure+DevOps+%28or+VSTS%29+integration) (Git Integration for Jira Cloud)

*   Page:

    [Licensing error - installCheck failed](/wiki/spaces/GITCLOUD/pages/420282445/Licensing+error+-+installCheck+failed) (Git Integration for Jira Cloud)

*   Page:

    [Why don't I see the Create branch or pull request features?](/wiki/spaces/GITCLOUD/pages/421593107) (Git Integration for Jira Cloud)

*   Page:

    [Connection error for self-hosted git servers](/wiki/spaces/GITCLOUD/pages/419659840/Connection+error+for+self-hosted+git+servers) (Git Integration for Jira Cloud)

*   Page:

    [SSH key file format is invalid](/wiki/spaces/GITCLOUD/pages/421363756/SSH+key+file+format+is+invalid) (Git Integration for Jira Cloud)

*   Page:

    [Error while reindexing - Java heap space / Object too large, rejecting the pack](/wiki/spaces/GITCLOUD/pages/421462043) (Git Integration for Jira Cloud)

*   Page:

    [OAuth connection error or error 401 page with Azure DevOps integration](/wiki/spaces/GITCLOUD/pages/420282493/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+integration) (Git Integration for Jira Cloud)

*   Page:

    [OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/wiki/spaces/GITCLOUD/pages/421527629/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+with+Active+Directory+integration) (Git Integration for Jira Cloud)

*   Page:

    [Empty list of repositories after integration of Azure Repos](/wiki/spaces/GITCLOUD/pages/421298248/Empty+list+of+repositories+after+integration+of+Azure+Repos) (Git Integration for Jira Cloud)