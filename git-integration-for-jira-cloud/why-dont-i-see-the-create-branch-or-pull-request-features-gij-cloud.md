---

title: Why don't I see the Create branch or pull request features?
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

### Problem

Users cannot see the **Create branch** or **Create pull/merge request** actions on the [Jira issue developer panel](/git-integration-for-jira-cloud/jira-git-integration-development-panel-gij-cloud).

<img src='/wp-content/uploads/gij-gitcloud-troubleshoot-createbranch-pullrequest.png' style='max-width:100%;margin:25px auto;display:block;' />

&nbsp;

### Solution

The **Create branch** and **Create pull/merge requests** features are enabled by connecting to one of the Full feature integrations.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png' style='max-width:100%;margin:25px auto;display:block;' />

1.  Navigate to the Manage integrations page.

2.  Click **Add integration** and select OAuth or PAT integration options (GitHub, GitLab, etc.).

3.  Complete the integration steps of the connection wizard.

See our [Integration Guides](/git-integration-for-jira-cloud/integration-guide-gij-cloud) for each Full feature integration option.

The regular Git integration and Limited connect feature Git option does not offer the Create branch and Create pull/merge request features.

<img src='/wp-content/uploads/gij-add-new-integration-plain-git-sel.png' style='max-width:100%;margin:25px auto;display:block;' />

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>
<br>

