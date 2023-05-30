---

title: Repositories missing from Azure DevOps (or VSTS) integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

## Problem

Some or all repositories in Azure DevOps (or Visual Studio Team Services - VSTS) integrations are not showing or seen by the integration user.

&nbsp;

## Diagnoses

**1\. Permissions**

The connecting Azure DevOps user must have access to the repository to be added to the Git Integration for Jira app.

**2\. Access Level**

Jira admins will notice that some repositories expected in the Azure DevOps integration do not appear in the Git Integration for Jira app.  `Basic` or `Visual Studio Professional` access is the minimum access level necessary for the Git Integration for Jira app as **Code** access level is required.

![](/wp-content/uploads/gij-azure-devops-code-access-level.png)

For more information - see Microsoft's article on [Azure DevOps Access Levels.](https://docs.microsoft.com/en-us/azure/devops/organizations/security/access-levels?view=azure-devops)

**3\. Repository format**

Only git format repositories are supported by the Git Integration for Jira app. Team Foundation Version Control (TFVC) formatted repositories are not supported.

&nbsp;

## Solutions

**1\. Permissions**

Assign the connecting Azure DevOps user appropriate access to the repository or repositories.

**2\. Access level**

 Grant at least `Basic` or `Visual Studio Professional` access is the minimum access level necessary for the Git Integration for Jira app.

**3\. Repository format**

Convert the Team Foundation Version Control (TFVC) formatted repositories to git format repositories

*   Microsoft article: [**Migrate from TFVC to Git**](https://docs.microsoft.com/en-us/devops/develop/git/migrate-from-tfvc-to-git)

*   Microsoft article: [**Import repositories from TFVC to Git**](https://docs.microsoft.com/en-us/azure/devops/repos/git/import-from-tfvc?view=azure-devops)

&nbsp;

## Workarounds

See the following articles:

[OAuth connection error or error 401 page with Azure DevOps integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-integration-gij-cloud)

[OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration-gij-cloud)

[I'm seeing a blank list of repositories after integration of Azure Repos](/git-integration-for-jira-cloud/empty-list-of-repositories-after-integration-of-azure-repos-gij-cloud)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

## Related articles

[Why don't I see commits? (Git Integration for Cloud)](/git-integration-for-jira-cloud/why-dont-i-see-commits-git-integration-for-cloud-gij-cloud) (Git Integration for Jira Cloud)

[Repositories missing from Azure DevOps (or VSTS) integration](/git-integration-for-jira-cloud/repositories-missing-from-azure-devops-or-vsts-integration-gij-cloud) (Git Integration for Jira Cloud)

[Licensing error - installCheck failed](/git-integration-for-jira-cloud/licensing-error-installcheck-failed-gij-cloud) (Git Integration for Jira Cloud)

[Why don't I see the Create branch or pull request features?](/git-integration-for-jira-cloud/why-dont-i-see-the-create-branch-or-pull-request-features-gij-cloud) (Git Integration for Jira Cloud)

[Connection error for self-hosted git servers](/git-integration-for-jira-cloud/connection-error-for-self-hosted-git-servers-gij-cloud) (Git Integration for Jira Cloud)

[SSH key file format is invalid](/git-integration-for-jira-cloud/ssh-key-file-format-is-invalid-gij-cloud) (Git Integration for Jira Cloud)

[Error while reindexing - Java heap space / Object too large, rejecting the pack](/git-integration-for-jira-cloud/error-while-reindexing-java-heap-space-object-too-large-rejecting-the-pack-gij-cloud) (Git Integration for Jira Cloud)

[OAuth connection error or error 401 page with Azure DevOps integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-integration-gij-cloud) (Git Integration for Jira Cloud)

[OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration-gij-cloud) (Git Integration for Jira Cloud)

[Empty list of repositories after integration of Azure Repos](/git-integration-for-jira-cloud/empty-list-of-repositories-after-integration-of-azure-repos-gij-cloud) (Git Integration for Jira Cloud)

[Reconnecting Azure DevOps and VSTS OAuth integrations](/git-integration-for-jira-cloud/reconnecting-azure-devops-and-vsts-oauth-integrations-gij-cloud)

