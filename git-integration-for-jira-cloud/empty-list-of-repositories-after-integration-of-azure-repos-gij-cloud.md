---

title: Empty list of repositories after integration of Azure Repos
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Problem

After integrating Azure DevOps to Jira, the Tracked Folder/Repositories dialog displays an empty list of repositories.

## Diagnosis

The integration status is UPDATED but users will see a blank list when performing **Actions** > **Show integration repositories** in the Git Integration app manage repository configuration list.

![](/wp-cotnent/uploads/gij-azure-no-repo-view-repos-cloud.png)

## Solution

If the integration is using the oAuth access, switch to personal access token instead.

If the problem still persists:

1.  Follow the solutions outlined in the following articles:

    *   [OAuth connection error or error 401 page with Azure DevOps integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-integration-gij-cloud)

    *   [OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration-gij-cloud)

2.  Configure [Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact us</b><br>
        If you still have a question - reach out to our <a href='https://bigbrassband.atlassian.net/servicedesk/customer/portals'>Support Desk</a> or email us at <a href='mailto:support@bigbrassband.com'>support@bigbrassband.com</a>.
    </div>
    </div>
</div>
<br>

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

**Empty list of repositories after integration of Azure Repos** (this page)

[Reconnecting Azure DevOps and VSTS OAuth integrations](/git-integration-for-jira-cloud/reconnecting-azure-devops-and-vsts-oauth-integrations-gij-cloud)