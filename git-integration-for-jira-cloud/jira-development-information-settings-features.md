---

title: Jira Development Information settings feature
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Access this setting on the dashboard menu via Apps ➜ Git Integration: Manage Git repositories ➜ (sidebar) **General settings**. Alternatively, go to dashboard ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Jira Settings ➜ Apps ➜ (sidebar) **General settings**.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1941373113/gitcloud-gencfg-jira-dev-info-settings.png?version=1&modificationDate=1631349902457&cacheVersion=1&api=v2)

There are four Jira Development Information settings that Jira administrators should aware of:

### Send Development Information to Jira Cloud

Enabling _**Send Development Information to Jira Cloud**_ setting will send new commit/branch/pull request data to Jira Cloud where it is processed and made available in a variety of views and features (described [here](/wiki/spaces/GITCLOUD/pages/643203115/Development+Information+Views) and [here](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/138772493/Jira+Development+Information#What-other-features-are-enabled-by-Jira-Development-Information%3F)).

Only newly received data is sent to Jira Cloud - so if you wish to see historical data in these views - remove the current repositories/integrations in Manage Git repositories and re-connect.

### Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers

The _**Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers**_ setting engages the native Jira Cloud Smart Commit processing (only `#time`, `#comment`, and `#transitions`) as well as enables **Automatic workflow triggers**.

For more information - see our [Smart Commits^](https://bigbrassband.com/git-integration-for-jira/documentation/smart-commits.html) or [Automatic workflow triggers](/wiki/spaces/GITCLOUD/pages/1940783182/Automatic+Workflow+Triggers) documentation.

### Enable Git Integration app Smart Commits

The _**Enable Git Integration app Smart Commits**_ setting engages BigBrassBand's Git Integration Smart Commit processing (`#time`, `#comment`, `#transitions`, and `#label`).

For more information - see our [Smart Commit documentation^](https://bigbrassband.com/git-integration-for-jira/documentation/smart-commits.html).

### Advanced: Clear Development Information

Behind the "Advanced" link is a function button that gives the Jira administrator the ability to clear out all Development Information associated with the Git Integration for Jira app.

Note that this action takes some time to process and Development Information may be visible in places until the process finishes. Expect the process to take up to 1 hour.

