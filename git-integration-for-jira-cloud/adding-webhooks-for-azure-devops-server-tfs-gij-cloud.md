---

title: Adding webhooks for Azure DevOps Server | TFS
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Pull request webhooks are now supported. <a href='/git-integration-for-jira-cloud/adding-webhooks-for-azure-devops-server-tfs-gij-cloud'>See details</a> on this page.<br>
        <p>Supported webhook events:</p>
        <ul>
            <li>Code pushed</li>
            <li>Pull request created</li>
            <li>Pull request updated</li>
            <li>Pull request merge attempted</li>
        </ul>
    </div>
    </div>
</div>
<br>

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/61wl72vp91?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/v2c5qrgps8'><b>here</b></a> to open this video in a new browser tab for more viewing options. (While the above video showcases VSTS/Azure DevOps, the entire process is entirely the same for Azure Repos webhooks setup.)</i>
</div>
<br>

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before you can proceed with the steps outlined on this guide, webhooks must be enabled in the Git Integration for Jira app repository configuration for your Jira instance. For more details, see <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud/'><b>Indexing triggers - Getting Started</b></a>.
    </div>
    </div>
</div>
<br>

## Setting up webhooks for Azure DevOps Server | TFS

Configure webhook by logging in to your Azure DevOps Server/TFS account.

1.  Open a project by clicking on it.

2.  Click **Project Settings** (sidebar) then select **Service Hooks**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/webhooks-azure-devops-add-shooks(c).png?version=1&modificationDate=1617193805282&cacheVersion=1&api=v2&width=544&height=233)

    Click the + Icon to add a new service hook subscription.

3.  Scroll to **Web Hooks** and click to select it.

4.  Click **Next**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/webhooks-azure-devops-triggers-cfg(c).png?version=1&modificationDate=1617193805288&cacheVersion=1&api=v2&width=476&height=499)

    *   Set **"code pushed"** for the _**Trigger on this type of event**_ selector.

    *   Set all **FILTERS** to **"Any"**.

    *   Click **Next** to proceed to the following screen.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/webhooks-azure-devops-action-cfg(c).png?version=1&modificationDate=1617193805292&cacheVersion=1&api=v2&width=516&height=541)

5.  Switch to your Jira instance then navigate to **Manage Git repositories** page and then click **Indexing triggers** (_or alternatively go to Jira Settings ➜ Apps. On the sidebar, click Indexing triggers_).

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/jira-cloud-webhook-url-loc(c1).png?version=1&modificationDate=1617193805295&cacheVersion=1&api=v2&width=646&height=430)

    Copy the complete secret key URL using the copy icon on the right.

6.  Switch back to Azure DevOps Server/TFS (where you left off) and paste this information into the provided **URL** box.

7.  Click **Test** to verify if webhook integration is successful or not.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/webhooks-azure-devops-test-cfg(c).png?version=1&modificationDate=1617193805298&cacheVersion=1&api=v2&width=584&height=413)

    Click **Finish** to complete this setup.

<br>

## Pull request webhooks

The Git Integration for Jira app supports pull request webhooks now.

You will need to have three (3) separate service hooks configuration for it to work properly. Aside from setting up the "**Code pushed**" service hook outlined above in step **6.a**, perform the same process with _**Pull request created**_ and _**Pull request updated**_ for the triggers.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/234782736/azure-devops-server-2019-req-service-hooks.png?version=2&modificationDate=1617193805302&cacheVersion=1&api=v2&width=680&height=239)

