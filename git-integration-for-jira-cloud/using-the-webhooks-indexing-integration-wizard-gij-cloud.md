---
title: "Using the Webhook indexing integration wizard"
description: "How to use the Webhook indexing integration wizard for Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Using the Webhook indexing integration wizard"
content_type: "reference"
audience: "all"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "all"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "reference"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Webhook indexing integration enables git servers behind firewalls to send data to Jira. This integration type has limited features, including no branch or pull/merge request creation from Jira.

| Integration path | Best for | Repository scope | Main limitation | Notes |
| :--- | :--- | :--- | :--- | :--- |
| Webhook indexing integration wizard | Firewalled git servers that can send outbound webhook requests | Multiple repositories | No branch or pull/merge request creation from Jira | Use when inbound access from Jira Cloud is not practical |
| Git service integration wizard | Standard multi-repository integrations | Multiple repositories | Requires the standard integration path rather than direct webhook-only indexing | Better when the full feature set is needed |
| Single git integration wizard | One specific repository over SSH or HTTP(S) | Single repository | Manual single-repository scope | Better when you only need one repository |

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Supported git host services: GitHub, GitLab, Microsoft, and Gerrit.
    </div>
    </div>
</div>

&nbsp;

## How to select a git service for webhook indexing

1. Go to the **Manage integration** page.
2. Click **Add integration**.
3. Select a supported Git service from the list.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-integrations-page-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## How to choose the webhook indexing integration type

1. Click the **Webhook indexing** integration type.
2. Click **Add integration** to proceed.

<img src='/wp-content/uploads/gij-gitcloud-add-new-integration-type-webhook-indexing-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## How to configure the webhook in your git host before finishing the wizard

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Important:</b> Don't click <b>Finish</b> yet! First, set up webhooks in your git host service using the information on this screen.
    </div>
    </div>
</div>

<img src='/wp-content/uploads/gij-gitcloud-webhook-indexing-data-sample-info-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

1. Copy the **Webhook URL** and **Secret key** from the wizard.
2. Follow the links under **Instructions** for your specific git host.
3. Create a webhook in your git host using the copied information.
4. Return to the wizard and click **Finish**.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Webhook events from this integration also appear in the indexing triggers log: <b>Git integration sidebar</b> ➜ <b>Indexing triggers</b> ➜ <b>Indexing triggers log</b>.
    </div>
    </div>
</div>

For detailed information, see [Webhook indexing integration guide](/git-integration-for-jira-cloud/webhook-indexing-integration-gij-cloud/).

&nbsp;
* * *

[**Prev:** Using the Git service integration wizard](/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud/)

[**Next:** Using the Single git repository integration](/git-integration-for-jira-cloud/using-the-single-git-integration-wizard-gij-cloud/)

&nbsp;

## Related topics

- [Git integration configuration page](/git-integration-for-jira-cloud/git-integration-configuration-page-gij-cloud/)
- [Managing integration or repository configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud/)
- [Using the Single git integration wizard](/git-integration-for-jira-cloud/using-the-single-git-integration-wizard-gij-cloud/)
- [Using the Git service integration wizard](/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud/)

<p>&nbsp;</p>

