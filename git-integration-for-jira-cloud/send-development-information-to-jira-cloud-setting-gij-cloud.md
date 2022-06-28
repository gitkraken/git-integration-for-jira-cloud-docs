---

title: Send development information to Jira Cloud setting
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

These settings are part of the [**General Settings**](/git-integration-for-jira-cloud/general-settings-gij-cloud) configuration page for Git Integration for Jira Cloud under [**Jira Development Information settings**](/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1207829176/gitcloud-gencfg-jira-dev-info-send-to-cloud.png?version=1&modificationDate=1645097991562&cacheVersion=1&api=v2&width=548&height=253)

Enable/disable this setting to send new commit/branch/pull request data to Jira Cloud where it is processed and made available in a variety of views and features.

**Default settings**
This setting is enabled in [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud) app by default.
This setting is turned off by default in [**Dev Info for Jira Cloud**](https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview) app.


Only newly added commits, branches and pull requests will be uploaded to Jira Cloud when enabling this setting. To upload the entire history of an integration or repository, remove the integration/repository and then add the integration/repository back.

**Permissions**
The **View Development Tools** _permission_ only applies to Jira _**Company-managed**_ projects. _**Team-managed**_ projects don't allow any modifications to the permission.


For more details, see [**Features: Send Development Information (Jira Cloud)**](/git-integration-for-jira-cloud/send-development-information-to-jira-cloud-setting-gij-cloud).

Turning this setting to `ON` automatically disables the [**Enable Git Integration app Smart Commits** setting](/git-integration-for-jira-cloud/enable-git-integration-app-smart-commits-setting-gij-cloud).


After all the settings have been configured according to your requirements, click **Update** to apply the changes.

## More Jira development information settings

*   [Send development information to Jira Cloud setting](/git-integration-for-jira-cloud/send-development-information-to-jira-cloud-setting-gij-cloud) (Git Integration for Jira Cloud)

*   [Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers setting](/git-integration-for-jira-cloud/enable-jira-cloud-smart-commits-automation-for-jira-and-workflow-triggers-setting-gij-cloud) (Git Integration for Jira Cloud)

*   [Enable Git Integration app smart commits setting](/git-integration-for-jira-cloud/enable-git-integration-app-smart-commits-setting-gij-cloud) (Git Integration for Jira Cloud)

*   [Advanced: Clear Development Information setting](/git-integration-for-jira-cloud/advanced-clear-development-information-setting-gij-cloud) (Git Integration for Jira Cloud)

