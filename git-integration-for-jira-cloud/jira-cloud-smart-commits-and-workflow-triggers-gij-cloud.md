---

title: Jira Cloud Smart Commits and Workflow Triggers
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Smart commits allows your team to perform actions on Jira issues from a single commit. Users can enter the issue key and the desired action such as time tracking or closing an issue.

The smart commit processing is **active by default** and can be enabled/disabled via **General settings** _(Jira dashboard menu Apps ➜ Git Integration: Manage integrations ➜ (sidebar) General settings)._

**What's on this page:**
- [General settings effect on Smart Commits commands](#general-settings-effect-on-smart-commits-commands)
- [How can a Jira administrator enable or disable the Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers?](#how-can-a-jira-administrator-enable-or-disable-the-jira-cloud-smart-commits-automation-for-jira-and-workflow-triggers)
- [More related topics about Jira Cloud smart commits and workflow triggers](#more-related-topics-about-jira-cloud-smart-commits-and-workflow-triggers)
- [More related topics on Jira Development Information](#more-related-topics-on-jira-development-information)


&nbsp;
<hr>
&nbsp;

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <a href='https://confluence.atlassian.com/jirasoftwarecloud/configuring-development-tools-764478056.html#Configuringdevelopmenttools-Workflowtriggers' target='_blank'>More information from Atlassian</a>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Administrator note</b><br>
        Both <b>Send Development Information to Jira Cloud</b> and <b>Enable Dev Info Smart Commits & Workflow</b> settings must be enabled for automatic workflow triggers to be enabled.
        <img src='/wp-content/uploads/gij-gitcloud-jira-dev-info-smart-commits-req-sel.png' style='display:block;margin:25px auto 0 auto;max-width:100%' />
    </div>
    </div>
</div>

&nbsp;

## General settings effect on Smart Commits commands

Please take note that the following settings will affect availability of specific smart commit commands as outlined below:

<img src='/wp-content/uploads/gij-gitcloud-jira-dev-info-smart-commits-req-sel.png' style='display:block;margin:25px auto;max-width:100%' />

| When this General setting is enabled | \#time | \#label |
|:---|:---|:---|
| Jira Cloud Smart Commits | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-not-red.png) |
| Git Integration app Smart Commits | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
|Both Jira Cloud Smart and GIJ app Smart commits | ![](/wp-content/uploads/gij-matrix-open-check-green.png)<br>(doubled \#time and \#comment) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |

&nbsp;

## How can a Jira administrator enable or disable the Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers?

1.  Install the [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) or the [**Dev Info for Jira**](https://marketplace.atlassian.com/1219270) app.

2.  Navigate to the **General settings** page of the application _Jira Settings_ ➜ _Apps_ ➜ (sidebar) _General settings_).

3.  Click the **Send Development Information to Jira Cloud** checkbox to mark and enable it. This also allows access to the **Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers** setting.

4.  Click the **Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers** checkbox to mark and enable this setting.

5.  Click **Update** to save the settings.

![](/wp-content/uploads/gij-gitcloud-gencfg-jira-devinfo-options-02.png)

&nbsp;

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'><b>Support Desk</b></a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

## More related topics about Jira Cloud smart commits and workflow triggers

[Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers](/git-integration-for-jira-cloud/enable-jira-cloud-smart-commits-automation-for-jira-and-workflow-triggers-gij-cloud)

[Automatic Workflow Triggers](/git-integration-for-jira-cloud/automatic-workflow-triggers-gij-cloud)

<br>
<br>
<hr>
<br>
<br>

## More related topics on Jira Development Information

*   [Development Information Views](/git-integration-for-jira-cloud/development-information-views-gij-cloud)

*   [JQL searching for commits and pull requests](/git-integration-for-jira-cloud/jql-searching-for-commits-and-pull-requests-gij-cloud)

*   **Jira Cloud Smart Commits and Workflow Triggers** (this page)

*   [Jira Development Information general settings](/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud)


