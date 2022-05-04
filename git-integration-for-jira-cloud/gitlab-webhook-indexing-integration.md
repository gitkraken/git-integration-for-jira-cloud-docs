---

title: GitLab webhook indexing integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# GitLab webhook indexing integration

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1503494176/GitLab+webhook+indexing+integration>

* * *

For more information on Webhook indexing:

*   [Webhook Indexing Explainer](/wiki/spaces/GITCLOUD/pages/1422819484/Webhook+Indexing+Explainer)
    
*   [Feature matrix of Git Integration for Jira Cloud](/wiki/spaces/GITCLOUD/pages/1470398499/Feature+matrix+of+Git+Integration+for+Jira+Cloud)
    

With webhook indexing integration, there’s no need to enable indexing triggers in the git manager configuration page.

For a step-by-step setup guide, watch the following demonstration videos:

*   [Setup webhook indexing integration (Repository Level)](#Repository-Level)
    
*   [Setup webhook indexing integration (Group Level)](#Group-Level)
    

## Video Guides

### Repository Level

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/ejgouua9x4) _and open this video in a new window/tab for more viewing options._

### Group Level

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/uh616awfnj) _and open this video in a new window/tab for more viewing options._

## Connect GitLab.com or GitLab CE|EE using the Webhook Indexing integration type to Jira Cloud:

The steps outlined below requires that [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app is already installed on your Jira Cloud instance. Otherwise, install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app first from the Atlassian Marketplace.

1.  ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Webhook indexing integration**
    
    1.  On your Jira Cloud dashboard, go to **Apps** ➜ **Git Integration: Manage integrations**.
        
    2.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1648550939105&cacheVersion=1&api=v2)
        
        On the Manage integrations page, click **Add integration.**
        
        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1648551205479&cacheVersion=1&api=v2)
    3.  On the following screen, click on the **Webhook indexing integration** panel for your integration type.
        
        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-managed-ui-webhook-idx-sel2(c).png?version=1&modificationDate=1648551332700&cacheVersion=1&api=v2)
    4.  Select **GitLab** for the git hosting service then click **Add integration**.
        
    5.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-managed-ui-webhook-idx-gitlab-sel(c).png?version=1&modificationDate=1648551532537&cacheVersion=1&api=v2)
        
        The following screen is displayed:
        
        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitcloud-managed-ui-webhook-idx-gitlab-setup(c).png?version=1&modificationDate=1648551862902&cacheVersion=1&api=v2)
        1.  Enter webhook indexing integration has been added to the manage integration list.
            
        2.  ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Before clicking **Finish**, make sure to configure webhook for your git service. Use the **Webhook URL** and the **Secret key** then follow the steps below for repository level or organization level webhook setup.
            
2.  ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) REPOSITORY LEVEL **GitLab Repository webhook setup** (see full video walkthrough on this page)  
    Open a new browser tab and login to your GitLab web portal to setup webhook triggers for the selected _**repository**_. Configure a webhook on your git service by performing the following steps:
    
    1.  On your GitLab web portal, open a repository to work on.
        
    2.  Go to ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Settings**.
        
    3.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1503494176/gitlab-web-repo-portal-sample(c).png?version=1&modificationDate=1618662448010&cacheVersion=1&api=v2)
        
        On the sidebar, click **Webhooks**. The next screen is displayed.
        
    4.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/webhook-indexing-GITLAB-paste-sel-url-type-key(acc).png?version=2&modificationDate=1621093126132&cacheVersion=1&api=v2&width=612&height=326)
        
        On the **URL** box, paste the **Webhook URL** that you got from the previous section.
        
    5.  On the **Secret token** box, paste the **Secret key** that you got from **step 4** above.
        
    6.  Set or select which events to trigger for this webhook:
        
        *   **Push events** – This will send trigger events for commits and branches only. (Recommended)
            
        *   **Tags push events** – COMING SOON This will be supported in the future.
            
        *   **Merge request events** – This will send trigger events for merge requests event triggers. (Recommended)
            
    7.  Review your webhook setup and we recommend to test your settings. For example, test **Push events** and **Merge request events** if it fails or succeeds.
        
    8.  If it returns no errors, click **Add webhook** to save the webhook configuration.
        
    9.  The webhook configuration is added to the webhooks list.
        
3.  ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) GROUP LEVEL **GitLab Group webhook setup** (see full video walkthrough on this page)  
    Open a new browser tab and login to your GitLab web portal to setup webhook triggers for the selected _**group**_. Configure a webhook on your git service by performing the following steps:
    
    1.  On your GitLab web portal, go to **Your groups** and open a group to work on.
        
    2.  Go to ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Settings**.
        
    3.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitlab-group-setup-webhooks-01(c).png?version=1&modificationDate=1621094785971&cacheVersion=1&api=v2&width=612&height=419)
        
        On the sidebar, click **Webhooks**. The next screen is displayed.
        
    4.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitlab-group-setup-webhooks-03(c).png?version=2&modificationDate=1621094660200&cacheVersion=1&api=v2&width=612&height=337)
        
        On the **URL** box, paste the **Webhook URL** that you got from the previous section.
        
    5.  On the **Secret token** box, paste the **Secret key** that you got from **step 4** above.
        
    6.  Set or select which events to trigger for this webhook:
        
        1.  **Push events** – This will send trigger events for commits and branches only. (Recommended)
            
        2.  **Tags push events** – COMING SOON This will be supported in the future.
            
        3.  **Merge request events** – This will send trigger events for merge requests event triggers. (Recommended)
            
    7.  Review your webhook setup and we recommend to test your settings. For example, test **Push events** and **Merge request events** if it fails or succeeds.
        
    8.  If it returns no errors, click **Add webhook** to save the webhook configuration.
        
    9.  The webhook configuration is added to the webhooks list.
        
