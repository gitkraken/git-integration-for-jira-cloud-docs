---

title: Adding webhooks for Azure DevOps Repos | VSTS
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Pull request webhooks are now supported.  [See details](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/172294150/Adding+webhooks+for+Azure+DevOps+Repos+%7C+VSTS#Pull-request-webhooks) on this page.

Supported webhook events:

*   Code pushed

*   Pull request created

*   Pull request updated

*   Pull request merge attempted


_Right click_ [_here_](https://bigbrassband.wistia.net/medias/61wl72vp91) _to open this video in a new tab/window for more viewing options._

Before you can proceed with the steps outlined on this guide, indexing triggers must be enabled in the Git Integration for Jira app repository configuration for your Jira Cloud instance. For more details, see [**Indexing Triggers - Getting Started**](/git-integration-for-jira-cloud/Indexing-Triggers).

## Setting up webhook for Azure Repos

Configure webhook by logging in to your VSTS/Azure DevOps account.

1.  Open a project by clicking on it.

2.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/172294150/webhooks-azure-devops-sel-proj(c).png?version=1&modificationDate=1617193372470&cacheVersion=1&api=v2&width=646&height=361)

    Click ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Project Settings** then select **Service Hooks**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/172294150/webhooks-azure-devops-add-shooks(c).png?version=1&modificationDate=1617193372476&cacheVersion=1&api=v2&width=544&height=233)
3.  Click ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) to add a new service hook subscription.

4.  Scroll to **Web Hooks** and click to select it.

5.  Click **Next**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/172294150/webhooks-azure-devops-triggers-cfg(c).png?version=1&modificationDate=1617193372478&cacheVersion=1&api=v2&width=476&height=499)
    1.  Set **"code pushed"** for the _**Trigger on this type of event**_ selector.

    2.  Set all **FILTERS** to **"Any"**.

    3.  Click **Next** to proceed to the following screen.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/172294150/webhooks-azure-devops-action-cfg(c).png?version=1&modificationDate=1617193372481&cacheVersion=1&api=v2&width=510&height=535)
6.  Switch to your Jira instance then navigate to **Manage Git repositories** page and then click **Indexing triggers** (_or alternatively go to Jira Settings ➜ Apps. On the sidebar, click Indexing triggers_).

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/172294150/jira-cloud-webhook-url-loc(c1).png?version=1&modificationDate=1617193372483&cacheVersion=1&api=v2&width=646&height=430)
7.  Copy the complete secret key URL by clicking the copy icon on the right.

8.  Switch back to VSTS/Azure DevOps (where you left off) and paste this information into the provided **URL** box.

9.  Click **Test** to verify if webhook integration is successful or not.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/172294150/webhooks-azure-devops-test-cfg(c).png?version=1&modificationDate=1617193372485&cacheVersion=1&api=v2&width=578&height=408)
10.  Click **Finish** to complete this setup.

11.  Repeat the above steps for **Pull request created** and **Pull request updated** webhooks.


## Pull request webhooks

The Git Integration for Jira app supports pull request webhooks now.

You will need to have three (3) separate service hooks configuration for it to work properly. Aside from setting up the "**Code pushed**" service hook outlined above in step **6.a**, perform the same process with _**Pull request created**_ and _**Pull request updated**_ for the triggers.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/172294150/azure-devops-server-2019-req-service-hooks.png?version=2&modificationDate=1617193372488&cacheVersion=1&api=v2&width=680&height=239)