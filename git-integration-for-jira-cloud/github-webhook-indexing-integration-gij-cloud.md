---

title: GitHub webhook indexing integration
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
        For more information on Webhook indexing:
        <ul>
            <li>
                <a href='/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud'>Webhook Indexing Explainer</a>
            </li>
            <li>
                <a href='/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud'>Feature matrix of Git Integration for Jira Cloud</a>
            </li>
        </ul>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        With the Webhook indexing integration, there is no need to enable indexing triggers in the git manager configuration page.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For a step-by-step setup guide, watch the following demonstration videos:
        <ul>
            <li><a href='#setup-webhook-indexing-integration-repository-level'>Setup webhook indexing integration (Repository Level)</a>
            </li>
            <li><a href='#setup-webhook-indexing-integration-organization-level'>Setup webhook indexing integration (Organization Level)</a>
            </li>
        </ul>
    </div>
    </div>
</div>

&nbsp;

## Video Guides

Watch video guides below showcasing Repository and Group level webhook indexing integration.

### Setup webhook indexing integration (Repository Level)

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/p54dj581ec?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:40px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/p54dj581ec'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

### Setup webhook indexing integration (Organization Level)

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/l6msatuap5?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:40px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/l6msatuap5'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

## Connect GitHub.com or GitHub Enterprise Server using the Webhook Indexing integration type to Jira Cloud:

The steps outlined below requires that [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app is already installed on your Jira Cloud instance. Otherwise, install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app first from the Atlassian Marketplace.

### Webhook indexing integration

1.  On your Jira Cloud dashboard, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  For the following screen, click **GitHub.com** to start integration with this git service. If you're using **GitHub Enterprise Server**, choose that instead.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-type-github.png)

4.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-github.png)

5.  For this guide, click on the **Webhook indexing** panel to select it.

    While webhook indexing integration has limited features (such as no branch/pull/merge request creation etc.), this type Git service integration does not require specific configuration behind a firewall.

6.  Click **Add integration**. This adds the current webhook indexing integration to the manage integration list.

    ![](/wp-content/uploads/gij-gitcloud-webhook-indexing-github-settings.png)

7.  <img src='/wp-content/uploads/bbb-alert-20.png' height=20px width=20px style='margin-right:3px'/> Before clicking <b>Finish</b>, make sure to configure webhook for your git service. Use the <b>Webhook URL</b> and the <b>Secret key</b> then follow the steps below for repository level or organization level webhook setup.

&nbsp;

### Repository Level

