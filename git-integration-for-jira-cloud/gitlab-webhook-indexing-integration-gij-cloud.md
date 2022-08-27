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
        <ul>
            <li>
                <a href='/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud/'>Webhook Indexing Explainer</a>
            </li>
            <li>
                <a href='/git-integration-for-jira-cloud/features-gij-cloud/'>Feature matrix of Git Integration for Jira Cloud</a>
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
        <ul>
            <li>
                <a href='#repository-level'>Setup webhook indexing integration (Repository Level)</a>
            </li>
            <li>
                <a href='#group-level'>Setup webhook indexing integration (Group Level)</a>
            </li>
        </ul>
    </div>
    </div>
</div>
<br>

## Video Guides

Watch video guides below showcasing Repository and Group level webhook indexing integration.

### Repository Level

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/ejgouua9x4?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/ejgouua9x4'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

### Group Level

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/uh616awfnj?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/uh616awfnj'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

## Connect GitLab.com or GitLab CE|EE using the Webhook Indexing integration type to Jira Cloud:

The steps outlined below requires that [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app is already installed on your Jira Cloud instance. Otherwise, install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app first from the Atlassian Marketplace.

*   **Webhook indexing integration**

    1.  On your Jira Cloud dashboard, go to **Apps** ➜ **Git Integration: Manage integrations**.

        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1648550939105&cacheVersion=1&api=v2)

    2.  On the Manage integrations page, click **Add integration.**

        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1648551205479&cacheVersion=1&api=v2)

    3.  On the following screen, click on the **Webhook indexing integration** panel for your integration type.

        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-managed-ui-webhook-idx-sel2(c).png?version=1&modificationDate=1648551332700&cacheVersion=1&api=v2)

    4.  Select **GitLab** for the git hosting service then click **Add integration**.

        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-managed-ui-webhook-idx-gitlab-sel(c).png?version=1&modificationDate=1648551532537&cacheVersion=1&api=v2)

    5.  The following screen is displayed:

        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-managed-ui-webhook-idx-gitlab-setup(c).png?version=1&modificationDate=1648551862902&cacheVersion=1&api=v2)

        *   The webhook indexing integration has been added to the manage integration list.

        *   <img src='/wp-content/uploads/bbb-alert-20.png' /> Before clicking **Finish**, make sure to configure webhook for your git service. Use the **Webhook URL** and the **Secret key** then follow the steps below for repository level or organization level webhook setup.

*   <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>REPOSITORY LEVEL</b> **GitLab Repository webhook setup** (see <a href='#Repository-level'>full video walkthrough</a> on this page)

    Open a new browser tab and login to your GitLab web portal to setup webhook triggers for the selected _**repository**_. Configure a webhook on your git service by performing the following steps:

    1.  On your GitLab web portal, open a repository to work on.

    2.  Go to **Settings**.

        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitlab-web-repo-portal-sample(c).png?version=1&modificationDate=1618662448010&cacheVersion=1&api=v2)

    3.  On the sidebar, click **Webhooks**. The next screen is displayed.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/webhook-indexing-GITLAB-paste-sel-url-type-key(acc).png?version=2&modificationDate=1621093126132&cacheVersion=1&api=v2&width=612&height=326)

        *   On the **URL** box, paste the **Webhook URL** that you got from the previous section.

        *   On the **Secret token** box, paste the **Secret key** that you got from **step 4** above.

        *   Set or select which events to trigger for this webhook:

            *   **Push events** – This will send trigger events for commits and branches only. (Recommended)

            *   **Tags push events** – COMING SOON This will be supported in the future.

            *   **Merge request events** – This will send trigger events for merge requests event triggers. (Recommended)

    4.  Review your webhook setup and we recommend to test your settings. For example, test **Push events** and **Merge request events** if it fails or succeeds.

    5.  If it returns no errors, click **Add webhook** to save the webhook configuration.

    6.  The webhook configuration is added to the webhooks list.

