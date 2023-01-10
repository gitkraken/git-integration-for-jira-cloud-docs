---

title: GitLab webhook indexing integration
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
        For more information on Webhook indexing:<br>
        <ul style='margin-bottom:0px !important'>
            <li>
                <a href='/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud'>Webhook Indexing Explainer</a>
            </li>
            <li>
                <a href='/git-integration-for-jira-cloud/features-gij-cloud'>Feature matrix of Git Integration for Jira Cloud</a>
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
        With webhook indexing integration, there’s no need to enable indexing triggers in the git manager configuration page.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For a step-by-step setup guide, watch the following demonstration videos:<br>
        <ul style='margin-bottom:0px !important'>
            <li>
                <a href='#setup-webhook-indexing-integration-repository-level'>Setup webhook indexing integration (Repository Level)</a>
            </li>
            <li>
                <a href='#setup-webhook-indexing-integration-group-level'>Setup webhook indexing integration (Group Level)</a>
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
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/ejgouua9x4?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:35px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/ejgouua9x4'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

### Setup webhook indexing integration (Group Level)

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/uh616awfnj?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:35px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/uh616awfnj'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

## Connect GitLab.com or GitLab CE/EE using the Webhook Indexing integration type to Jira Cloud:

The steps outlined below requires that [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app is already installed on your Jira Cloud instance. Otherwise, install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app first from the Atlassian Marketplace.

### Webhook indexing integration

1.  On your Jira Cloud dashboard, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  For the following screen, click **GitLab.com** to start integration with this git service. If you're using GitLab CE/EE, choose **GitLab Server** instead.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-type-gitlab-com.png)

4.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-gitlab.png)

5.  For this guide, click on the **Webhook indexing** panel to select it.

    While webhook indexing integration has limited features (such as no branch/pull/merge request creation etc.), this type Git service integration does not require specific configuration behind a firewall.

6.  Click **Add integration** to proceed. The screen below shows the webhook indexing settings for use with the GitLab git service webhook setup. This also adds the current webhook indexing integration to the manage integration list.

    ![](/wp-content/uploads/gij-gitcloud-webhook-indexing-github-settings.png)

7.  <img src='/wp-content/uploads/bbb-alert-20.png' style='margin-right:3px' /> Before clicking <b>Finish</b>, make sure to configure webhook for your git service. Use the <b>Webhook URL</b> and the <b>Secret key</b> then follow the steps below for repository level or group level webhook setup.

#### GitLab Repository level

