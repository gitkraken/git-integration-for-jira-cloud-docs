---

title: Indexing triggers (formerly Webhooks)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Indexing triggers allows immediate reindex of your repositories from remote systems, where near real-time data is sent to Jira whenever your git data changes. This provides Jira with more often up-to-date information. Setting up indexing triggers will result in a much faster indexing time where you don’t have to wait for the regular polling interval (_every 5 minutes_).

Most git providers will also allow you to create webhooks at an account-level or org-level. For more information about this topic, see [**About GitLab Webhooks**](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/web_hooks/web_hooks.md).

## Getting started

Setup webhooks for your configured integration/repositories from remote systems by enabling the feature first.

<img src='/wp-content/uploads/gij-gitcloud-indexing-triggers-loc.png' style='display:block;margin:25px auto;max-width:100%' />

1.  From your Jira dashboard, go to the **Apps** menu.

2.  Click **Git Integration:** **Manage Git repositories**.

3.  On the sidebar, click **Indexing triggers** to open the Webhooks configuration page.

4.  Turn on the webhook feature by switching the **Indexing triggers enabled** setting to `ON`.


<img src='/wp-content/uploads/gij-gitcloud-indexing-triggers-enable.png' style='display:block;margin:25px auto;max-width:100%' />

Use the **Webhook URL** to setup webhook for your remote git host.

The **Secret Key** is a secure random-generated alphanumeric string at the time of the Git Integration for Jira app installation. The user can change this to a different value by generating another secret token according to your Git host.

Use this key in the form of:

```java
<JIRA_BASE_URL>/git/webhook/reindex/<SECRET_KEY>
```

All the repositories will be reindexed if the URL specified above is activated through `GET`, `POST`, or `PUT` and the webhooks are enabled.

There is no support for other HTTP methods such as  `DELETE`  or  `HEAD` .


See [About indexing triggers in Jira Cloud](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud) for a more detailed information on this topic.

For more information about triggers and event types, see [Creating reindex triggers for a single repository](/git-integration-for-jira-cloud/creating-indexing-triggers-for-a-single-repository-gij-cloud).

<br>
<br>
<hr>
<br>
<br>

[**Prev:** Reindexing](/git-integration-for-jira-cloud/reindexing-gij-cloud/)

[**Next:** Localization support](/git-integration-for-jira-cloud/localization-support-gij-cloud/)

