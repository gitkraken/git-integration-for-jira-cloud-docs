---

title: Setting up indexing triggers
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Setting up indexing triggers

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923023481/Setting+up+indexing+triggers>

* * *

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

The Git Integration for Jira app supports GitHub and GitLab push events to define individual repository to index. For more information, see [Creating reindex triggers manually](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/171213231/Creating+indexing+triggers+for+a+single+repository) and it’s sub-pages.

[« Setting up web linking](/wiki/spaces/GITCLOUD/pages/1923023467/Setting+up+web+linking)

[Working with SSH Keys »](/wiki/spaces/GITCLOUD/pages/1923023617/Working+with+SSH+keys)

### More related topics about getting started for git admins

*   Page:
    
    [New GitLab v10+ authentication](/wiki/spaces/GITCLOUD/pages/1923023311) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Setup GitLab Server to respond to incoming network API calls](/wiki/spaces/GITCLOUD/pages/1923023297/Setup+GitLab+Server+to+respond+to+incoming+network+API+calls) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Setting up web linking](/wiki/spaces/GITCLOUD/pages/1923023467/Setting+up+web+linking) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Setting up indexing triggers](/wiki/spaces/GITCLOUD/pages/1923023481/Setting+up+indexing+triggers) (Git Integration for Jira Cloud)