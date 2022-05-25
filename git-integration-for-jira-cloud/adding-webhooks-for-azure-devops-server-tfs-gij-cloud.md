---

title: Adding webhooks for Azure DevOps Server | TFS
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Pull request webhooks are now supported. [See details](/git-integration-for-jira-cloud/adding-webhooks-for-azure-devops-server-tfs/) on this page.

Supported webhook events:

*   Code pushed

*   Pull request created

*   Pull request updated

*   Pull request merge attempted


_Right-click_ [_here_](https://bigbrassband.wistia.com/medias/61wl72vp91) _and view this video in a new browser tab. (While the above video showcases VSTS/Azure DevOps, the entire process is entirely the same for Azure Repos webhooks setup.)_

Before you can proceed with the steps outlined on this guide, webhooks must be enabled in the Git Integration for Jira app repository configuration for your Jira instance. For more details, see [**Indexing triggers - Getting Started**](/git-integration-for-jira-cloud/Indexing-Triggers).

## Setting up webhooks for Azure DevOps Server | TFS

Configure webhook by logging in to your Azure DevOps Server/TFS account.

1.  Open a project by clicking on it.

2.  Click ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Project Settings** (sidebar) then select **Service Hooks**. The following screen is displayed.

3.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/webhooks-azure-devops-add-shooks(c).png?version=1&modificationDate=1617193805282&cacheVersion=1&api=v2&width=544&height=233)

    Click ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) to add a new service hook subscription.

4.  Scroll to **Web Hooks** and click to select it.

5.  Click **Next**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/webhooks-azure-devops-triggers-cfg(c).png?version=1&modificationDate=1617193805288&cacheVersion=1&api=v2&width=476&height=499)
    1.  Set **"code pushed"** for the _**Trigger on this type of event**_ selector.

    2.  Set all **FILTERS** to **"Any"**.

    3.  Click **Next** to proceed to the following screen.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/webhooks-azure-devops-action-cfg(c).png?version=1&modificationDate=1617193805292&cacheVersion=1&api=v2&width=516&height=541)
6.  Switch to your Jira instance then navigate to **Manage Git repositories** page and then click **Indexing triggers** (_or alternatively go to Jira Settings ➜ Apps. On the sidebar, click Indexing triggers_).

7.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/jira-cloud-webhook-url-loc(c1).png?version=1&modificationDate=1617193805295&cacheVersion=1&api=v2&width=646&height=430)

    Copy the complete secret key URL using the copy icon on the right.

8.  Switch back to Azure DevOps Server/TFS (where you left off) and paste this information into the provided **URL** box.

9.  Click **Test** to verify if webhook integration is successful or not.

10.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/webhooks-azure-devops-test-cfg(c).png?version=1&modificationDate=1617193805298&cacheVersion=1&api=v2&width=584&height=413)

    Click **Finish** to complete this setup.


## Pull request webhooks

The Git Integration for Jira app supports pull request webhooks now.

You will need to have three (3) separate service hooks configuration for it to work properly. Aside from setting up the "**Code pushed**" service hook outlined above in step **6.a**, perform the same process with _**Pull request created**_ and _**Pull request updated**_ for the triggers.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/azure-devops-server-2019-req-service-hooks.png?version=2&modificationDate=1617193805302&cacheVersion=1&api=v2&width=680&height=239)