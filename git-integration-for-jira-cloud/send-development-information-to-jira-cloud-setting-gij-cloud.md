---

title: Send development information to Jira Cloud setting
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
        These settings are part of the <a href='/git-integration-for-jira-cloud/general-settings-gij-cloud'><b>General Settings</b></a> configuration page for Git Integration for Jira Cloud under <a href='/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud'><b>Jira Development Information settings</b></a>.
    </div>
    </div>
</div>
<br>

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1207829176/gitcloud-gencfg-jira-dev-info-send-to-cloud.png?version=1&modificationDate=1645097991562&cacheVersion=1&api=v2&width=548&height=253)

Enable/disable this setting to send new commit/branch/pull request data to Jira Cloud where it is processed and made available in a variety of views and features.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        This setting is enabled in <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud" target="_blank"><b>Git Integration for Jira Cloud</b></a> app by default.<br>
        This setting is turned off by default in <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview" target="_blank"><b>Dev Info for Jira Cloud</b></a> app.
    </div>
    </div>
</div>
<br>

Only newly added commits, branches and pull requests will be uploaded to Jira Cloud when enabling this setting. To upload the entire history of an integration or repository, remove the integration/repository and then add the integration/repository back.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        The <b>View Development Tools</b> <i>permission</i> only applies to Jira <b><i>Company-managed</i></b> projects. <b><i>Team-managed</i></b> projects don't allow any modifications to the permission.
    </div>
    </div>
</div>
<br>

For more details, see [**Features: Send Development Information (Jira Cloud)**](/git-integration-for-jira-cloud/send-development-information-to-jira-cloud-setting-gij-cloud).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Turning this setting to <code>ON</code> automatically disables the <a href='/git-integration-for-jira-cloud/enable-git-integration-app-smart-commits-setting-gij-cloud'><b>Enable Git Integration app Smart Commits</b> setting</a>.
    </div>
    </div>
</div>
<br>

After all the settings have been configured according to your requirements, click **Update** to apply the changes.

## More Jira development information settings

*   [Send development information to Jira Cloud setting](/git-integration-for-jira-cloud/send-development-information-to-jira-cloud-setting-gij-cloud)

*   [Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers setting](/git-integration-for-jira-cloud/enable-jira-cloud-smart-commits-automation-for-jira-and-workflow-triggers-setting-gij-cloud)

*   [Enable Git Integration app smart commits setting](/git-integration-for-jira-cloud/enable-git-integration-app-smart-commits-setting-gij-cloud)

*   [Advanced: Clear Development Information setting](/git-integration-for-jira-cloud/advanced-clear-development-information-setting-gij-cloud)

