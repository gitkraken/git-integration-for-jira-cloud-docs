---

title: Adding webhooks to AWS CodeCommit
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Pull request webhooks are now supported. <a href='#setup-webhook-for-aws-repository'>See details</a> on this page.<br>
        <p>Supported webhook events:</p>
        <ul style='margin-bottom:0px;'>
            <li><i>Repository</i> - Push</li>
            <li><i>Pull request</i> - Created</li>
            <li><i>Pull request</i> - Updated</li>
        </ul>
    </div>
    </div>
</div>
<br>

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before you can proceed with the steps outlined in this guide, webhooks must be enabled in the Git Integration for Jira app repository configuration for your Jira instance. For more details, see <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'><b>Indexing triggers - Getting started</b></a>.
    </div>
    </div>
</div>

**What's on this page:**
- [Getting started](#getting-started)
- [Creating an SNS topic](#creating-an-sns-topic)
- [Adding webhook URL via Subscriptions](#adding-webhook-url-via-subscriptions)
- [Setup webhook for AWS repository](#setup-webhook-for-aws-repository)
- [Verification and troubleshooting](#verification-and-troubleshooting)

&nbsp;
* * *
&nbsp;

### Getting started

AWS CodeCommit supports webhooks. For users that came from other Git hosting services, this feature is accessible in the triggers settings. This guide will help users who are unfamiliar with AWS web portal to get things moving.

Start by logging in to your AWS CodeCommit _admin_ or _poweruser_ account that has access to configure SNS topics.

&nbsp;

### Creating an SNS topic

![](/wp-content/uploads/gij-aws-cc-sns-setup-access.png)

1.  From your Console Home, go to Amazon **Simple Notification Service** to start creating a topic. _You may use the Services search bar to access the SNS configuration page._

    ![](/wp-content/uploads/gij-aws-cc-sns-setup-access-01c.png)

    On the **Create topic** section, type a **Topic name** on the provided box.

2.  Click **Next step**. The following page is displayed.

    ![](/wp-content/uploads/gij-aws-cc-sns-setup-access-02c.png)

    *   For the Details section, set _**Type**_ to **Standard**.

    *   _The Name field uses the Topic name entered from the previous page_.

    *   Scroll down to the bottom of the page and click **Create topic**. This creates a new SNS topic with the specified name.

        ![](/wp-content/uploads/gij-aws-cc-sns-setup-access-03c.png)

&nbsp;

### Adding webhook URL via Subscriptions

1.  Continuing from the steps above, go to the **Subscriptions** tab and create a new subscription. You’ll be seeing the following page.

    ![](/wp-content/uploads/gij-aws-cc-sns-setup-access-04c.png)

    *   For the _**Topic ARN**_, select an SNS topic. For this case, set it to the SNS topic created previously from the above steps.

    *   Set Protocol to **HTTPS**.

2.  On your Jira Cloud instance, go to Apps ➜ Git Integration: Manage integrations ➜ **Indexing triggers** and copy the **Webhook URL**.

    ![](/wp-content/uploads/gij-gitcloud-gitmgr-indexing-triggers-url-link-loc-2025.png)

3.  Switch back to your AWS web portal (_where you’re on the Create subscription page_) and paste this URL into the **Endpoint** field.

4.  Click **Create subscription** to complete this setup.

AWS CodeCommit sends a special type of confirmation request, “`SubscriptionConfirmation`", to the specified endpoint URL. The Git Integration for Jira app receives this request, processes it, and then sends back the confirmation automatically. If CodeCommit doesn't receive the handshake to the confirmation request, the subscription will hang in ‘Pending confirmation’ status for three days – see the related article [**here**](https://aws.amazon.com/premiumsupport/knowledge-center/sns-cannot-delete-topic-subscription/).

&nbsp;

### Setup webhook for AWS repository

The webhook setup can be simply performed by any user to the repository as long as an existing SNS topic has been configured.

![](/wp-content/uploads/gij-aws-cc-create-triggers-access-c.png)

1.  On the AWS web portal, open the CodeCommit git repository to work on.

2.  Go to the repository **Settings** on the sidebar.

3.  Start to create a trigger for this repository via the **Triggers** tab.

4.  Click **Create trigger**. The following screen is displayed.

    ![](/wp-content/uploads/gij-aws-cc-create-triggers-filled-up-c.png)

    *   Enter a meaningful **Trigger name**.

    *   Set _**Events**_ to **All repository events** (RECOMMENDED).

    *   Setting the **Branch name** is optional unless a specific branch is used.

    *   For _**Service to use**_, choose **Amazon SNS**.

    *   Use the **SNS topic** subscription created from the previous process.

5.  Test the trigger to see if everything works. Otherwise, verify entered settings.

6.  Click **Create trigger**. This configuration is added to the Triggers list.

&nbsp;

### Verification and troubleshooting

Test and create new commits and see if webhooks have arrived without errors in the Indexing triggers log on your Jira Cloud instance.

![](/wp-content/uploads/gij-gitcloud-indexing-triggers-webhook-log-sample.png)

If errors are received, verify AWS triggers settings and make the necessary changes. Perform a reindex on the integration/repository in the Git repository configuration list to pull supported events and commits from the AWS repository.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Webhooks will be automatically registered for each AWS CodeCommit repository connected to Jira Cloud to instantly index your commits. For this to work, the connecting service user must have the <a href='/git-integration-for-jira-cloud/aws-codecommit-gij-cloud#required-permissions'><b>basic + all features</b> required permissions</a> mentioned in the integration guide.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Webhooks will be deleted when AWS CodeCommit integration is disconnected from Git Integration for Jira Cloud.
    </div>
    </div>
</div>
<br>

