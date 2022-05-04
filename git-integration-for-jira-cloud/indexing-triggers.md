---

title: Indexing Triggers
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Indexing Triggers

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/171475219/Indexing+Triggers>

* * *

**What’s on this page:**

* * *

## What are indexing triggers and why use them?

Indexing triggers (webhooks) can be an extremely powerful tool that can be configured to activate an immediate re-index of your repositories from remote systems. Your git server can send this near real-time data to Jira when your git data changes. This results in a much faster indexing time where you don’t have to wait for the regular polling interval (see [**General settings**](/wiki/spaces/GITCLOUD/pages/781942911/General+Settings)).

Webhooks can be initiated whenever certain actions are performed. For example, you can configure a webhook to execute when:

*   a new commit is pushed
    
*   a pull request is opened
    
*   a branch is merged
    

You can create indexing triggers for individual repositories. Most git providers will also allow you to create webhooks at an account-level or org-level.

## Do I need to set up indexing triggers?

By configuring indexing triggers to initiate reindexing, Jira will more often have up-to-date information.

Without setting up indexing triggers, you will be relying on the default polling of the app which is unchangeable by non-Jira administrators. Jira users will have to wait for the default interval for updates (usually 5 minutes) – which means users will not quickly see new commits or pull requests until the next indexing interval.

## Getting started

**Important**  
To use the indexing triggers feature, it must be enabled in the Manage (Git) repositories ➜ **Indexing triggers** page.

Configure indexing triggers to activate immediate reindex of your repositories from remote systems.

1.  From your Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Repository browser**. (_Alternatively, go to_ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) _Jira Settings ➜ Apps_).
    
2.  On the sidebar, click **Indexing triggers**. The following screen is displayed.
    
    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/171475219/gitcloud-new-webhooks-settings-page(c).png?version=1&modificationDate=1617197700707&cacheVersion=1&api=v2)
3.  Enable/disable the indexing trigger feature by clicking on the **Indexing triggers enabled** toggle switch.
    

## Where to get the indexing triggers webhook URL?

The webhooks URL can be accessed on the following locations:

1.  From your Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Repository browser**. On the sidebar, click **Indexing triggers**. (_Alternatively, go to_ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) _Jira Settings_ ➜ _Apps**.** On the sidebar, click Indexing triggers_).
    
    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/gitcloud-indexing-triggers-loc-01(c).png?version=1&modificationDate=1617197700714&cacheVersion=1&api=v2&width=646&height=301)
2.  On the Manage Git repositories configuration page, click the Indexing triggers button at the top right of the page.
    
    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/gitcloud-indexing-triggers-loc-02(c).png?version=1&modificationDate=1617197700717&cacheVersion=1&api=v2&width=646&height=414)
3.  In the **Manage repository** page of a tracked repository — click on a repository/integration from the git configuration list. Look for the Webhook URL field.
    
    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/git-cloud-webhook-url-repo-list-loc(c).png?version=1&modificationDate=1617197700720&cacheVersion=1&api=v2&width=646&height=206)
4.  In the Repository Settings page of a repository in a tracked repository or a single connected repository — on the git configuration page, go to ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Show integration repositories**.
    
    *   ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/git-cloud-webhook-url-repo-cfg-tracked-repos(c).png?version=1&modificationDate=1617197700722&cacheVersion=1&api=v2&width=625&height=196)
    *   ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/jira-cloud-repo-cfg-view-tracked-repo-dlg(c).png?version=1&modificationDate=1617197700725&cacheVersion=1&api=v2&width=625&height=338)

The **Secret Key** is a secure random-generated alphanumeric string at the time of the Git Integration for Jira app installation. The user can change this to a different value by generating another secret token according to your Git host.

Use this key in the form of:

