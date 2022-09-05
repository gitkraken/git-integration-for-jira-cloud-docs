---

title: Adding webhooks for Bitbucket Cloud
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
        Pull request webhooks are now supported. <a href='/git-integration-for-jira-cloud/adding-webhooks-for-bitbucket-cloud-gij-cloud'>See details</a> on this page.<br>
        <p>Supported webhook events:</p>
        <ul>
            <li><i>Repository</i> - Push</li>
            <li><i>Pull request</i> - Created</li>
            <li><i>Pull request</i> - Updated</li>
        </ul>
    </div>
    </div>
</div>
<br>

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/7tt09xc1my?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/7tt09xc1my'><b>here</b></a> to open this video in a new browser tab for more viewing options. (While the above video showcases other integration, jump to <a href='https://bigbrassband.wistia.com/medias/7tt09xc1my?wtime=1m41s' target='_blank' title='Click to open in a new tab/window'><b>01:41</b></a> <br>to see Webhook setup for Bitbucket Cloud.)</i>
</div>
<br>

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before you can proceed with the steps outlined on this guide, webhooks must be enabled in the Git Integration for Jira app repository configuration for your Jira instance. For more details, see <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'><b>Indexing triggers - Getting Started</b></a>.
    </div>
    </div>
</div>
<br>

## Setting up webhooks for Bitbucket Cloud

Configure webhook by logging in to your Bitbucket.

1.  Open a project by clicking on it.

    <img src='/wp-content/uploads/gij-webhooks-bitbucket-add-shooks-c.png' width=408 height=329 style='margin:25px 0' />

    Click **Repository Settings** then under **WORKFLOW**, select **Webhooks**.

2.  Click **Add webhook** to create a webhook for the repository. The _**Add new webhook**_ screen appears.

    <img src='/wp-content/uploads/gij-webhooks-add-new-whook-bitbucket-dlg-w.png' width=578 height=759 style='margin:25px 0' />

    *   **Title** - This is the title name for this webhook.

    *   **URL** - This field accepts the webhook url from your Git Integration for Jira app ➜ **Webhooks** setting.

    *   **Triggers** - By default, the trigger for the webhook is a repository push. If you want different actions to trigger the webhook, click _**Choose from a full list of triggers**_. The list of all the webhook trigger event types is displayed.
        
        Set the necessary scope depending on your organization access/usage rules. For this guide, choose the following triggers:

        *   Repository - **Push** (required)

        *   Pull Request (optional) - select these options to also include the pull request triggers

            *   **Created**

            *   **Updated**

3.  Switch to your Jira instance then navigate to **Manage Git repositories** page and then click **Indexing triggers** (_or alternatively go to Jira Settings ➜ Apps. On the sidebar, click Indexing triggers_).

    <img src='/wp-content/uploads/gij-jira-cloud-webhook-url-loc-c1.png' width=646 height=430 style='margin:25px 0' />

    Copy the complete secret key URL mentioned from the paragraph description below the **Secret key** box.

4.  Switch back to Bitbucket (where you left off) and paste this information into the provided **URL** box.

5.  Enter a meaningful **Title** name for this webhook.

6.  For the **Triggers**, if your organization does not require pull request events, select **Repository push**. Otherwise, select _**Choose from a full list of triggers**_ (recommended) and then tick Repository (**Push**) and Pull Request (**Created**, **Updated**).

7.  Click **Save** to complete this setup.

<br>

## Pull request webhooks

The Git Integration for Jira app supports pull request webhooks now.

For pull request triggers, you will need to have three (3) separate service hooks configuration for it to work properly. See **step 9**, **second option** for the webhook triggers.

<img src='/wp-content/uploads/gij-webhooks-bitbucket-sample.png' width=680 height=195 style='margin:25px 0' />

