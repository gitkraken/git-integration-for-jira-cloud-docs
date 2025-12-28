---

title: Indexing triggers (formerly Webhooks)
description: How to configure indexing triggers for faster repository updates
taxonomy:
    category: git-integration-for-jira-cloud

---

Indexing triggers allow immediate reindexing of your repositories from remote systems, sending near real-time data to Jira whenever your git data changes. This provides Jira with more frequently updated information. Setting up indexing triggers results in much faster indexing time where you don't have to wait for the regular polling interval (every 5 minutes).

Most git providers also allow you to create webhooks at an account-level or org-level. For more information about this topic, see [**About GitLab Webhooks**](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/web_hooks/web_hooks.md).

## Getting Started

Set up webhooks for your configured integrations/repositories from remote systems by enabling the feature first.

![](/wp-content/uploads/gij-gitcloud-indexing-triggers-loc-new.png)

1.  From your Jira dashboard, go to the **Apps** menu.

2.  Click **Git Integration: Manage Git repositories**.

3.  On the sidebar, click **Indexing triggers** to open the Webhooks configuration page.

4.  Enable the webhook feature by switching the **Indexing triggers enabled** setting to `ON`.

<img src='/wp-content/uploads/gij-gitcloud-indexing-triggers-enable.png' style='display:block;margin:25px auto;max-width:100%' />

Use the **Webhook URL** to set up webhooks for your remote git host.

The **Secret Key** is a secure random-generated alphanumeric string created at the time of Git Integration for Jira app installation. You can change this to a different value by generating another secret token according to your Git host.

Use this key in the form of:

```java
<JIRA_BASE_URL>/git/webhook/reindex/<SECRET_KEY>
```

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        All repositories are reindexed if the URL specified above is activated through <code>GET</code>, <code>POST</code>, or <code>PUT</code> and webhooks are enabled.
        <p style='margin-bottom:-10px'>There is no support for other HTTP methods such as <code>DELETE</code> or <code>HEAD</code>.</p>
    </div>
    </div>
</div>

See [About indexing triggers in Jira Cloud](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud) for more detailed information on this topic.

For more information about triggers and event types, see [Creating reindex triggers for a single repository](/git-integration-for-jira-cloud/creating-indexing-triggers-for-a-single-repository-gij-cloud).

&nbsp;
* * *
&nbsp;

[**Prev:** Reindexing](/git-integration-for-jira-cloud/reindexing-gij-cloud/)

[**Next:** Localization support](/git-integration-for-jira-cloud/localization-support-gij-cloud/)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
