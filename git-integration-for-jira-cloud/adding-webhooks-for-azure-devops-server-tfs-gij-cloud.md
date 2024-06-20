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
        Pull request webhooks are now supported. <a href='/git-integration-for-jira-cloud/adding-webhooks-for-azure-devops-server-tfs-gij-cloud'>See details</a> on this page.<br>
        <p>Supported webhook events:</p>
        <ul style='margin-bottom:0px;'>
            <li>Code pushed</li>
            <li>Pull request created</li>
            <li>Pull request updated</li>
            <li>Pull request merge attempted</li>
        </ul>
    </div>
    </div>
</div>

&nbsp;

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/61wl72vp91?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:12px;margin-bottom:30px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/61wl72vp91'><b>here</b></a> to open this video in a new browser tab for more viewing options. (While the above video showcases VSTS/Azure DevOps, the entire process is entirely the same for Azure Repos webhooks setup.)</i>
</div>

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before you can proceed with the steps outlined on this guide, webhooks must be enabled in the Git Integration for Jira app repository configuration for your Jira instance. For more details, see <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'><b>Indexing triggers - Getting Started</b></a>.
    </div>
    </div>
</div>

&nbsp;

Configure webhook by logging in to your VSTS/Azure DevOps account:

1.  Open a project by clicking on it.

    ![](/wp-content/uploads/gij-webhooks-azure-devops-sel-proj-c.png)

2.  On the sidebar, click **Project Settings** then select **Service Hooks**. The following screen is displayed.

    ![](/wp-content/uploads/gij-cloud-TFS-create-add-new-subscription-c.png)

3.  Click **Create subscription** to add a new service hook subscription.

4.  Scroll down to **Web Hooks** and click to select it.

5.  Click **Next**. The following screen is displayed.

    ![](/wp-content/uploads/gij-webhooks-azure-devops-triggers-cfg-c.png)

    a. Set **"code pushed"** for the _**Trigger on this type of event**_ selector.

    b. Set all **FILTERS** to _**Any**_.

    c. Click **Next** to proceed to the following screen.

    ![](/wp-content/uploads/gij-webhooks-azure-devops-action-cfg-c.png)

6.  Switch to your Jira Cloud instance and navigate to Apps ➜ **Git Integration: Manage integrations** then click **Indexing triggers** on the sidebar.

    ![](/wp-content/uploads/gij-gitcloud-gitmgr-indexing-triggers-url-link-loc.png)

7.  Copy the complete webhook URL by clicking the copy icon on the right (4).

8.  Switch back to VSTS/Azure DevOps portal (where you left off):

    ![](/wp-content/uploads/gij-cloud-TFS-action-settings-header-etc-c.png)

    a. Paste the webhook URL into the Settings **URL** field.

    b. For the **HTTP header**, enter `X-GIJ-Microsoft-Event:1`. This header will improve webhook processing efficiency since we are only expecting specific MS events.

    c. Set <u>Resource details to send</u> to _**All**_.

    d. Set <u>Messages to send</u> to _**None**_.

    e. Set <u>Detailed messages to send</u> to _**None**_.

    The settings **8.d** and **8.e** limits the data transfered to your Jira instance since too much webhook traffic can degrade Jira performance.

9.  Click **Test** to verify if webhook integration is successful or not.

    ![](/wp-content/uploads/gij-cloud-TFS-webook-test-verify-c.png)

10.  Click **Finish** to complete this setup.

11.  Repeat the above steps for **Pull request created** and **Pull request updated** webhooks.

![](/wp-content/uploads/gij-cloud-TFS-webhook-idx-trigger-complete-c.png)

&nbsp;

### Pull request webhooks

The Git Integration for Jira app supports pull request webhooks now.

You will need to have three (3) separate service hooks configuration for it to work properly. Aside from setting up the "**Code pushed**" service hook outlined above in step **5.a**, perform the same process with _**Pull request created**_ and _**Pull request updated**_ for the triggers.

<img src='/wp-content/uploads/gij-cloud-TFS-webhook-service-hook-list-c.png' style='margin:25px auto;max-width: 100%;display:block;' />

