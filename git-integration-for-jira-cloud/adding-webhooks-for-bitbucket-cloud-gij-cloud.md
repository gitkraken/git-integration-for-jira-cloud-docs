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

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/467271681/webhooks-bitbucket-add-shooks(c).png?version=1&modificationDate=1588130532215&cacheVersion=1&api=v2&width=408&height=329)

    Click **Repository Settings** then under **WORKFLOW**, select **Webhooks**.

2.  Click **Add webhook** to create a webhook for the repository. The _**Add new webhook**_ screen appears.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/467271681/webhooks-add-new-whook-bitbucket-dlg(w).png?version=1&modificationDate=1588130531394&cacheVersion=1&api=v2&width=578&height=759)

    *   **Title** - This is the title name for this webhook.

    *   **URL** - This field accepts the webhook url from your Git Integration for Jira app ➜ **Webhooks** setting.

    *   **Triggers** - By default, the trigger for the webhook is a repository push. If you want different actions to trigger the webhook, click _**Choose from a full list of triggers**_. The list of all the webhook trigger event types is displayed.
        
        Set the necessary scope depending on your organization access/usage rules. For this guide, choose the following triggers:

        *   Repository - **Push** (required)

        *   Pull Request (optional) - select these options to also include the pull request triggers

            *   **Created**

            *   **Updated**

3.  Switch to your Jira instance then navigate to **Manage Git repositories** page and then click **Indexing triggers** (_or alternatively go to Jira Settings ➜ Apps. On the sidebar, click Indexing triggers_).

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/467271681/jira-cloud-webhook-url-loc(c1).png?version=1&modificationDate=1617191745969&cacheVersion=1&api=v2&width=646&height=430)

    Copy the complete secret key URL mentioned from the paragraph description below the **Secret key** box.

4.  Switch back to Bitbucket (where you left off) and paste this information into the provided **URL** box.

5.  Enter a meaningful **Title** name for this webhook.

6.  For the **Triggers**, if your organization does not require pull request events, select **Repository push**. Otherwise, select _**Choose from a full list of triggers**_ (recommended) and then tick Repository (**Push**) and Pull Request (**Created**, **Updated**).

7.  Click **Save** to complete this setup.

<br>

## Pull request webhooks

The Git Integration for Jira app supports pull request webhooks now.

For pull request triggers, you will need to have three (3) separate service hooks configuration for it to work properly. See **step 9**, **second option** for the webhook triggers.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/467271681/webhooks-bitbucket-sample.png?version=1&modificationDate=1588130531945&cacheVersion=1&api=v2&width=680&height=195)

