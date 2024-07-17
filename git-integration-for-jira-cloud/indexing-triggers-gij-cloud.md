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

<br>
<br>
<hr>
<br>
<br>


## What are indexing triggers and why use them?

Indexing triggers (webhooks) can be an extremely powerful tool that can be configured to activate an immediate re-index of your repositories from remote systems. Your git server can send this near real-time data to Jira when your git data changes. This results in a much faster indexing time where you don’t have to wait for the regular polling interval (see [**General settings**](/git-integration-for-jira-cloud/general-settings-gij-cloud)).

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

    ![](/wp-content/uploads/gij-gitcloud-new-webhooks-settings-page-c.png)

3.  Enable/disable the indexing trigger feature by clicking on the **Indexing triggers enabled** toggle switch.

## Where to get the indexing triggers webhook URL?

The webhooks URL can be accessed on the following locations:

1.  From your Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Repository browser**. On the sidebar, click **Indexing triggers**. (_Alternatively, go to Jira Settings_ ➜ _Apps. On the sidebar, click Indexing triggers_).

    ![](/wp-content/uploads/gij-gitcloud-indexing-triggers-loc-01c.png)

2.  On the Manage Git repositories configuration page, click the Indexing triggers button at the top right of the page.

    ![](/wp-content/uploads/gij-gitcloud-indexing-triggers-loc-02c.png)

3.  In the **Manage repository** page of a tracked repository — click on a repository/integration from the git configuration list. Look for the Webhook URL field.

    ![](/wp-content/uploads/gij-git-cloud-webhook-url-repo-list-loc-c.png)

4.  In the Repository Settings page of a repository in a tracked repository or a single connected repository — on the git configuration page, go to <img src='/wp-content/uploads/actions-icon.png' Actions ➜ **Show integration repositories**.

<img src='/wp-content/uploads/gij-git-cloud-webhook-url-repo-cfg-tracked-repos-c.png' style='display:block;margin:25px auto 0 auto;max-width:100%' />

<img src='/wp-content/uploads/gij-jira-cloud-repo-cfg-view-tracked-repo-dlg-c.png' style='display:block;margin:0 auto 25px auto;max-width:100%' />

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

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/4o796wnrdx?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:40px;'>
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

![](/wp-content/uploads/gij-gitcloud-indexing-triggers-access-locations.png)

*   Manage Git repositories sidebar, **Indexing triggers**

*   On the **Productivity** panel on the Administrator Toolbox, click **Configure indexing triggers**

<img src='/wp-content/uploads/gij-gitcloud-indexing-trigger-webhook-url-level-1.png' style='display:block;margin:25px auto;max-width:100%' />

<br>

### Webhook URL: Integration level

This webhook URL triggers events only for the repositories within that integration.

**Webhook access location:**

*   Manage integrations page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit integration ➜ **Feature Settings** (sidebar)

    ![](/wp-content/uploads/gij-gitcloud-indexing-triggers-integration-level-01.png)    

*   Manage integrations page ➜ click an integration ➜ **Feature Settings** (sidebar)

    ![](/wp-content/uploads/gij-gitcloud-indexing-triggers-integration-level-03.png)

![](/wp-content/uploads/gij-gitcloud-indexing-triggers-integration-level-02.png)

<p>&nbsp;</p>

### Webhook URL: Repository level

This webhook URL triggers events only for the configured repository.

**Webhook access location:**

*   Manage repositories page ➜ click a repository; or

    <img src='/wp-content/uploads/gij-gitcloud-indexing-triggers-repo-level-01.png' style='margin:15px 0 25px 0' />

*   Manage Git repositories page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit repository settings**

<img src='/wp-content/uploads/gij-gitcloud-indexing-triggers-repo-level-02.png' style='display:block;margin:25px auto 35px auto;max-width:100%' />

<br>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px 0 0; font-size: small;'>NEW UPDATE!</b><br>
        Repository IDs are extracted from all webhook types (even from the install level ones) and only the repositories specified in the webhook will be indexed. This implementation prevents indexing all repositories in integrations that especially important for large integrations.
    </div>
    </div>
</div>
<br>