[https://gitforjiracloud.bigbrassband.com/api/1/webhook/reindex/install/](https://gitforjiracloud.bigbrassband.com/api/1/webhook/reindex/install/)**<INSTANCE\_ID>**/**<SECRET\_KEY>**

Copy the **Webhook URL** to the system clipboard by clicking the copy icon adjacent to the right. Use this URL when required by the repository web hooks setting of your git host.

|     |
| --- |
| **Example** |
| Assign your Jira base URL and Secret Key to the example URL structure: |
| [https://gitforjiracloud.bigbrassband.com/api/1/webhook/reindex/install/](https://gitforjiracloud.bigbrassband.com/api/1/webhook/reindex/install/)**x5chdqpqln0j04xcgv02zy7h9**/**vfTmXtqIFyqeCYYS3WjLIn2RRz5rHSDO** |

**HTTP Method**  
All the repositories will be reindexed if the URL specified above is activated through `GET`, `POST`, or `PUT` and the webhooks are enabled.

There is no support for other HTTP methods such as `DELETE` or `HEAD`. 

## Setting up indexing triggers (video guide)

Watch the video guide below to get familiarize with indexing triggers setup in Jira Cloud:

_Right click_ [_here_](https://bigbrassband.wistia.net/medias/4o796wnrdx) _to open this video in a new tab/window for more viewing options._

## Levels of Webhook URL

There are three (3) levels of webhook url:

1.  Install level
    
2.  Integration Level
    
3.  Repository level
    

Each level references which webhook URL was utilized to configure the webhook:

|     |
| --- |
| ### Webhook URL: Install level |
| This is the default webhook URL that is added upon the installation of the Git Integration for Jira app. For this level, events are triggered for all configured repositories.<br><br>We recommend to use this webhook URL because it's generally easy to configure and simple to understand.<br><br>**Webhook access location:**<br><br>*   Manage Git repositories sidebar, **Indexing triggers**<br>    <br>*   Click **Indexing triggers** button at top right of Manage Git repositories page<br>    <br>    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/gitcloud-indexing-trigger-webhook-url-level-1.png?version=1&modificationDate=1617197829120&cacheVersion=1&api=v2&width=584&height=303) |

|     |
| --- |
| ### Webhook URL: Integration level |
| This webhook URL triggers events only for the repositories within that integration.<br><br>**Webhook access location:**<br><br>*   Manage Git repositories page ➜ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Edit integration settings**<br>    <br>    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/webhook-level-integration.png?version=2&modificationDate=1617197854067&cacheVersion=1&api=v2&width=646&height=301) |

|     |
| --- |
| ### Webhook URL: Repository level |
| This webhook URL triggers events only for the configured repository.<br><br>**Webhook access location:**<br><br>*   Manage Git repositories page ➜ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Show integration repositories** ➜ click a repository; or<br>    <br>*   Manage Git repositories page ➜ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Edit repository settings**<br>    <br>    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/webhook-level-repository.png?version=2&modificationDate=1617197898666&cacheVersion=1&api=v2&width=646&height=599) |

For indexing to trigger, the repository URL that arrives in the webhook payload must match a repository that is in the Git Integration configuration account. However, it must also match within the webhook level.

## More indexing triggers recommended topics

*   Page:
    
    [Creating indexing triggers for a single repository](/wiki/spaces/GITCLOUD/pages/171213231/Creating+indexing+triggers+for+a+single+repository) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for GitHub repository](/wiki/spaces/GITCLOUD/pages/171377213/Adding+webhooks+for+GitHub+repository) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for GitLab repository](/wiki/spaces/GITCLOUD/pages/171377217/Adding+webhooks+for+GitLab+repository) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Webhook GitHub Organization support](/wiki/spaces/GITCLOUD/pages/171278791/Webhook+GitHub+Organization+support) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for Azure DevOps Repos | VSTS](/wiki/spaces/GITCLOUD/pages/172294150/Adding+webhooks+for+Azure+DevOps+Repos+%7C+VSTS) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for Azure DevOps Server | TFS](/wiki/spaces/GITCLOUD/pages/234782736/Adding+webhooks+for+Azure+DevOps+Server+%7C+TFS) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for Bitbucket Cloud](/wiki/spaces/GITCLOUD/pages/467271681/Adding+webhooks+for+Bitbucket+Cloud) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks to AWS CodeCommit](/wiki/spaces/GITCLOUD/pages/864288787/Adding+webhooks+to+AWS+CodeCommit) (Git Integration for Jira Cloud)