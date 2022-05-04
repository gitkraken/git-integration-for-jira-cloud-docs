---

title: Webhook Indexing Explainer
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Webhook Indexing Explainer

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1422819484/Webhook+Indexing+Explainer>

* * *

The [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/4984) app now offers a new type of integration: **Webhook Indexing**.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1422819484/CleanShot2021-03-26%20at%2021.37.36@2x-20210327-013823.png?version=1&modificationDate=1616809113344&cacheVersion=1&api=v2)

## What is Webhook Indexing?

In the Classic Indexing options, all features are available (explained here: [Classic Indexing Explainer](/wiki/spaces/GITCLOUD/pages/183369754/Classic+Indexing+Explainer)) but require two-way communication originating from outside your network (see [Allow list (whitelist) BigBrassBand Cloud](/wiki/spaces/GITCLOUD/pages/121241614/Allow+list+%28whitelist%29+BigBrassBand+Cloud)). Webhook Indexing only requires that your Git server be able to make outbound Internet requests.

## How does Webhook Indexing work?

With Webhook Indexing, the git metadata available in the git server webhook payload is used to index the commit, branch, and pull request (git tag support coming soon). A Jira administrator creates a “Webhook indexing” integration, selects the Git server type (GitHub, GitLab, Azure DevOps, etc), and then configures the Git server to send webhooks to a unique and password protected address hosted by the Git Integration for Jira Cloud app.

## How do I configure Webhook Indexing in the Git Integration for Jira Cloud app?

Configuring Webhook Indexing begins with the Jira administrator by installing the [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app. Click on the “Webhooks” limited feature connection option and select your git server type. In your git server, create a new webhook by copying the webhook URL and secret from the Webhook Indexing wizard. And you’re done! Now all future commit, branch, and pull/merge request activity will be indexed by the [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app.

Tip: Setup the webhook at the organization/group/project level in your git server to configure webhooks for multiple git repositories at once.

**Specific platform instructions**:

[Webhook Indexing for GitHub](/wiki/spaces/GITCLOUD/pages/1494646787/GitHub+webhook+indexing+integration) SUPPORTED

[Webhook Indexing for GitLab](/wiki/spaces/GITCLOUD/pages/1503494176/GitLab+webhook+indexing+integration) SUPPORTED

[Webhook Indexing for Azure DevOps, VSTS and TFS](/wiki/spaces/GITCLOUD/pages/1509032469/Microsoft+webhook+indexing+integration) SUPPORTED

Webhook indexing for Gerrit FEATURE COMING SOON

## Frequently Asked Questions

### 1\. What git servers are supported by the Webhook Indexing feature? (as of March 26, 2021)

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1422819484/CleanShot2021-03-26%20at%2021.32.32@2x-20210327-013237.png?version=1&modificationDate=1616808763631&cacheVersion=1&api=v2)

### 2\. What data is sent in a webhook?

Each git server is different, but generally the webhooks sent by leading git server vendors such as GitHub, GitLab, and Azure DevOps include the following:

*   Repository URL
    
*   Repository name
    
*   Commit URL
    
*   Commit author name
    
*   Commit author email
    
*   Commit SHA
    
*   Commit message
    
*   Files changed
    
*   and other meta-data
    

Webhook payloads by the leading git server vendors **do not include source code**.

### 3\. How is Webhook indexing different from Indexing triggers?

Previously in the application we called Indexing triggers “Webhooks”). Indexing triggers are used simply to trigger a reindex of a repository in a “Classic” integration to update Jira Cloud with commits, branches, pull requests and tags (see [Indexing Triggers](/wiki/spaces/GITCLOUD/pages/171475219/Indexing+Triggers)).

### 4\. If webhooks are sent only once by my git server - what if Git Integration for Jira Cloud is down?

The Webhook indexing feature is built to automatically scale up to any number of webhooks sent for indexing using enterprise-grade AWS services . These webhooks are queued in a separate highly-available AWS service until they are indexed and sent to Jira Cloud. This architecture means that webhooks will be received even if the Git Integration for Jira Cloud application is down for maintenance (see [BigBrassBand Cloud Status](https://status.bigbrassband.com)) or if indexing webhooks slows down. In the event that the Git Integration for Jira app is unavailable for a period of time, the webhooks will be processed when the Git Integration for Jira Cloud app is back online.

### 5\. What happens if my git server is down for a period of time and suddenly send thousands of webhooks in a short burst?

The Webhook indexing feature is built to automatically scale up to any number of webhooks sent for indexing using enterprise-grade AWS services . These webhooks are queued in a separate highly-available AWS service until they are indexed and sent to Jira Cloud. This architecture means that all webhooks will be received, even in the event of a burst of webhook activity.

### 6\. If webhooks are sent only once by my git server - what if the format of the webhook changes and the Git Integration for Jira Cloud app does not recognize the format?

Webhook payloads are stored in case they need to be reprocessed. Future enhancements to the Webhook Indexing features may allow Jira administrators to reprocess webhook payloads.

### 7\. What if I want to delete all of my data in the Git Integration for Jira Cloud app?

Jira administrators can remove all git integration data by removing the integration. This deletes the data from BigBrassBand production servers immediately. BigBrassBand does maintain backups including customer data for 7 days after which the backup data is deleted.

### 8\. When I tested Webhook Indexing, I noticed that webhooks are received with a 202 response. Why?

The HyperText Transfer Protocol (HTTP) `202 Accepted` response status code communicates that the request has been accepted for processing, but the processing has not been completed; in fact, processing may not have started yet. We provide this response because webhooks are received by a highly-available AWS services separate from the Git Integration for Jira Cloud indexing process. In practice, Webhook indexing updates can be viewed in Jira Cloud within a few seconds by Jira users.

### 9\. What security precautions does BigBrassBand take to secure my data?

See: [Security & Trust](https://bigbrassband.com/security-and-trust.html)

### 10\. What are the limitations of Webhook indexing?

*   Webhook indexing relies on git server webhook sending which are only sent for new activity. This means that previous pushes containing commit, branch, and pull request activity cannot be resent. Historical repository information is not available through Webhook indexing.
    
*   Git servers have a variety of webhook sending behaviors. GitHub will limit a webhook to 1000 commits in a single push. Azure DevOps limits a webhook to 25 commits in a single push. GitLab limits a webhook to 20 commits in a single push. We recommend communicating these limitations to developers on your teams.
    
*   Because no source code is included in the webhook payload, the code review capabilities available in Classic Indexing integrations are not available.
    
*   For more - see [Feature matrix of Git Integration for Jira Cloud](/wiki/spaces/GITCLOUD/pages/1470398499/Feature+matrix+of+Git+Integration+for+Jira+Cloud).
    

### 11\. I have more questions about Webhook indexing

Please reach out to us at [support@bigbrassband.com](mailto:support@bigbrassband.com) or via our [Support Portal](https://bigbrassband.atlassian.net/servicedesk/customer/portals).