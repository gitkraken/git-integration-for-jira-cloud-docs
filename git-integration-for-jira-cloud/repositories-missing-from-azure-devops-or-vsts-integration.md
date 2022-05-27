---

title: Repositories missing from Azure DevOps (or VSTS) integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
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

[OAuth connection error or error 401 page with Azure DevOps integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-integration/)

[OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration/)

[I'm seeing a blank list of repositories after integration of Azure Repos](/git-integration-for-jira-cloud/empty-list-of-repositories-after-integration-of-azure-repos/)

**Contact Us**
If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).
