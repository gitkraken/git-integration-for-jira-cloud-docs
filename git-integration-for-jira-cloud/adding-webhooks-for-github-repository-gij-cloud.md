---
title: Adding webhooks for GitHub repository
description: Configure webhooks for GitHub repositories in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Supported webhook events:</b>
        <ul style='margin-bottom:0px;'>
            <li>Pushes</li>
            <li>Pull requests</li>
        </ul>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Prerequisite:</b> Enable indexing triggers in the Git Integration for Jira app before proceeding. See <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'><b>Indexing Triggers - Getting Started</b></a>.
    </div>
    </div>
</div>

&nbsp;

## Configure GitHub Webhooks

1. Log in to your GitHub account and select a repository.

    ![](/wp-content/uploads/gij-new-github-webhook-setting-page-c1.png)

2. Go to **Settings** ➜ **Webhooks** (sidebar).

3. Click **Add webhook**.

    ![](/wp-content/uploads/gij-web-hooks-github-settings-add-c.png)

4. Configure the webhook:

    - **Payload URL**: Paste the Secret URL from Git Integration for Jira ➜ **Indexing triggers** page
    
        ![](/wp-content/uploads/gij-gitcloud-gitmgr-indexing-triggers-url-link-loc-2025.png)
    
    - **Content type**: Select **application/json**
    - **Secret**: Enter the Secret key from the Indexing triggers page

5. Under **Which events would you like to trigger this webhook?**, select **Just the push event** for commits only.

6. Leave **Active** enabled.

7. Click **Add webhook**.

&nbsp;

## Enable Pull Request Webhooks

To receive both commit and pull request events:

1. Go to your repository's **Settings** ➜ **Webhooks**.

2. Edit your existing webhook or create a new one.

3. Under **Which events would you like to trigger this webhook?**, select **Let me select individual events**.

4. Enable both **Pushes** and **Pull requests**.

    ![](/wp-content/uploads/gij-github-pull-request-event-trigger-webhook.png)

5. Click **Update webhook** or **Add webhook**.

### Event Trigger Options

| Option | Behavior | Recommended |
|--------|----------|-------------|
| Just the push event | Commits only | For basic indexing |
| Send me everything | All events (very verbose) | Not recommended |
| Let me select individual events | Choose Pushes + Pull requests | Recommended for full functionality |

&nbsp;

## Automatic Webhook Registration

Indexing triggers are automatically registered for each GitHub repository connected to Jira Cloud. For automatic registration to work, the connecting GitHub user must be:

- The Organization Owner, OR
- Have repository **ADMIN** rights

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Indexing triggers for GitHub are deleted when you disconnect the GitHub integration from Git Integration for Jira Cloud.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Git Integration for Jira indexes only the repositories indicated by the GitHub organization webhook, not all repositories.
    </div>
    </div>
</div>

<kbd>Last updated: December 2025</kbd>
