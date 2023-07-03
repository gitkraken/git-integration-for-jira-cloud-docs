---

title: OAuth connection error or error 401 page with Azure DevOps integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

### Problem

You are getting the OAuth connection error or a 401 web page error is displayed when integrating Azure DevOps.

&nbsp;

### Diagnosis

These issues are related to the security settings in your Azure DevOps portal where certain security policies are rejecting connections to Git Integration for Jira app.

&nbsp;

### Cause

On most cases, this is caused by an OAuth setting being turned OFF.

&nbsp;

### Solution

Git Integration for Jira Cloud requires Git admins to allow the third-party app access OAuth security policy in their organization settings:

1.  On your VSTS/Azure DevOps portal, go to the home page.

2.  Click an organization then go to **Organization Settings** (sidebar).

3.  Under _**Security**_, click **Policies**.

4.  Ensure that the **Third-party application access via OAuth** option is set to ON.


![](/wp-content/uploads/gij-vsts-azure-devops-org-cfg-policy-oauth.png)


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

### Related articles

[Why don't I see commits? (Git Integration for Cloud)](/git-integration-for-jira-cloud/why-dont-i-see-commits-git-integration-for-cloud-gij-cloud) (Git Integration for Jira Cloud)

[Repositories missing from Azure DevOps (or VSTS) integration](/git-integration-for-jira-cloud/repositories-missing-from-azure-devops-or-vsts-integration-gij-cloud) (Git Integration for Jira Cloud)

[Licensing error - installCheck failed](/git-integration-for-jira-cloud/licensing-error-installcheck-failed-gij-cloud) (Git Integration for Jira Cloud)

[Why don't I see the Create branch or pull request features?](/git-integration-for-jira-cloud/why-dont-i-see-the-create-branch-or-pull-request-features-gij-cloud) (Git Integration for Jira Cloud)

[Connection error for self-hosted git servers](/git-integration-for-jira-cloud/connection-error-for-self-hosted-git-servers-gij-cloud) (Git Integration for Jira Cloud)

[SSH key file format is invalid](/git-integration-for-jira-cloud/ssh-key-file-format-is-invalid-gij-cloud) (Git Integration for Jira Cloud)

[Error while reindexing - Java heap space / Object too large, rejecting the pack](/git-integration-for-jira-cloud/error-while-reindexing-java-heap-space-object-too-large-rejecting-the-pack-gij-cloud) (Git Integration for Jira Cloud)

**OAuth connection error or error 401 page with Azure DevOps integration** (this page)

[OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration-gij-cloud) (Git Integration for Jira Cloud)

[Empty list of repositories after integration of Azure Repos](/git-integration-for-jira-cloud/empty-list-of-repositories-after-integration-of-azure-repos-gij-cloud) (Git Integration for Jira Cloud)

[Reconnecting Azure DevOps and VSTS OAuth integrations](/git-integration-for-jira-cloud/reconnecting-azure-devops-and-vsts-oauth-integrations-gij-cloud)

