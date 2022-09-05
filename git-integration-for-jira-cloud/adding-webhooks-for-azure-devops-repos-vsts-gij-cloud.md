---

title: Adding webhooks for Azure DevOps Repos | VSTS
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
        Pull request webhooks are now supported.  <a href='/git-integration-for-jira-cloud/adding-webhooks-for-azure-devops-repos-vsts-gij-cloud'>See details</a> on this page.<br>
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

<div align='center' style='margin-top:10px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/61wl72vp91'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before you can proceed with the steps outlined on this guide, indexing triggers must be enabled in the Git Integration for Jira app repository configuration for your Jira Cloud instance. For more details, see <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'>Indexing Triggers - Getting Started</a>.
    </div>
    </div>
</div>
<br>

## Setting up webhook for Azure Repos

Configure webhook by logging in to your VSTS/Azure DevOps account.

1.  Open a project by clicking on it.

    <img src='/wp-content/uploads/gij-webhooks-azure-devops-sel-proj-c.png' width=646 height=361 style='margin:25px 0' />

2.  Click **Project Settings** then select **Service Hooks**. The following screen is displayed.

    <img src='/wp-content/uploads/gij-webhooks-azure-devops-add-shooks-c.png' width=544 height=233 style='margin:25px 0' />

3.  Click + icon to add a new service hook subscription.

4.  Scroll to **Web Hooks** and click to select it.

5.  Click **Next**. The following screen is displayed.

    <img src='/wp-content/uploads/gij-webhooks-azure-devops-triggers-cfg-c.png' width=476 height=499 style='margin:25px 0' />

    *   *Set **"code pushed"** for the _**Trigger on this type of event**_ selector.

    *   Set all **FILTERS** to **"Any"**.

    *   Click **Next** to proceed to the following screen.

        <img src='/wp-content/uploads/gij-webhooks-azure-devops-action-cfg-c.png' width=510&height=535 style='margin:25px 0' />

6.  Switch to your Jira instance then navigate to **Manage Git repositories** page and then click **Indexing triggers** (_or alternatively go to Jira Settings ➜ Apps. On the sidebar, click Indexing triggers_).

    <img src='/wp-content/uploads/gij-jira-cloud-webhook-url-loc-c1.png' width=646 height=430 style='margin:25px 0' />

7.  Copy the complete secret key URL by clicking the copy icon on the right.

8.  Switch back to VSTS/Azure DevOps (where you left off) and paste this information into the provided **URL** box.

9.  Click **Test** to verify if webhook integration is successful or not.

    <img src='/wp-content/uploads/gij-webhooks-azure-devops-test-cfg-c.png' width=578 height=408 style='margin:25px 0' />

10.  Click **Finish** to complete this setup.

11.  Repeat the above steps for **Pull request created** and **Pull request updated** webhooks.

<br>

## Pull request webhooks

The Git Integration for Jira app supports pull request webhooks now.

You will need to have three (3) separate service hooks configuration for it to work properly. Aside from setting up the "**Code pushed**" service hook outlined above in step **6.a**, perform the same process with _**Pull request created**_ and _**Pull request updated**_ for the triggers.

<img src='/wp-content/uploads/gij-azure-devops-server-2019-req-service-hooks.png' width=680 height=239 style='margin:25px 0;max-width: 100%;' />