*   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>GROUP LEVEL</b> **GitLab Group webhook setup** (see <a href='#Group-level'>full video walkthrough</a> on this page)
    
    Open a new browser tab and login to your GitLab web portal to setup webhook triggers for the selected _**group**_. Configure a webhook on your git service by performing the following steps:

    1.  On your GitLab web portal, go to **Your groups** and open a group to work on.

    2.  Go to **Settings**.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitlab-group-setup-webhooks-01(c).png?version=1&modificationDate=1621094785971&cacheVersion=1&api=v2&width=612&height=419)

    3.  On the sidebar, click **Webhooks**. The next screen is displayed.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitlab-group-setup-webhooks-03(c).png?version=2&modificationDate=1621094660200&cacheVersion=1&api=v2&width=612&height=337)

        *   On the **URL** box, paste the **Webhook URL** that you got from the previous section.

        *   On the **Secret token** box, paste the **Secret key** that you got from **step 4** above.

        *   Set or select which events to trigger for this webhook:

            *   **Push events** – This will send trigger events for commits and branches only. (Recommended)

            *   **Tags push events** – <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b> This will be supported in the future.

            *   **Merge request events** – This will send trigger events for merge requests event triggers. (Recommended)

    4.  Review your webhook setup and we recommend to test your settings. For example, test **Push events** and **Merge request events** if it fails or succeeds.

    5.  If it returns no errors, click **Add webhook** to save the webhook configuration.

    6.  The webhook configuration is added to the webhooks list.

After you’re done setting up the webhook with your git service (GitLab), switch to the Jira Cloud browser tab. Click **Finish** to complete this setup.

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
<br>

## How to link commits, branches and pull requests to a Jira issue?

Make a commit if you don’t see commits in the Git Commits tab of an associated Jira issue.

For information on this topic, see [Linking git commits, associating branches and pull requests to a Jira issue](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud/).

## Git Roll Up tab

The Git Roll Up tab is now supported for GitLab webhook indexing integration.

## Limited features for GitLab webhook indexing integration

The feature table displays the supported git features for the selected git server. For more information, see [Feature matrix for Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud/).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitcloud-webhook-indexing-compare-vs-full-gitlab.png?version=1&modificationDate=1648552846840&cacheVersion=1&api=v2&width=566&height=372)

### ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) Works with git servers behind firewall

The webhooks indexing integration limits the features available. However, networks hosting git do not need to be updated to allow incoming requests as long as outbound requests can be made. See [Webhook Indexing explainer](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud/) for more information.

### ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) View commits, branches, pull requests in Jira

Commits, branches, pull requests are visible in the**Jira Development Information** panel as well as in the **Git Commits issue** tab and **Git Integration** side panel of the Jira issue. Jira administrators can regulate access to these displays using the _View development tools_ permission.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitcloud-jira-issue-webhook-idx-gitlab.png?version=2&modificationDate=1618832120050&cacheVersion=1&api=v2&width=680&height=369)

### View tags in Jira

COMING SOON

### ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) Support for Automation for Jira + Smart Commits

**Automation for Jira** - the following triggers are supported:

1.  `Commit created`

2.  `Branch created`

3.  `Pull request created`

4.  `Pull request declined`

5.  `Pull request merged`


**Smart Commits:** Atlassian’s Smart Commits are enabled by default. Additional Smart Commit commands are available. See [Smart Commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud/) for more information.

### ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) Repository Browser

The Repository Browser allows users to view commits in git repositories by branch1. Users can manually link and unlink commits to Jira issues2.

*   Click a git repository on the **View all repositories** page to start from here.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitcloud-wh-idx-repo-browser-sel.png?version=2&modificationDate=1618636199313&cacheVersion=1&api=v2&width=680&height=269)

### ![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) Create branches and pull requests in Jira

This feature is not supported with webhook indexing integration. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud/)

### Support for large number of commits in git pushes

Git servers may truncate how much of the activity is captured in a webhook on large git push events resulting in some git activity. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud/).

### ![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) Indexing full repository history

Webhook indexing integration will only show new commit/branch/pull request activity once webhooks are configured on the git server according to this wizard. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud/).

### ![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) View source code in Jira

Webhook indexing integration does not have this option as webhooks do not contain source code.

