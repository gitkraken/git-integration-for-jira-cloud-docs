---

title: Webhook Indexing Explainer
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/4984) app now offers a new type of integration: **Webhook Indexing**.

<img src='/wp-content/uploads/gij-webhook-indexing-explainer.png' width=244 height=196 style='margin: 25px auto; max-width: 100%; display: block;' alt='Highlights the webhook indexing integration feature (boxed)' />

<br>

## What is Webhook Indexing?

In the Classic Indexing options, all features are available (explained here: [Classic Indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud) but require two-way communication originating from outside your network (see [Allow list (whitelist) BigBrassBand Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud). Webhook Indexing only requires that your Git server be able to make outbound Internet requests.

## How does Webhook Indexing work?

With Webhook Indexing, the git metadata available in the git server webhook payload is used to index the commit, branch, and pull request (git tag support coming soon). A Jira administrator creates a “Webhook indexing” integration, selects the Git server type (GitHub, GitLab, Azure DevOps, etc), and then configures the Git server to send webhooks to a unique and password protected address hosted by the Git Integration for Jira Cloud app.

## How do I configure Webhook Indexing in the Git Integration for Jira Cloud app?

Configuring Webhook Indexing begins with the Jira administrator by installing the [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app. Click on the “Webhooks” limited feature connection option and select your git server type. In your git server, create a new webhook by copying the webhook URL and secret from the Webhook Indexing wizard. And you’re done! Now all future commit, branch, and pull/merge request activity will be indexed by the [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Tip!</b><br>
        Setup the webhook at the organization/group/project level in your git server to configure webhooks for multiple git repositories at once.
    </div>
    </div>
</div>
<br>

**Specific platform instructions**:

[Webhook Indexing for GitHub](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud) &nbsp;<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>SUPPORTED</b>

[Webhook Indexing for GitLab](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud) &nbsp;<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>SUPPORTED</b>

[Webhook Indexing for Azure DevOps, VSTS and TFS](/git-integration-for-jira-cloud/microsoft-webhook-indexing-integration-gij-cloud) &nbsp;<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>SUPPORTED</b>

Webhook indexing for Gerrit &nbsp;<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>FEATURE COMING SOON</b>

## Frequently Asked Questions

### What git servers are supported by the Webhook Indexing feature?

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>As of March 26, 2021</b>

<img src='/wp-content/uploads/gij-webhook-indexing-explainer-git-service-support.png' width=349 height=446 style='margin: 25px auto; max-width: 100%' alt='Shows the list of supported git host services' />

<br>

### What data is sent in a webhook?

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

### How is Webhook indexing different from Indexing triggers?

Previously in the application we called Indexing triggers “Webhooks”). Indexing triggers are used simply to trigger a reindex of a repository in a “Classic” integration to update Jira Cloud with commits, branches, pull requests and tags (see [Indexing Triggers](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud).

### If webhooks are sent only once by my git server - what if Git Integration for Jira Cloud is down?

The Webhook indexing feature is built to automatically scale up to any number of webhooks sent for indexing using enterprise-grade AWS services . These webhooks are queued in a separate highly-available AWS service until they are indexed and sent to Jira Cloud. This architecture means that webhooks will be received even if the Git Integration for Jira Cloud application is down for maintenance (see [BigBrassBand Cloud Status](https://status.bigbrassband.com)) or if indexing webhooks slows down. In the event that the Git Integration for Jira app is unavailable for a period of time, the webhooks will be processed when the Git Integration for Jira Cloud app is back online.

### What happens if my git server is down for a period of time and suddenly send thousands of webhooks in a short burst?

The Webhook indexing feature is built to automatically scale up to any number of webhooks sent for indexing using enterprise-grade AWS services . These webhooks are queued in a separate highly-available AWS service until they are indexed and sent to Jira Cloud. This architecture means that all webhooks will be received, even in the event of a burst of webhook activity.

### If webhooks are sent only once by my git server - what if the format of the webhook changes and the Git Integration for Jira Cloud app does not recognize the format?

Webhook payloads are stored in case they need to be reprocessed. Future enhancements to the Webhook Indexing features may allow Jira administrators to reprocess webhook payloads.

### What if I want to delete all of my data in the Git Integration for Jira Cloud app?

Jira administrators can remove all git integration data by removing the integration. This deletes the data from BigBrassBand production servers immediately. BigBrassBand does maintain backups including customer data for 7 days after which the backup data is deleted.

### When I tested Webhook Indexing, I noticed that webhooks are received with a 202 response. Why?

The HyperText Transfer Protocol (HTTP) `202 Accepted` response status code communicates that the request has been accepted for processing, but the processing has not been completed; in fact, processing may not have started yet. We provide this response because webhooks are received by a highly-available AWS services separate from the Git Integration for Jira Cloud indexing process. In practice, Webhook indexing updates can be viewed in Jira Cloud within a few seconds by Jira users.

### What security precautions does BigBrassBand take to secure my data?

See: [Security & Trust](https://bigbrassband.com/security-and-trust.html)

### What are the limitations of Webhook indexing?

*   Webhook indexing relies on git server webhook sending which are only sent for new activity. This means that previous pushes containing commit, branch, and pull request activity cannot be resent. Historical repository information is not available through Webhook indexing.

*   Git servers have a variety of webhook sending behaviors. GitHub will limit a webhook to 1000 commits in a single push. Azure DevOps limits a webhook to 25 commits in a single push. GitLab limits a webhook to 20 commits in a single push. We recommend communicating these limitations to developers on your teams.

*   Because no source code is included in the webhook payload, the code review capabilities available in Classic Indexing integrations are not available.

*   For more - see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).


### I have more questions about Webhook indexing

Please reach out to us at [support@gitkraken.com](mailto:support@gitkraken.com) or via our [Support Portal](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

