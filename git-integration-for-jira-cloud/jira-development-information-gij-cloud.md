---

title: Jira Development Information
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<!-- FEATURES -->

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <b>View Development Tools</b> <i>permission</i> only applies to Jira <b><i>Company-managed</i></b> projects. <b><i>Team-managed</i></b> projects don't allow to modify the permission.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Only newly added commits, branches and pull requests will be uploaded to Jira Cloud when enabling the <a href='/git-integration-for-jira-cloud/send-development-information-to-jira-cloud-setting-gij-cloud'>Send Development Information to Jira Cloud</a> setting. If you wish to upload the entire history of an integration or repository - remove the integration/repository and then add the integration/repository back.
    </div>
    </div>
</div>

&nbsp;

**What's on this page:**
- [What is Jira Development Information?](#what-is-jira-development-information)
- [How does Jira Development Information work?](#how-does-jira-development-information-work)
- [Who can see Jira Development Information?](#who-can-see-jira-development-information)
- [How can a Jira administrator enable or disable Jira Development Information?](#how-can-a-jira-administrator-enable-or-disable-jira-development-information)
- [What other features are enabled by Jira Development Information?](#what-other-features-are-enabled-by-jira-development-information)

<br>
<br>
<hr>
<br>
<br>

## What is Jira Development Information?

Jira Development Information is a suite of new features available in Jira Software on the Cloud platform that puts commits, branches, and pull requests in context of Jira issue.

*   By default, [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) has Jira Development Information disabled. ([How to enable?](/git-integration-for-jira-cloud/how-can-a-jira-administrator-enable-or-disable-jira-development-information-gij-cloud))

*   By default, [**Dev Info for Jira**](https://marketplace.atlassian.com/1219270) has Jira Development Information enabled. ([How to disable?](/git-integration-for-jira-cloud/how-can-a-jira-administrator-enable-or-disable-jira-development-information-gij-cloud))

## How does Jira Development Information work?

The [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) and [**Dev Info for Jira**](https://marketplace.atlassian.com/1219270) apps can be configured to "push" development information (commits, branches, and pull requests) directly into your Jira Cloud instance. Once the data is stored by Jira Cloud - the commits, branches, and pull requests can be displayed by Atlassian in a variety of locations within Jira Cloud. This data additionally enables a new of [new features](#What-other-features-are-enabled-by-Jira-Development-Information%3).

## Who can see Jira Development Information?

*   Jira users with the View development tools Jira permission for a given Jira project can.

*   Jira administrators can verify a user's permissions using the [**Permission Helper**](https://confluence.atlassian.com/adminjiracloud/jira-admin-helper-818578850.html).

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <b>View developer tools</b> <i>permission</i> is required to view the Jira Development Information. Jira users must also have the <b>Browse Project</b> <i>permissions</i> to a project associated with a repository to view.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Note that the <b>Project Permissions</b> feature in the <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud" target="_blank"><b>Git Integration for Jira</b></a> and <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview" target="_blank"><b>Dev Info for Jira</b></a> app does not apply to Jira Development Information. All users with <b>View Development Tools</b> permission can access Jira Development Information.
    </div>
    </div>
</div>
<br>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://bigbrassband.atlassian.net/servicedesk/customer/portals'><b>Support Desk</b></a> or email us at <a href='mailto:gijsupport@bigbrassband.com'>gijsupport@bigbrassband.com</a>.
    </div>
    </div>
</div>

&nbsp;

## How can a Jira administrator enable or disable Jira Development Information?

Install the [Git Integration for Jira](https://marketplace.atlassian.com/4984) or the [Dev Info for Jira](https://marketplace.atlassian.com/1219270) app.

1.  Navigate to the General settings page of the application (Jira Settings ➜ Apps ➜ (sidebar) **General settings**).

2.  Enable or disable the setting: `Send Development Information to Jira Cloud`.

3.  Click **Update** button.

<img src='/wp-content/uploads/gij-gitcloud-gencfg-send-devinfo-to-jira-cloud.png' style='display:block;margin:25px auto 35px auto;max-width:100%' />

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        See <a href='/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud'>Jira Development Information general settings</a> to learn more about smart commits and other settings.
    </div>
    </div>
</div>
<br>
<br>

## What other features are enabled by Jira Development Information?

Follow the links below to learn related topics about Jira Development Information

*   [Development Information Views](/git-integration-for-jira-cloud/development-information-views-gij-cloud)

    *   [Development status in Jira Issue Searching](/git-integration-for-jira-cloud/development-status-in-jira-issue-searching-gij-cloud)

    *   [Release Hub](/git-integration-for-jira-cloud/release-hub-warnings-gij-cloud)

    *   [NextGen projects only: View commits, branches, and pull requests in Jira Boards](/git-integration-for-jira-cloud/next-gen-projects-only-view-commits-branches-and-pull-requests-in-jira-boards-gij-cloud)

*   [JQL searching for commits and pull requests](/git-integration-for-jira-cloud/jql-searching-for-commits-and-pull-requests-gij-cloud)

*   [Jira Cloud Smart Commits and Workflow Triggers](/git-integration-for-jira-cloud/jira-cloud-smart-commits-and-workflow-triggers-gij-cloud/)

    *   [How can a Jira administrator enable or disable the Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers?](/git-integration-for-jira-cloud/how-can-a-jira-administrator-enable-or-disable-the-jira-cloud-smart-commits-automation-for-jira-and-workflow-triggers-gij-cloud/)

    *   [Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers](/git-integration-for-jira-cloud/enable-jira-cloud-smart-commits-automation-for-jira-and-workflow-triggers-gij-cloud/)

    *   [Automatic Workflow Triggers](/git-integration-for-jira-cloud/automatic-workflow-triggers-gij-cloud)

*   [Jira Development Information general settings](/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud)