[See full video walkthrough on this page](#setup-webhook-indexing-integration-repository-level)

Open a new browser tab and login to your GitLab web portal to setup webhook triggers for the selected _**repository**_. Configure a webhook on your git service by performing the following steps:

1.  On your GitLab web portal, open a repository to work on.

    ![](/wp-content/uploads/gij-gitlab-web-repo-webhook-cfg-portal-sample.png)

2.  On the sidebar, go to **Settings** then click **Webhooks**.

3.  The next screen is displayed.

    ![](/wp-content/uploads/gij-webhook-indexing-GITLAB-paste-sel-url-type-key.png)

4.  On the **URL** box, paste the **Webhook URL** that you got from the webhook indexing integration (_settings screen with the Finish button_).

5.  On the **Secret token** box, paste the **Secret key** that you got from the webhook indexing integration (_settings screen with the Finish button_).

6.  Set or select which events to trigger for this webhook:

    *   **Push events** – This will send trigger events for commits and branches only. <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b>

    *   **Tags push events** – <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b> <i>This will be supported in the future.</i>

    *   **Merge request events** – This will send trigger events for merge requests event triggers. <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b>

7.  Review your settings then click **Add webhook** to save the webhook configuration.

The webhook configuration is added to the webhooks list. You may click **Finish** on the webhook indexing integration screen (Jira Cloud) to wrap the repository level setup.

#### GitLab Group level

[See full video walkthrough on this page](#setup-webhook-indexing-integration-group-level)
    
Open a new browser tab and login to your GitLab web portal to setup webhook triggers for the selected _**group**_. Configure a webhook on your git service by performing the following steps:

1.  On your GitLab web portal, open a repository to work on.

    ![](/wp-content/uploads/gij-gitlab-web-group-webhook-cfg-portal-sample-.png)

2.  On the sidebar, go to **Settings** then click **Webhooks**.

3.  The next screen is displayed.

    ![](/wp-content/uploads/gij-webhook-indexing-GITLAB-paste-sel-url-type-key.png)

4.  On the **URL** box, paste the **Webhook URL** that you got from the webhook indexing integration (_settings screen with the Finish button_).

5.  On the **Secret token** box, paste the **Secret key** that you got from the webhook indexing integration (_settings screen with the Finish button_).

6.  Set or select which events to trigger for this webhook:

    *   <b>Push events</b> – This will send trigger events for commits and branches only. <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b>

    *   <b>Tags push events</b> – <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b> <i>This will be supported in the future.</i>

    *   <b>Merge request events</b> – This will send trigger events for merge requests event triggers. <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b>

7.  Review your settings then click **Add webhook** to save the webhook configuration.

The webhook configuration is added to the webhooks list. You may click **Finish** in the previous session to wrap up the group level setup.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If you see any issues with the newly added webhook, verify that the <b>Payload URL</b> and <b>Secret key</b> are set properly. Edit the these settings and try again.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Edit integration settings via <b>Actions</b> on the Manage Git repository page. In here, you will find <b>Webhook URL</b> and <b>Secret key</b> for use with webhook setup with your git service.
    </div>
    </div>
</div>

&nbsp;

## How to link commits, branches and pull requests to a Jira issue?

Make a commit if you don’t see commits in the Git Commits tab of an associated Jira issue.

For information on this topic, see [Linking git commits, associating branches and pull requests to a Jira issue](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Git Roll Up tab

The Git Roll Up tab is now supported for GitLab webhook indexing integration.

## Limited features for GitLab webhook indexing integration

The feature table displays the supported git features for the selected git server. For more information, see [Feature matrix for Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

![](/wp-content/uploads/gij-gitcloud-webhook-indexing-compare-vs-full-gitlab.png)

### ![](/wp-content/uploads/gij-check.png) Works with git servers behind firewall

The webhooks indexing integration limits the features available. However, networks hosting git do not need to be updated to allow incoming requests as long as outbound requests can be made. See [Webhook Indexing explainer](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud) for more information.

### ![](/wp-content/uploads/gij-check.png) View commits, branches, pull requests in Jira

Commits, branches, pull requests are visible in the**Jira Development Information** panel as well as in the **Git Commits issue** tab and **Git Integration** side panel of the Jira issue. Jira administrators can regulate access to these displays using the _View development tools_ permission.

![](/wp-content/uploads/gij-gitcloud-jira-issue-webhook-idx-gitlab.png)

### View tags in Jira

<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b>

### ![](/wp-content/uploads/gij-check.png) Support for Automation for Jira + Smart Commits

**Automation for Jira** - the following triggers are supported:

1.  `Commit created`

2.  `Branch created`

3.  `Pull request created`

4.  `Pull request declined`

5.  `Pull request merged`


**Smart Commits:** Atlassian’s Smart Commits are enabled by default. Additional Smart Commit commands are available. See [Smart Commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud) for more information.

### ![](/wp-content/uploads/gij-error.png) Repository Browser

The Repository Browser allows users to view commits in git repositories by branch1. Users can manually link and unlink commits to Jira issues.

*   Click a git repository on the **View all repositories** page to start from here.

![](/wp-content/uploads/gij-gitcloud-wh-idx-repo-browser-sel.png)

### ![](/wp-content/uploads/gij-error.png) Create branches and pull requests in Jira

This feature is not supported with webhook indexing integration. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud)

### Support for large number of commits in git pushes

Git servers may truncate how much of the activity is captured in a webhook on large git push events resulting in some git activity. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

### ![](/wp-content/uploads/gij-error.png) Indexing full repository history

Webhook indexing integration will only show new commit/branch/pull request activity once webhooks are configured on the git server according to this wizard. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

### ![](/wp-content/uploads/gij-error.png) View source code in Jira

Webhook indexing integration does not have this option as webhooks do not contain source code.

&nbsp;

## Other supported webhook indexing integration articles

[GitHub webhook indexing integration](/git-integration-for-jira-cloud/github-webhook-indexing-integration)

**GitLab webhook indexing integration** (this page)

[Microsoft webhook indexing integration](/git-integration-for-jira-cloud/microsoft-webhook-indexing-integration-gij-cloud)

