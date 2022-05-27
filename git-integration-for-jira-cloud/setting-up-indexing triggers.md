---

title: Setting up indexing triggers
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Before you can use indexing triggers (formerly webhooks), it needs to be enabled in the Git Integration for Jira indexing triggers settings.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923023481/gitcloud-sidebar-indexing-triggers-loc.png?version=1&modificationDate=1630926067805&cacheVersion=1&api=v2&width=680&height=357)

Access the Git Integration for Jira app indexing triggers configuration page:

1.  Go to Jira dashboard menu Apps ➜ **Git Integration: Manage Git repositories**.

2.  On the sidebar under _Git Integration for Jira_, click **Indexing triggers**.

3.  Click the toggle button to enable this feature.


![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923023481/gitcloud-indexing-triggers-cfg-enable.png?version=1&modificationDate=1630925521030&cacheVersion=1&api=v2)

On this page, you can also find the **Webhook URL** and the **Secret key** for use with your git host webhook configuration. The secret key is a secure random-generated alphanumeric string at the time of the Git Integration for Jira app installation.

Disabling, reinstalling or even installing another version of the Git Integration for Jira app does not change the value of the key (for security purposes and unique identity). Administrators can manually change this key to a different value by generating another secret token according to your Git host and organization policies.

For instance:

```java
ruby -rsecurerandom -e 'puts SecureRandom.hex(32)'
```


The secret key also has the same restrictions on the valid set of characters as a regular URL. Invalid characters such as spaces, slashes, colon, etc. are not allowed. The default recommended length for the secret key is 32 chars and the maximum length is 255 chars.

## More information on webhooks configuration

For detailed information on setting up webhooks for supported git hosts, see Indexing triggers.

The Git Integration for Jira app supports GitHub and GitLab push events to define individual repository to index. For more information, see [Creating reindex triggers manually](/git-integration-for-jira-cloud/creating-indexing-triggers-for-a-single-repository/) and it’s sub-pages.

[« Setting up web linking](/git-integration-for-jira-cloud/setting-up-web-linking/)

[Working with SSH Keys »](/git-integration-for-jira-cloud/working-with-ssh-keys-gij-cloud/)

