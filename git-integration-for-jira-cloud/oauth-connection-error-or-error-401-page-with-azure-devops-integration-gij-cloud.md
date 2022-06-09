---

title: OAuth connection error or error 401 page with Azure DevOps integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
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

