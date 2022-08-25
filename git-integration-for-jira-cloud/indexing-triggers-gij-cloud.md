---

title: Indexing Triggers
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
**What’s on this page:**

- [What are indexing triggers and why use them?](#what-are-indexing-triggers-and-why-use-them)
- [Do I need to set up indexing triggers?](#do-i-need-to-set-up-indexing-triggers)
- [Getting started](#getting-started)
- [Where to get the indexing triggers webhook URL?](#where-to-get-the-indexing-triggers-webhook-url)
- [Setting up indexing triggers (video guide)](#setting-up-indexing-triggers-video-guide)
- [Levels of Webhook URL](#levels-of-webhook-url)
  - [Webhook URL: Install level](#webhook-url-install-level)
  - [Webhook URL: Integration level](#webhook-url-integration-level)
  - [Webhook URL: Repository level](#webhook-url-repository-level)

* * *

## What are indexing triggers and why use them?

Indexing triggers (webhooks) can be an extremely powerful tool that can be configured to activate an immediate re-index of your repositories from remote systems. Your git server can send this near real-time data to Jira when your git data changes. This results in a much faster indexing time where you don’t have to wait for the regular polling interval (see [**General settings**](/git-integration-for-jira-cloud/general-settings-gij-cloud).

Webhooks can be initiated whenever certain actions are performed. For example, you can configure a webhook to execute when:

*   a new commit is pushed

*   a pull request is opened

*   a branch is merged


You can create indexing triggers for individual repositories. Most git providers will also allow you to create webhooks at an account-level or org-level.

## Do I need to set up indexing triggers?

By configuring indexing triggers to initiate reindexing, Jira will more often have up-to-date information.

Without setting up indexing triggers, you will be relying on the default polling of the app which is unchangeable by non-Jira administrators. Jira users will have to wait for the default interval for updates (usually 5 minutes) – which means users will not quickly see new commits or pull requests until the next indexing interval.

## Getting started

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Important</b><br>
        To use the indexing triggers feature, it must be enabled in the Manage (Git) repositories ➜ <b>Indexing triggers</b> page.
    </div>
    </div>
</div>
<br>


Configure indexing triggers to activate immediate reindex of your repositories from remote systems.

1.  From your Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Repository browser**. (_Alternatively, go to Jira Settings ➜ Apps_).

2.  On the sidebar, click **Indexing triggers**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/171475219/gitcloud-new-webhooks-settings-page(c).png?version=1&modificationDate=1617197700707&cacheVersion=1&api=v2)

3.  Enable/disable the indexing trigger feature by clicking on the **Indexing triggers enabled** toggle switch.

## Where to get the indexing triggers webhook URL?

The webhooks URL can be accessed on the following locations:

1.  From your Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Repository browser**. On the sidebar, click **Indexing triggers**. (_Alternatively, go to Jira Settings_ ➜ _Apps. On the sidebar, click Indexing triggers_).

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/gitcloud-indexing-triggers-loc-01(c).png?version=1&modificationDate=1617197700714&cacheVersion=1&api=v2&width=646&height=301)

2.  On the Manage Git repositories configuration page, click the Indexing triggers button at the top right of the page.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/gitcloud-indexing-triggers-loc-02(c).png?version=1&modificationDate=1617197700717&cacheVersion=1&api=v2&width=646&height=414)

3.  In the **Manage repository** page of a tracked repository — click on a repository/integration from the git configuration list. Look for the Webhook URL field.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/git-cloud-webhook-url-repo-list-loc(c).png?version=1&modificationDate=1617197700720&cacheVersion=1&api=v2&width=646&height=206)

4.  In the Repository Settings page of a repository in a tracked repository or a single connected repository — on the git configuration page, go to Actions ➜ **Show integration repositories**.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/git-cloud-webhook-url-repo-cfg-tracked-repos(c).png?version=1&modificationDate=1617197700722&cacheVersion=1&api=v2&width=625&height=196)

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/jira-cloud-repo-cfg-view-tracked-repo-dlg(c).png?version=1&modificationDate=1617197700725&cacheVersion=1&api=v2&width=625&height=338)

The **Secret Key** is a secure random-generated alphanumeric string at the time of the Git Integration for Jira app installation. The user can change this to a different value by generating another secret token according to your Git host.

Use this key in the form of:

https://gitforjiracloud.bigbrassband.com/api/1/webhook/reindex/install/**\<INSTANCE\_ID\>**/**\<SECRET\_KEY\>**

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Copy the <b>Webhook URL</b> to the system clipboard by clicking the copy icon adjacent to the right. Use this URL when required by the repository web hooks setting of your git host.
    </div>
    </div>
</div>
<br>

**Example**
Assign your Jira base URL and Secret Key to the example URL structure:
`https://gitforjiracloud.bigbrassband.com/api/1/webhook/reindex/install/`**x5chdqpqln0j04xcgv02zy7h9**`/`**vfTmXtqIFyqeCYYS3WjLIn2RRz5rHSDO**

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>HTTP Method</b><br>
        All the repositories will be reindexed if the URL specified above is activated through <code>GET</code>, <code>POST</code>, or <code>PUT</code> and the webhooks are enabled.<br><br>
        There is no support for other HTTP methods such as <code>DELETE</code> or <code>HEAD</code>.
    </div>
    </div>
</div>
<br>

## Setting up indexing triggers (video guide)

Watch the video guide below to get familiarize with indexing triggers setup in Jira Cloud:

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/4o796wnrdx?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/4o796wnrdx'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

## Levels of Webhook URL

There are three (3) levels of webhook url:

1.  Install level

2.  Integration Level

3.  Repository level


Each level references which webhook URL was utilized to configure the webhook:

### Webhook URL: Install level

This is the default webhook URL that is added upon the installation of the Git Integration for Jira app. For this level, events are triggered for all configured repositories.

We recommend to use this webhook URL because it's generally easy to configure and simple to understand.

**Webhook access location:**

*   Manage Git repositories sidebar, **Indexing triggers**

*   Click **Indexing triggers** button at top right of Manage Git repositories page

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/gitcloud-indexing-trigger-webhook-url-level-1.png?version=1&modificationDate=1617197829120&cacheVersion=1&api=v2&width=584&height=303)

    <br>

### Webhook URL: Integration level

This webhook URL triggers events only for the repositories within that integration.

**Webhook access location:**

*   Manage Git repositories page ➜ Actions ➜ **Edit integration settings**

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/webhook-level-integration.png?version=2&modificationDate=1617197854067&cacheVersion=1&api=v2&width=646&height=301)

<br>

### Webhook URL: Repository level

This webhook URL triggers events only for the configured repository.

**Webhook access location:**

*   Manage Git repositories page ➜ Actions ➜ **Show integration repositories** ➜ click a repository; or

*   Manage Git repositories page ➜ Actions ➜ **Edit repository settings**

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171475219/webhook-level-repository.png?version=2&modificationDate=1617197898666&cacheVersion=1&api=v2&width=646&height=599)

    <br>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For indexing to trigger, the repository URL that arrives in the webhook payload must match a repository that is in the Git Integration configuration account. However, it must also match within the webhook level.
    </div>
    </div>
</div>

