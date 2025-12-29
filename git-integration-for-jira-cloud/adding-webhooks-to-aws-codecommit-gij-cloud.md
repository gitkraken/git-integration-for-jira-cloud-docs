---
title: Adding webhooks to AWS CodeCommit
description: Configure webhooks for AWS CodeCommit repositories in Git Integration for Jira Cloud.
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
            <li>Repository - Push</li>
            <li>Pull request - Created</li>
            <li>Pull request - Updated</li>
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
        <b>Prerequisite:</b> Enable webhooks in the Git Integration for Jira app before proceeding. See <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'><b>Indexing triggers - Getting started</b></a>.
    </div>
    </div>
</div>

**On this page:**
- [Create an SNS topic](#create-an-sns-topic)
- [Add the webhook URL subscription](#add-the-webhook-url-subscription)
- [Configure the repository trigger](#configure-the-repository-trigger)
- [Verify the configuration](#verify-the-configuration)

&nbsp;
* * *
&nbsp;

## Create an SNS Topic

AWS CodeCommit uses SNS (Simple Notification Service) topics to send webhook notifications.

1. Log in to your AWS Console with an admin or poweruser account.

2. Go to **Amazon Simple Notification Service** (use the Services search bar).

    ![](/wp-content/uploads/gij-aws-cc-sns-setup-access.png)

3. In the **Create topic** section, enter a **Topic name**.

    ![](/wp-content/uploads/gij-aws-cc-sns-setup-access-01c.png)

4. Click **Next step**.

    ![](/wp-content/uploads/gij-aws-cc-sns-setup-access-02c.png)

5. Configure the topic:

    - Set **Type** to **Standard**
    - The Name field uses the topic name from step 3

6. Scroll down and click **Create topic**.

    ![](/wp-content/uploads/gij-aws-cc-sns-setup-access-03c.png)

&nbsp;

## Add the Webhook URL Subscription

1. Go to the **Subscriptions** tab for your new SNS topic.

    ![](/wp-content/uploads/gij-aws-cc-sns-setup-access-04c.png)

2. Configure the subscription:

    - **Topic ARN**: Select the SNS topic you created
    - **Protocol**: Select **HTTPS**

3. Get the webhook URL from Jira:

    - Go to **Apps** ➜ **Git Integration: Manage integrations** ➜ **Indexing triggers**
    
        ![](/wp-content/uploads/gij-gitcloud-gitmgr-indexing-triggers-url-link-loc-2025.png)
    
    - Copy the **Webhook URL**

4. Paste the URL into the **Endpoint** field.

5. Click **Create subscription**.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        AWS CodeCommit sends a <code>SubscriptionConfirmation</code> request to the endpoint URL. Git Integration for Jira automatically processes and confirms this request. If confirmation fails, the subscription remains in 'Pending confirmation' status for three days.
    </div>
    </div>
</div>

&nbsp;

## Configure the Repository Trigger

1. Open your CodeCommit repository in the AWS web portal.

    ![](/wp-content/uploads/gij-aws-cc-create-triggers-access-c.png)

2. Go to **Settings** ➜ **Triggers** (sidebar).

3. Click **Create trigger**.

    ![](/wp-content/uploads/gij-aws-cc-create-triggers-filled-up-c.png)

4. Configure the trigger:

    | Setting | Value |
    |---------|-------|
    | Trigger name | Enter a descriptive name |
    | Events | All repository events (recommended) |
    | Branch name | Leave blank for all branches, or specify a branch |
    | Service to use | Amazon SNS |
    | SNS topic | Select the topic you created |

5. Click **Test trigger** to verify the configuration.

6. Click **Create trigger**.

&nbsp;

## Verify the Configuration

1. Make a test commit to your repository.

2. Check the Indexing triggers log in Jira:

    **Apps** ➜ **Git Integration: Manage integrations** ➜ **Indexing triggers** ➜ **Indexing triggers log**

    ![](/wp-content/uploads/gij-gitcloud-indexing-triggers-webhook-log-sample.png)

If errors appear, verify your AWS trigger settings and reindex the integration.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Webhooks are automatically registered for each AWS CodeCommit repository. The connecting service user must have the <a href='/git-integration-for-jira-cloud/aws-codecommit-gij-cloud#required-permissions'><b>basic + all features</b> required permissions</a>.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Webhooks are deleted when you disconnect the AWS CodeCommit integration from Git Integration for Jira Cloud.
    </div>
    </div>
</div>

<kbd>Last updated: December 2025</kbd>
