---

title: OAuth connection error or error 401 page with Azure DevOps with Active Directory integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Problem

You are getting the OAuth connection error or a 401 web page error is displayed when integrating with Azure DevOps connected to Active Directory.

## Diagnosis

These issues are related to the security settings in your Azure DevOps portal where certain security policies are rejecting connections to Git Integration for Jira app.

Moreover, for Azure Active Directory connections, the conditional access policy setting (when enabled) will force all untrusted location to require MFA in order to connect with Azure DevOps.

## Cause

For Azure DevOps with Active Directory connections, this is due to the conditional access security setting being enabled.

## Solution

Git Integration for Jira Cloud requires Git admins to allow the third-party app access OAuth security policy in their organization settings:

1.  On your VSTS/Azure DevOps portal, go to the home page.

2.  Click an organization then go to **Organization Settings** (sidebar).

3.  Under _**Security**_, click **Policies**.

4.  Ensure that the **Third-party application access via OAuth** option is set to ON.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/421527629/vsts-azure-devops-org-cfg-policy-oauth.png?version=1&modificationDate=1586320352768&cacheVersion=1&api=v2&width=680&height=178)

For projects connected with Azure Active Directory, the above requirement must also be enabled and set the conditional access policy validation to OFF:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/421527629/enable-conditional-access-policy-AD.png?version=1&modificationDate=1586320353218&cacheVersion=1&api=v2&width=510&height=146)

**Contact Us**

If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).
