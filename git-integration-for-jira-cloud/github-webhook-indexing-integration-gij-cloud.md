---

title: GitHub webhook indexing integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
For more information on Webhook indexing:

*   [Webhook Indexing Explainer](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud)

*   [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud)


With the Webhook indexing integration, there is no need to enable indexing triggers in the git manager configuration page.

For a step-by-step setup guide, watch the following demonstration videos:
## Video Guides
### Repository Level

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/p54dj581ec) _and open this video in a new window/tab for more viewing options._

### Organization Level

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/l6msatuap5) _and open this video in a new window/tab for more viewing options._

## Connect GitHub.com or GitHub Enterprise Server using the Webhook Indexing integration type to Jira Cloud:

The steps outlined below requires that [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app is already installed on your Jira Cloud instance. Otherwise, install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app first from the Atlassian Marketplace.

1.  **Webhook indexing integration**

    1.  On your Jira Cloud dashboard, go to **Apps** ➜ **Git Integration: Manage integrations**.

    2.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1494646787/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1648376688044&cacheVersion=1&api=v2)

        On the Manage integrations page, click **Add integration.**

    3.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1494646787/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1648376962985&cacheVersion=1&api=v2)

        On the following screen, click on the **Webhook indexing integration** panel for your integration type.

    4.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1494646787/gitcloud-managed-ui-webhook-idx-sel2(c).png?version=1&modificationDate=1648377219272&cacheVersion=1&api=v2)

        Select **GitHub** for the git hosting service then click **Add integration**.

    5.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1494646787/gitcloud-managed-ui-webhook-idx-github-sel(c).png?version=1&modificationDate=1648377774862&cacheVersion=1&api=v2)

        The following screen is displayed.

        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1494646787/gitcloud-managed-ui-webhook-idx-github-setup(c).png?version=1&modificationDate=1648383893223&cacheVersion=1&api=v2)
        1.  The webhook indexing integration has been added to the manage integration list.

        2.  Before clicking **Finish**, make sure to configure webhook for your git service. Use the **Webhook URL** and the **Secret key** then follow the steps below for repository level or organization level webhook setup.

2.  **Repository Level** ([see full video walkthrough on this page](#Repository-Level))
    Open a new browser tab and login to your GitHub web portal to setup webhook triggers for the selected _**repository**_. Configure a webhook on your git service by performing the following steps:

    1.  On your GitHub web portal, open a repository to work on.

    2.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1494646787/github-webhooks-setup-add-loc(acc).png?version=1&modificationDate=1618548411025&cacheVersion=1&api=v2)

        Go to **Settings**.

    3.  On the sidebar, click **Webhooks**.

    4.  Click **Add webhook**. The next screen is displayed.

    5.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1494646787/webhook-indexing-github-paste-sel-url-type-key(acc1).png?version=2&modificationDate=1618547229990&cacheVersion=1&api=v2&width=612&height=326)

        On the **Payload URL** box, paste the **Webhook URL** that you got from the previous section.

    6.  Select `application/json` as the **Content type**.

    7.  On the **Secret** box, paste the **Secret key** that you got from **step 4** above.

    8.  Set or select which events to trigger for this webhook:

        *   **Just the push event** – This will send trigger events for commits and branches only.

        *   **Send me everything** – This will send triggers for every event the git service supports. However, this may impact Jira performance. (Not recommended)

        *   **Let me select individual events** – This will send trigger events based on the specified selected events to track. We highly suggest to only select **Pushes** and **Pull requests** event triggers. (Recommended)

    9.  Review your settings then click **Add webhook** to save the webhook configuration.

    10.  The webhook configuration is added to the webhooks list.

