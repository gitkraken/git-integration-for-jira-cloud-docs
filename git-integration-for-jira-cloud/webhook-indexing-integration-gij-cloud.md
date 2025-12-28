---

title: Webhook indexing integration
description: Learn how to configure webhook indexing integration for Git Integration for Jira Cloud to work with git servers behind firewalls.
taxonomy:
    category: git-integration-for-jira-cloud

---

The [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/4984) app offers an integration type called **Webhook Indexing**.

The classic full feature Git service integration gives you access to all features for the connected git servers. However, it requires two-way communication originating from outside your network. Therefore, you need to allow incoming requests by updating your network/firewall settings. For more information, see [Allow list (whitelist) GIJ Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud).

Webhook indexing integration allows your connected git servers to work behind a firewall. This is its main advantage. However, the integration has limited features as stated in the Connect to your Git server features table.

<img src='/wp-content/uploads/gij-gitcloud-add-new-integration-type-webhook-indexing.png' style='height:auto; max-width:100%; display:block; margin:25px auto;' />

&nbsp;

**On this page:**
- [What is Webhook Indexing?](#what-is-webhook-indexing)
- [How does Webhook Indexing work?](#how-does-webhook-indexing-work)
- [How do I configure Webhook Indexing?](#how-do-i-configure-webhook-indexing)
- [Supported webhook indexing integrations](#supported-webhook-indexing-integrations)
- [Frequently Asked Questions](#frequently-asked-questions)

&nbsp;

* * *

&nbsp;

## What is Webhook Indexing?

<img src='/wp-content/uploads/gij-webhook-indexing-explainer.png' width=244 height=196 style='margin: 25px auto; max-width: 100%; display: block;' alt='Highlights the webhook indexing integration feature (boxed)' />

In the Classic Indexing options, all features are available (explained here: [Classic Indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud)) but require two-way communication originating from outside your network (see [Allow list (whitelist) GIJ Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud)). Webhook Indexing only requires that your Git server can make outbound Internet requests.

&nbsp;

## How does Webhook Indexing work?

With Webhook Indexing, the system uses the git metadata available in the git server webhook payload to index the commit, branch, and pull request (git tag support coming soon). A Jira administrator creates a "Webhook indexing" integration, selects the Git server type (GitHub, GitLab, Azure DevOps, etc), and then configures the Git server to send webhooks to a unique and password-protected address hosted by the Git Integration for Jira Cloud app.

&nbsp;

## How do I configure Webhook Indexing?

Configuring Webhook Indexing begins with the Jira administrator installing the [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app. Click the "Webhooks" limited feature connection option and select your git server type. In your git server, create a new webhook by copying the webhook URL and secret from the Webhook Indexing wizard. That's it! Now all future commit, branch, and pull/merge request activity will be indexed by the [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Tip!</b><br>
        Set up the webhook at the organization/group/project level in your git server to configure webhooks for multiple git repositories at once.
    </div>
    </div>
</div>

&nbsp;

## Supported webhook indexing integrations

- [GitHub webhook indexing integration](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud) &nbsp;<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>SUPPORTED</b>

- [GitLab webhook indexing integration](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud) &nbsp;<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>SUPPORTED</b>

- [Microsoft webhook indexing integration](/git-integration-for-jira-cloud/microsoft-webhook-indexing-integration-gij-cloud) &nbsp;<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>SUPPORTED</b>

- [Gerrit webhook indexing integration](/git-integration-for-jira-cloud/gerrit-webhook-indexing-integration-gij-cloud) &nbsp;<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>SUPPORTED</b>

&nbsp;

* * *

&nbsp;

## Frequently Asked Questions

### What git servers does the Webhook Indexing feature support?

<img src='/wp-content/uploads/gij-webhook-indexing-explainer-git-service-support.png' width=349 height=446 style='margin: 25px auto; max-width: 100%' alt='Shows the list of supported git host services' />

&nbsp;

### What data does a webhook send?

Each git server is different, but generally webhooks from leading git server vendors such as GitHub, GitLab, and Azure DevOps include the following:

- Repository URL
- Repository name
- Commit URL
- Commit author name
- Commit author email
- Commit SHA
- Commit message
- Files changed
- Other metadata

Webhook payloads from leading git server vendors **do not include source code**.

&nbsp;

### How is Webhook indexing different from Indexing triggers?

Previously, the application called Indexing triggers "Webhooks." Indexing triggers simply trigger a reindex of a repository in a "Classic" integration to update Jira Cloud with commits, branches, pull requests, and tags (see [Indexing Triggers](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud)).

&nbsp;

### If webhooks are sent only once by my git server, what happens if Git Integration for Jira Cloud is down?

The Webhook indexing feature automatically scales to any number of webhooks sent for indexing using enterprise-grade AWS services. A separate highly-available AWS service queues these webhooks until the system indexes them and sends them to Jira Cloud. This architecture means the system receives webhooks even if the Git Integration for Jira Cloud application is down for maintenance (see [BigBrassBand Cloud Status](https://status.bigbrassband.com)) or if indexing webhooks slows down. If the Git Integration for Jira app is unavailable for a period of time, the system processes the webhooks when the Git Integration for Jira Cloud app comes back online.

&nbsp;

### What happens if my git server is down for a period of time and suddenly sends thousands of webhooks in a short burst?

The Webhook indexing feature automatically scales to any number of webhooks sent for indexing using enterprise-grade AWS services. A separate highly-available AWS service queues these webhooks until the system indexes them and sends them to Jira Cloud. This architecture means the system receives all webhooks, even during a burst of webhook activity.

&nbsp;

### If webhooks are sent only once by my git server, what happens if the webhook format changes and the Git Integration for Jira Cloud app does not recognize the format?

The system stores webhook payloads in case they need reprocessing. Future enhancements to the Webhook Indexing features may allow Jira administrators to reprocess webhook payloads.

&nbsp;

### What if I want to delete all of my data in the Git Integration for Jira Cloud app?

Jira administrators can remove all git integration data by removing the integration. This deletes the data from BigBrassBand production servers immediately. BigBrassBand maintains backups including customer data for 7 days, after which the system deletes the backup data.

&nbsp;

### When I tested Webhook Indexing, I noticed that webhooks receive a 202 response. Why?

The HyperText Transfer Protocol (HTTP) `202 Accepted` response status code communicates that the server accepted the request for processing, but processing has not completed; in fact, processing may not have started yet. We provide this response because a highly-available AWS service (separate from the Git Integration for Jira Cloud indexing process) receives the webhooks. In practice, Jira users can view Webhook indexing updates in Jira Cloud within a few seconds.

&nbsp;

### What security precautions does BigBrassBand take to secure my data?

See: [Security & Trust](https://bigbrassband.com/security-and-trust.html)

&nbsp;

### What are the limitations of Webhook indexing?

- Webhook indexing relies on git server webhooks, which are only sent for new activity. This means the git server cannot resend previous pushes containing commit, branch, and pull request activity. Historical repository information is not available through Webhook indexing.

- Git servers have different webhook sending behaviors. GitHub limits a webhook to 1000 commits in a single push. Azure DevOps limits a webhook to 25 commits in a single push. GitLab limits a webhook to 20 commits in a single push. We recommend communicating these limitations to developers on your teams.

- Because webhooks do not include source code, the code review capabilities available in Classic Indexing integrations are not available.

- For more details, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

&nbsp;

### I have more questions about Webhook indexing

Please reach out to us at [gijsupport@gitkraken.com](mailto:gijsupport@gitkraken.com) or via our [Support Portal](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

<kbd>Last updated: December 2025</kbd>
