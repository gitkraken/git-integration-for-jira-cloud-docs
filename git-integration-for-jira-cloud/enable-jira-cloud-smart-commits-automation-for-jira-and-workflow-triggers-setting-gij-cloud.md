---

title: Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers setting
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<!-- SETTINGS -->

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        These settings are part of the <a href="/git-integration-for-jira-cloud/general-settings-gij-cloud">General settings</a> configuration page for Git Integration for Jira Cloud under <a href="/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud">Jira Development Information settings</a>.
    </div>
    </div>
</div>

&nbsp;

<img src='/wp-content/uploads/gij-gitcloud-gencfg-enable-smart-commits-automation.png' style='display:block;margin:25px auto;max-width:100%' />

This setting engages the native Atlassian Jira Cloud Smart Commit processor. At this time only `#time`, `#comment` and `#transitions` are supported for the triggers. This also enables the [Automatic Workflow Triggers](/git-integration-for-jira-cloud/automatic-workflow-triggers-gij-cloud) feature.

The automatic workflow triggers allows you to use your development activity to make automatic changes in your Jira project workflows. For example, you can use the workflow trigger to transition your Jira issues.

For more information on Automation for Jira, see article [Git Integration + Jira Automation](/git-integration-for-jira-cloud/git-integration-jira-automation-gij-cloud).

After all the settings have been configured according to your requirements, click **Update** to apply the changes.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        With both smart commits processors active, the #time and #comment commands will be processed twice and you'll get duplicated results.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Compared to the other smart commit processor option, this one has support for Jira Automation but lacks the <code>#label</code> command.
    </div>
    </div>
</div>

&nbsp;

## More Jira development information settings

[Send development information to Jira Cloud setting](/git-integration-for-jira-cloud/send-development-information-to-jira-cloud-setting-gij-cloud)

**Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers setting** (this page)

[Enable Git Integration app smart commits setting](/git-integration-for-jira-cloud/enable-git-integration-app-smart-commits-setting-gij-cloud)

[Advanced: Clear Development Information setting](/git-integration-for-jira-cloud/advanced-clear-development-information-setting-gij-cloud)

<br>
<br>
<hr>
<br>
<br>

## More related topics on Jira Development Information

[Development Information Views](/git-integration-for-jira-cloud/development-information-views-gij-cloud)

[JQL searching for commits and pull requests](/git-integration-for-jira-cloud/jql-searching-for-commits-and-pull-requests-gij-cloud)

[Jira Cloud Smart Commits and Workflow Triggers](/git-integration-for-jira-cloud/jira-cloud-smart-commits-and-workflow-triggers-gij-cloud/)

[Jira Development Information general settings](/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud)