3.  **Organization Level** ([see full video walkthrough on this page](#Organization-Level))
    Open a new browser tab and login to your GitHub web portal to configure webhook triggers for your selected _**organization**_. Configure a webhook on your git service by performing the following steps:

    1.  On your GitHub web portal, open an organization to work on.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1494646787/github-web-acc-webhook-org-settings(c).png?version=1&modificationDate=1618478203844&cacheVersion=1&api=v2&width=612&height=461)
    2.  Go to **Settings**. The following screen is displayed.

    3.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1494646787/github-web-acc-webhook-org-add(ca).png?version=2&modificationDate=1618548809758&cacheVersion=1&api=v2)

        On the sidebar, click **Webhooks**.

    4.  Click **Add webhook**. The next screen is displayed.

    5.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1494646787/webhook-indexing-github-paste-sel-url-type-key(acc1).png?version=2&modificationDate=1618547229990&cacheVersion=1&api=v2&width=612&height=326)

        On the **Payload URL** box, paste the **Webhook URL** that you got from the previous section.

    6.  Select `application/json` as the **Content type**.

    7.  On the **Secret** box, paste the **Secret key** that you got from **step 4** above.

    8.  Set or select which events to trigger for this webhook:

        *   **Just the push event** – This will send trigger events for commits and branches only.

        *   **Send me everything** – This will send triggers for every event the git service supports. However, this may impact Jira performance. (Not recommended)

        *   **Let me select individual events** – This will send trigger events based on the specified selected events to track. We highly suggest to only select **Pushes** and **Pull requests** event triggers. (Recommended)

    9.  Review your settings then click **Add webhook** to save the webhook configuration.

    10.  The webhook configuration is added to the webhooks list.

4.  After you’re done setting up the webhook with your git service (GitHub), switch to the Jira Cloud browser tab. Click **Finish** to complete this setup.


With organization level webhook settings, all repositories within the org will be able to send webhook triggers as configured.

If you see any issues with the newly added webhook, verify that the **Payload URL**, **Secret key** and **Content type** are set properly. Edit these settings and try again.

Edit integration settings via **Actions** on the Manage integration page. In here, you will find **Webhook URL** and **Secret key** for use with webhook setup with your git service.

The events are detected only after the Webhook indexing integration. If you see no repositories in the Manage repositories page, make sure to trigger either the push or pull/merge request events of the working repository.

## How to link commits, branches and pull requests to a Jira issue?

Make a git commit if you don’t see any commits in the Git Commits tab of a Jira issue.

For information on this topic, see [Linking git commits, associating branches and pull requests to a Jira issue](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Git Roll Up tab

The Git Roll Up tab is now supported for GitHub webhook indexing integration.

## Limited features for GitHub webhook indexing integration

The feature table displays the supported git features for the selected git server. For more information, see [Feature matrix for Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1494646787/gitcloud-webhook-indexing-compare-vs-full.png?version=1&modificationDate=1648550807671&cacheVersion=1&api=v2&width=566&height=372)

### ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) Works with git servers behind firewall

The webhooks indexing integration limits the features available. However, networks hosting git do not need to be updated to allow incoming requests as long as outbound requests can be made. See [Webhook Indexing explainer](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud) for more information.

### ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) View commits, branches, pull requests in Jira

Commits, branches, pull requests are visible in the **Jira Development Information** panel as well as in the **Git Commits issue** tab and **Git Integration** side panel of the Jira issue. Jira administrators can regulate access to these displays using the _View development tools_ permission.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1494646787/gitcloud-jira-issue-webhook-idx-sample.png?version=1&modificationDate=1618483032016&cacheVersion=1&api=v2)

### View tags in Jira

COMING SOON

### Support for Automation for Jira + Smart Commits

**Automation for Jira** - the following triggers are supported:

1.  `Commit created`

2.  `Branch created`

3.  `Pull request created`

4.  `Pull request declined`

5.  `Pull request merged`


**Smart Commits:** Atlassian’s Smart Commits are enabled by default. Additional Smart Commit commands are available. See [Smart Commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud) for more information.

### ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) Repository Browser

The Repository Browser allows users to view commits in git repositories by branch1. Users can manually link and unlink commits to Jira issues2.

*   Click a git repository on the **View all repositories** page to start from here.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1494646787/gitcloud-wh-idx-repo-browser-sel.png?version=1&modificationDate=1618484981635&cacheVersion=1&api=v2&width=680&height=269)

### ![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) Create branches and pull requests in Jira

This feature is not supported with webhook indexing integration. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud)

### ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) Support for large number of commits in git pushes

Git servers may truncate how much of the activity is captured in a webhook on large git push events resulting in some git activity. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

### ![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) Indexing full repository history

Webhook indexing integration will only show new commit/branch/pull request activity once webhooks are configured on the git server according to this wizard. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

### ![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) View source code in Jira

Webhook indexing integration does not have this option as webhooks do not contain source code.

