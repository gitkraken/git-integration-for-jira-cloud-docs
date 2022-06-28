---

title: Adding webhooks for GitLab repository
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Merge request webhooks are now supported. [See details](/git-integration-for-jira-cloud/adding-webhooks-for-gitlab-repository/) on this page.

Supported webhook events:

*   Push events

*   Merge request events


Git Integration for Jira Cloud app now supports **GitLab System Hooks** (menu Admin Area ➜ System Hooks ➜ _Merge Request events)_. However, it is only available for self-hosted GitLab instances. We highly recommend that Jira administrators should use this feature as it greatly reduces the amount of configuration time to setup webhooks.

_Right click_ [_here_](https://bigbrassband.wistia.net/medias/trp1frsfl4) _to open this video in a new tab/window for more viewing options._

Before you can proceed with the steps outlined on this guide, webhooks must be enabled in the Git Integration for Jira app repository configuration for your Jira Cloud instance.  For more details, see [**Indexing Triggers - Getting Started**](/git-integration-for-jira-cloud/Indexing-Triggers).

## Setting up webhooks for GitLab

Configure webhook by logging in to your GitLab account:

1.  Select a repository.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/171377217/web-hooks-gitlab-settings(c).png?version=1&modificationDate=1617193057400&cacheVersion=1&api=v2)
2.  Go to the settings page by clicking **Settings** on the sidebar.

3.  Select **Webhooks**. The following page is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171377217/web-hooks-gitlab-settings-add(c).png?version=1&modificationDate=1617193057409&cacheVersion=1&api=v2&width=584&height=867)
4.  Paste the obtained _**Secret URL**_ from the _Git Integration for Jira_ app ➜ **Webhooks** page into the _**Payload URL**_ field.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171377217/jira-cloud-webhook-url-loc(c1).png?version=1&modificationDate=1617193057414&cacheVersion=1&api=v2&width=646&height=430)
5.  Select the _**Push events**_ as a triggering event option. This is the default option when creating a new webhook.

6.  Click **Add webhook** to save the new webhook settings.


## Merge request event webhook

The Git Integration for Jira app supports GitLab merge request webhooks now.

You will need to enable two (2) event triggers in your GitLab webhooks configuration _(Repo ➜ Settings ➜ Webhooks)_ for it to work properly. Select both "**Push events**" and "**Merge request events**" triggers as outlined above in **step** **5**.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171377217/gitlab-merge-request-event-trigger-webhook.png?version=2&modificationDate=1617193057420&cacheVersion=1&api=v2&width=566&height=152)