4.  After you’re done setting up the webhook with your git service (GitLab), switch to the Jira Cloud browser tab. Click **Finish** to complete this setup.
    

If you see any issues with the newly added webhook, verify that the **Payload URL** and **Secret key** are set properly. Edit the these settings and try again.

Edit integration settings via **Actions** on the Manage Git repository page. In here, you will find **Webhook URL** and **Secret key** for use with webhook setup with your git service.

## How to link commits, branches and pull requests to a Jira issue?

Make a commit if you don’t see commits in the Git Commits tab of an associated Jira issue.

For information on this topic, see [Linking git commits, associating branches and pull requests to a Jira issue](/wiki/spaces/GITCLOUD/pages/1503526923).

## Git Roll Up tab

The Git Roll Up tab is now supported for GitLab webhook indexing integration.

## Limited features for GitLab webhook indexing integration

The feature table displays the supported git features for the selected git server. For more information, see [Feature matrix for Git Integration for Jira Cloud](/wiki/spaces/GITCLOUD/pages/1470398499/Feature+matrix+of+Git+Integration+for+Jira+Cloud).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitcloud-webhook-indexing-compare-vs-full-gitlab.png?version=1&modificationDate=1648552846840&cacheVersion=1&api=v2&width=566&height=372)

### ![(tick)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) Works with git servers behind firewall

The webhooks indexing integration limits the features available. However, networks hosting git do not need to be updated to allow incoming requests as long as outbound requests can be made. See [Webhook Indexing explainer](/wiki/spaces/GITCLOUD/pages/1422819484/Webhook+Indexing+Explainer) for more information.

### ![(tick)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) View commits, branches, pull requests in Jira

Commits, branches, pull requests are visible in the ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Jira Development Information** panel as well as in the ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Git Commits issue** tab and ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Git Integration** side panel of the Jira issue. Jira administrators can regulate access to these displays using the _View development tools_ permission.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitcloud-jira-issue-webhook-idx-gitlab.png?version=2&modificationDate=1618832120050&cacheVersion=1&api=v2&width=680&height=369)

### ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) View tags in Jira

COMMING SOON

### ![(tick)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) Support for Automation for Jira + Smart Commits

**Automation for Jira** - the following triggers are supported:

1.  `Commit created`
    
2.  `Branch created`
    
3.  `Pull request created`
    
4.  `Pull request declined`
    
5.  `Pull request merged`
    

**Smart Commits:** Atlassian’s Smart Commits are enabled by default. Additional Smart Commit commands are available. See [Smart Commits](https://bigbrassband.com/git-integration-for-jira/documentation/smart-commits.html) for more information.

### ![(tick)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) Repository Browser

The Repository Browser allows users to view commits in git repositories by branch1. Users can manually link and unlink commits to Jira issues2.

*   Click a git repository on the **View all repositories** page to start from here.
    

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1503494176/gitcloud-wh-idx-repo-browser-sel.png?version=2&modificationDate=1618636199313&cacheVersion=1&api=v2&width=680&height=269)

### ![(error)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) Create branches and pull requests in Jira

This feature is not supported with webhook indexing integration. For more information, see [Feature matrix of Git Integration for Jira Cloud](/wiki/spaces/GITCLOUD/pages/1470398499/Feature+matrix+of+Git+Integration+for+Jira+Cloud)

### ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Support for large number of commits in git pushes

Git servers may truncate how much of the activity is captured in a webhook on large git push events resulting in some git activity. For more information, see [Feature matrix of Git Integration for Jira Cloud](/wiki/spaces/GITCLOUD/pages/1470398499/Feature+matrix+of+Git+Integration+for+Jira+Cloud).

### ![(error)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) Indexing full repository history

Webhook indexing integration will only show new commit/branch/pull request activity once webhooks are configured on the git server according to this wizard. For more information, see [Feature matrix of Git Integration for Jira Cloud](/wiki/spaces/GITCLOUD/pages/1470398499/Feature+matrix+of+Git+Integration+for+Jira+Cloud).

### ![(error)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) View source code in Jira

Webhook indexing integration does not have this option as webhooks do not contain source code.

## Other supported webhook indexing integration articles

*   Page:
    
    [GitHub webhook indexing integration](/wiki/spaces/GITCLOUD/pages/1494646787/GitHub+webhook+indexing+integration) (Git Integration for Jira Cloud)
    
*   Page:
    
    [GitLab webhook indexing integration](/wiki/spaces/GITCLOUD/pages/1503494176/GitLab+webhook+indexing+integration) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Microsoft webhook indexing integration](/wiki/spaces/GITCLOUD/pages/1509032469/Microsoft+webhook+indexing+integration) (Git Integration for Jira Cloud)