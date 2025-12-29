---
title: Webhook indexing integration
description: Learn how to configure webhook indexing integration for Git Integration for Jira Cloud to work with git servers behind firewalls.
taxonomy:
    category: git-integration-for-jira-cloud
---

Webhook indexing integration enables your git servers to work behind a firewall while still sending git data to Jira Cloud.

**On this page:**
- [Understand webhook indexing](#understand-webhook-indexing)
- [Configure webhook indexing](#configure-webhook-indexing)
- [Supported integrations](#supported-integrations)
- [Frequently asked questions](#frequently-asked-questions)

&nbsp;
* * *
&nbsp;

## Understand Webhook Indexing

<img src='/wp-content/uploads/gij-webhook-indexing-explainer.png' width=244 height=196 style='margin: 25px auto; max-width: 100%; display: block;' alt='Highlights the webhook indexing integration feature (boxed)' />

### Classic vs webhook indexing

Classic indexing provides all features but requires two-way communication originating from outside your network. You must allow incoming requests by updating your network/firewall settings (see [Allow list (whitelist) GIJ Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud)).

Webhook indexing only requires that your git server can make outbound Internet requests. This is its main advantage for servers behind firewalls. However, this integration type has limited features.

<img src='/wp-content/uploads/gij-gitcloud-add-new-integration-type-webhook-indexing.png' style='height:auto; max-width:100%; display:block; margin:25px auto;' />

### How webhook indexing works

The system uses git metadata from webhook payloads to index commits, branches, and pull requests (git tag support coming soon):

1. A Jira administrator creates a webhook indexing integration and selects the git server type
2. The administrator configures the git server to send webhooks to a unique, password-protected address
3. Future commit, branch, and pull/merge request activity is automatically indexed

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Set up webhooks at the organization/group/project level in your git server to configure multiple repositories at once.
    </div>
    </div>
</div>

&nbsp;

## Configure Webhook Indexing

1. Install the [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app.

2. Click the **Webhooks** limited feature connection option.

3. Select your git server type.

4. Copy the webhook URL and secret from the wizard.

5. Create a new webhook in your git server using the copied information.

&nbsp;

## Supported Integrations

| Git Service | Status |
|-------------|--------|
| [GitHub webhook indexing](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud) | Supported |
| [GitLab webhook indexing](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud) | Supported |
| [Microsoft webhook indexing](/git-integration-for-jira-cloud/microsoft-webhook-indexing-integration-gij-cloud) | Supported |
| [Gerrit webhook indexing](/git-integration-for-jira-cloud/gerrit-webhook-indexing-integration-gij-cloud) | Supported |

&nbsp;
* * *
&nbsp;

## Frequently Asked Questions

### What git servers does webhook indexing support?

<img src='/wp-content/uploads/gij-webhook-indexing-explainer-git-service-support.png' width=349 height=446 style='margin: 25px auto; max-width: 100%' alt='Shows the list of supported git host services' />

### What data does a webhook send?

Webhooks from GitHub, GitLab, and Azure DevOps typically include:

- Repository URL and name
- Commit URL, SHA, author, and message
- Files changed
- Other metadata

Webhook payloads **do not include source code**.

### How is webhook indexing different from indexing triggers?

Indexing triggers (previously called "Webhooks") trigger a reindex of repositories in Classic integrations. Webhook indexing is a separate integration type that receives git data directly from webhook payloads. See [Indexing Triggers](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud) for more information.

### What happens if Git Integration for Jira Cloud is down?

The webhook indexing feature uses enterprise-grade AWS services with automatic scaling. A separate highly-available service queues webhooks until the system indexes them. Webhooks received during maintenance are processed when the app comes back online.

### What happens during a burst of webhook activity?

The architecture handles any number of webhooks using AWS services that automatically scale. All webhooks are received and queued, even during bursts.

### What happens if the webhook format changes?

The system stores webhook payloads for potential reprocessing. Future enhancements may allow Jira administrators to reprocess stored payloads.

### How do I delete all my data?

Remove the integration to delete all git integration data from BigBrassBand production servers immediately. Backups containing customer data are maintained for 7 days, then deleted.

### Why do webhooks receive a 202 response?

The HTTP `202 Accepted` response indicates the server accepted the request for processing, but processing may not have started yet. A separate AWS service receives webhooks before they're processed. In practice, updates appear in Jira within seconds.

### What security precautions does BigBrassBand take?

See [Security & Trust](https://bigbrassband.com/security-and-trust.html).

### What are the limitations?

- **No historical data**: Webhooks are only sent for new activity. Previous commits, branches, and pull requests are not available.
- **Commit limits per push**: GitHub limits 1000 commits, Azure DevOps limits 25 commits, GitLab limits 20 commits per webhook.
- **No code review**: Source code is not included in webhooks, so code review features are unavailable.
- See [Feature matrix](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud) for details.

### I have more questions

Contact us at [gijsupport@gitkraken.com](mailto:gijsupport@gitkraken.com) or via our [Support Portal](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

<kbd>Last updated: December 2025</kbd>
