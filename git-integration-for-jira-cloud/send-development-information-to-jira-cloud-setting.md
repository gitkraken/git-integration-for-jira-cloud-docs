---

title: Send development information to Jira Cloud setting
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

These settings are part of the [**General Settings**](/git-integration-for-jira-cloud/General-Settings) configuration page for Git Integration for Jira Cloud under [**Jira Development Information settings**](/wiki/spaces/GITCLOUD/pages/1207796181/Jira+development+information+settings).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1207829176/gitcloud-gencfg-jira-dev-info-send-to-cloud.png?version=1&modificationDate=1645097991562&cacheVersion=1&api=v2&width=548&height=253)

Enable/disable this setting to send new commit/branch/pull request data to Jira Cloud where it is processed and made available in a variety of views and features.

**Default settings**
This setting is enabled in [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud) app by default.
This setting is turned off by default in [**Dev Info for Jira Cloud**](https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview) app.


Only newly added commits, branches and pull requests will be uploaded to Jira Cloud when enabling this setting. To upload the entire history of an integration or repository, remove the integration/repository and then add the integration/repository back.

**Permissions**
The **View Development Tools** _permission_ only applies to Jira _**Company-managed**_ projects. _**Team-managed**_ projects don't allow any modifications to the permission.


For more details, see [**Features: Send Development Information (Jira Cloud)**](http://link.bigbrassband.com/jira-gitcloud-send-development-information-to-jira-cloud).

Turning this setting to `ON` automatically disables the [**Enable Git Integration app Smart Commits** setting](/wiki/spaces/GITCLOUD/pages/1207829205/Enable+Git+Integration+app+smart+commits+setting).


After all the settings have been configured according to your requirements, click **Update** to apply the changes.

## More Jira development information settings

*   Page:

    [Send development information to Jira Cloud setting](/wiki/spaces/GITCLOUD/pages/1207829176/Send+development+information+to+Jira+Cloud+setting) (Git Integration for Jira Cloud)

*   Page:

    [Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers setting](/wiki/spaces/GITCLOUD/pages/1207796196/Enable+Jira+Cloud+Smart+Commits%2C+Automation+for+Jira+and+Workflow+Triggers+setting) (Git Integration for Jira Cloud)

*   Page:

    [Enable Git Integration app smart commits setting](/wiki/spaces/GITCLOUD/pages/1207829205/Enable+Git+Integration+app+smart+commits+setting) (Git Integration for Jira Cloud)

*   Page:

    [Advanced: Clear Development Information setting](/wiki/spaces/GITCLOUD/pages/1207829225/Advanced%3A+Clear+Development+Information+setting) (Git Integration for Jira Cloud)

