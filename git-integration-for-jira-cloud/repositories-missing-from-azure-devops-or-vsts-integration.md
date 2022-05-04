---

title: Repositories missing from Azure DevOps (or VSTS) integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Repositories missing from Azure DevOps (or VSTS) integration

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/421462017/Repositories+missing+from+Azure+DevOps+%28or+VSTS%29+integration>

* * *

## Problem

Some or all repositories in Azure DevOps (or Visual Studio Team Services - VSTS) integrations are not showing or seen by the integration user.

## Diagnoses

|     |
| --- |
| **1\. Permissions** |
| The connecting Azure DevOps user must have access to the repository to be added to the Git Integration for Jira app. |
| **2\. Access Level** |
| Jira admins will notice that some repositories expected in the Azure DevOps integration do not appear in the Git Integration for Jira app.  `Basic` or `Visual Studio Professional` access is the minimum access level necessary for the Git Integration for Jira app as **Code** access level is required.<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/421462017/azure-devops-code-access-level.png?version=1&modificationDate=1586316011297&cacheVersion=1&api=v2&width=680&height=212)<br><br>For more information - see Microsoft's article on [Azure DevOps Access Levels.](https://docs.microsoft.com/en-us/azure/devops/organizations/security/access-levels?view=azure-devops) |
| **3\. Repository format** |
| Only git format repositories are supported by the Git Integration for Jira app.  Team Foundation Version Control (TFVC) formatted repositories are not supported. |

## Solutions

|     |
| --- |
| **1\. Permissions** |
| Assign the connecting Azure DevOps user appropriate access to the repository or repositories. |
| **2\. Access level** |
| Grant at least `Basic` or `Visual Studio Professional` access is the minimum access level necessary for the Git Integration for Jira app. |
| **3\. Repository format** |
| Convert the Team Foundation Version Control (TFVC) formatted repositories to git format repositories<br><br>*   Microsoft article: [**Migrate from TFVC to Git**](https://docs.microsoft.com/en-us/devops/develop/git/migrate-from-tfvc-to-git)<br>    <br>*   Microsoft article: [**Import repositories from TFVC to Git**](https://docs.microsoft.com/en-us/azure/devops/repos/git/import-from-tfvc?view=azure-devops) |

## Workarounds

See the following of the articles:

[OAuth connection error or error 401 page with Azure DevOps integration](/wiki/spaces/GITCLOUD/pages/420282493/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+integration)

[OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/wiki/spaces/GITCLOUD/pages/421527629/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+with+Active+Directory+integration)

[I'm seeing a blank list of repositories after integration of Azure Repos](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/421298248/I+m+seeing+a+blank+list+of+repositories+after+integration+of+Azure+Repos)

**Contact Us**  
If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).

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