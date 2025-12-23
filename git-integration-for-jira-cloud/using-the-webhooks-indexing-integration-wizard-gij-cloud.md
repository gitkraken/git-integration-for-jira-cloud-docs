---

title: Using the Webhook indexing integration wizard
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Webhook indexing integration allows your connected git servers to work behind a firewall. This is its main aspect. However, the downside is that your integration will have limited features (such as no branch and pull/merge request creation).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Currently, supported Git host services are GitHub, GitLab, Microsoft, and Gerrit.
    </div>
    </div>
</div>

&nbsp;

## Step 1

On the Manage integration page, click **Add integration** then click on a supported Git service from the list.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-integrations-page-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## Step 2

Click on the **Webhook indexing** integration type then click **Add integration** to proceed.

<img src='/wp-content/uploads/gij-gitcloud-add-new-integration-type-webhook-indexing-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

## Step 3

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Don’t click <b>Finish</b> yet!<br>
        Setup webhooks to your git host service using the information provided from this screen.
    </div>
    </div>
</div>

<img src='/wp-content/uploads/gij-gitcloud-webhook-indexing-data-sample-info-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

Refer to the links under the **Instructions** section to provide you guidance while using generated information from the Webhook indexing integration screen (**Webhook URL** and **Secret key**). This is because [indexing triggers](/git-integration-for-jira-cloud/indexing-triggers-formerly-webhooks-gij-cloud/) and webhook indexing integration have different pipelines. However, the webhook events triggered by this integration also appears in the indexing triggers log (Git integration sidebar ➜ Indexing triggers ➜ **Indexing triggers log**).

For detailed information on this integration type, see [Webhook indexing integration guide](/git-integration-for-jira-cloud/webhook-indexing-integration-gij-cloud/).

&nbsp;
* * *

[**Prev:** Using the Git service integration wizard](/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud/)

[**Next:** Using the Single git repository integration](/git-integration-for-jira-cloud/using-the-single-git-integration-wizard-gij-cloud/)

&nbsp;

## Related topics about setting up integration

[Git integration configuration page](/git-integration-for-jira-cloud/git-integration-configuration-page-gij-cloud/) (Git Integration for Jira Cloud)

[Managing integration or repository configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Using the Single git integration wizard](/git-integration-for-jira-cloud/using-the-single-git-integration-wizard-gij-cloud/) (Git Integration for Jira Cloud)

[Using the Git service integration wizard](/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud/) (Git Integration for Jira Cloud)