[See full video walkthrough on this page](#setup-webhook-indexing-integration-repository-level)

Open a new browser tab and login to your GitHub web portal to setup webhook triggers for the selected _**repository**_. Configure a webhook on your git service by performing the following steps:

![](/wp-content/uploads/gij-github-webhooks-setup-add-loc.png)

1.  On your GitHub web portal, open a repository to work on.

2.  Go to **Settings**.

3.  On the sidebar, click **Webhooks**.

4.  Click **Add webhook**. The next screen is displayed.

    ![](/wp-content/uploads/gij-webhook-indexing-github-paste-sel-url-type-key.png)

5.  On the **Payload URL** box, paste the **Webhook URL** that you got from the webhook indexing integration (_settings screen with the Finish button_).

6.  Select `application/json` as the **Content type**. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b>

7.  On the **Secret** box, paste the **Secret key** that you got from the webhook indexing integration (_settings screen with the Finish button_).

8.  Next, set or select which events to trigger for this webhook:

    *   <b>Just the push event</b> – This will send trigger events for commits and branches only.

    *   <b>Send me everything</b> – This will send triggers for every event the git service supports. However, this may impact Jira performance. <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>NOT RECOMMENDED</b>

    *   <b>Let me select individual events</b> – This will send trigger events based on the specified selected events to track. We highly suggest to only select <b>Pushes</b> and <b>Pull requests</b> event triggers. <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b>

9.  Review your settings then click **Add webhook** to save the webhook configuration.

The webhook configuration is added to the webhooks list. You may click **Finish** in the previous session to wrap up the repository level setup.

&nbsp;

### Organization Level

[See full video walkthrough on this page](#setup-webhook-indexing-integration-organization-level)
    
Open a new browser tab and login to your GitHub web portal to configure webhook triggers for your selected _**organization**_. Configure a webhook on your git service by performing the following steps:

1.  On your GitHub web portal, open an organization to work on.

    ![](/wp-content/uploads/gij-github-web-acc-webhook-org-settings.png)

2.  Go to **Settings**. The following screen is displayed.

    ![](/wp-content/uploads/gij-github-web-acc-webhook-org-add.png)

3.  On the sidebar, click **Webhooks**.

4.  Click **Add webhook**. The next screen is displayed.

    ![](/wp-content/uploads/gij-webhook-indexing-github-paste-sel-url-type-key.png)

    On the **Payload URL** box, paste the **Webhook URL** that you got from the webhook indexing integration (_settings screen with the Finish button_).

5.  Select `application/json` as the **Content type**.

6.  On the **Secret** box, paste the **Secret key** that you got from **step 4** above.

7.  Set or select which events to trigger for this webhook:

    *   **Just the push event** – This will send trigger events for commits and branches only.

    *   **Send me everything** – This will send triggers for every event the git service supports. However, this may impact Jira performance. (Not recommended)

    *   **Let me select individual events** – This will send trigger events based on the specified selected events to track. We highly suggest to only select **Pushes** and **Pull requests** event triggers. (Recommended)

8.  Review your settings then click **Add webhook** to save the webhook configuration.

9.  After you’re done setting up the webhook with your git service (GitHub), switch to the Jira Cloud browser tab. Click **Finish** to complete this setup.

The webhook configuration is added to the webhooks list. You may click **Finish** in the previous session to wrap up the organization level setup.

## Post-setup tips

*   With organization level webhook settings, all repositories within the org will be able to send webhook triggers as configured.

*   If you see any issues with the newly added webhook, verify that the **Payload URL**, **Secret key** and **Content type** are set properly. Edit these settings and try again.

*   Edit integration settings via ![](/wp-content/uploads/actions-icon.png) **Actions** on the Manage integrations page. In here, you will find **Webhook URL** and **Secret key** for use with webhook setup with your git service.

*   The events are detected only after the Webhook indexing integration. If you see no repositories in the Manage repositories page, make sure to trigger either the push or pull/merge request events of the working repository.

## How to link commits, branches and pull requests to a Jira issue?

Make a git commit if you don’t see any commits in the Git Commits tab of a Jira issue.

For information on this topic, see [Linking git commits, associating branches and pull requests to a Jira issue](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Git Roll Up tab

The Git Roll Up tab is now supported for GitHub webhook indexing integration.

## Limited features for GitHub webhook indexing integration

The feature table displays the supported git features for the selected git server. For more information, see [Feature matrix for Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

![](/wp-content/uploads/gij-gitcloud-webhook-indexing-compare-vs-full.png)

### ![](/wp-content/uploads/gij-check.png) Works with git servers behind firewall

The webhooks indexing integration limits the features available. However, networks hosting git do not need to be updated to allow incoming requests as long as outbound requests can be made. See [Webhook Indexing explainer](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud) for more information.

### ![](/wp-content/uploads/gij-check.png) View commits, branches, pull requests in Jira

Commits, branches, pull requests are visible in the **Jira Development Information** panel as well as in the **Git Commits issue** tab and **Git Integration** side panel of the Jira issue. Jira administrators can regulate access to these displays using the _View development tools_ permission.

![](/wp-content/uploads/gij-gitcloud-jira-issue-webhook-idx-sample.png)

### View tags in Jira

<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b>

### Support for Automation for Jira + Smart Commits

**Automation for Jira** - the following triggers are supported:

1.  `Commit created`

2.  `Branch created`

3.  `Pull request created`

4.  `Pull request declined`

5.  `Pull request merged`


**Smart Commits:** Atlassian’s Smart Commits are enabled by default. Additional Smart Commit commands are available. See [Smart Commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud) for more information.

### ![](/wp-content/uploads/gij-check.png) Repository Browser

The Repository Browser allows users to view commits in git repositories by branch1. Users can manually link and unlink commits to Jira issues2.

*   Click a git repository on the **View all repositories** page to start from here.

![](/wp-content/uploads/gij-gitcloud-wh-idx-repo-browser-sel.png)

### ![](/wp-content/uploads/gij-error.png) Create branches and pull requests in Jira

This feature is not supported with webhook indexing integration. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud)

### ![](/wp-content/uploads/gij-check.png) Support for large number of commits in git pushes

Git servers may truncate how much of the activity is captured in a webhook on large git push events resulting in some git activity. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

### ![](/wp-content/uploads/gij-error.png) Indexing full repository history

Webhook indexing integration will only show new commit/branch/pull request activity once webhooks are configured on the git server according to this wizard. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

### ![](/wp-content/uploads/gij-error.png) View source code in Jira

Webhook indexing integration does not have this option as webhooks do not contain source code.

## Other supported webhook indexing integration articles

**GitHub webhook indexing integration** (this page)

[GitLab webhook indexing integration](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud)

[Microsoft webhook indexing integration](/git-integration-for-jira-cloud/microsoft-webhook-indexing-integration-gij-cloud)

