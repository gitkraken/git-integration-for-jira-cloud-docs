---

title: OAuth connection error or error 401 page with Azure DevOps integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# OAuth connection error or error 401 page with Azure DevOps integration

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/420282493/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+integration>

* * *

## Problem

You are getting the OAuth connection error or a 401 web page error is displayed when integrating Azure DevOps.

## Diagnosis

These issues are related to the security settings in your Azure DevOps portal where certain security policies are rejecting connections to Git Integration for Jira app.

## Cause

On most cases, this is caused by an OAuth setting being turned OFF.

## Solution

Git Integration for Jira Cloud requires Git admins to allow the third-party app access OAuth security policy in their organization settings:

1.  On your VSTS/Azure DevOps portal, go to the home page.
    
2.  Click an organization then go to **Organization Settings** (sidebar).
    
3.  Under _**Security**_, click **Policies**.
    
4.  Ensure that the **Third-party application access via OAuth** option is set to ON.
    

![](https://bigbrassband.atlassian.net/wiki/download/attachments/420282493/vsts-azure-devops-org-cfg-policy-oauth.png?version=1&modificationDate=1586320251412&cacheVersion=1&api=v2)

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