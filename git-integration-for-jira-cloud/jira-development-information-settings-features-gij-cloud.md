---

title: Jira Development Information settings feature
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Access this setting on the dashboard menu via Apps ➜ Git Integration: Manage Git repositories ➜ (sidebar) **General settings**. Alternatively, go to dashboard Jira Settings ➜ Apps ➜ (sidebar) **General settings**.

![](/wp-content/uploads/gij-gitcloud-jira-dev-info-general-settings.png)

There are four Jira Development Information settings that Jira administrators should aware of:

&nbsp;

### Send Development Information to Jira Cloud

Enabling _**Send Development Information to Jira Cloud**_ setting will send new commit/branch/pull request data to Jira Cloud where it is processed and made available in a variety of views and features (described [here](/git-integration-for-jira-cloud/development-information-views-gij-cloud) and [here](/git-integration-for-jira-cloud/jira-development-information-gij-cloud).

Only newly received data is sent to Jira Cloud - so if you wish to see historical data in these views - remove the current repositories/integrations in Manage Git repositories and re-connect.

&nbsp;

### Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers

The _**Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers**_ setting engages the native Jira Cloud Smart Commit processing (only `#time`, `#comment`, and `#transitions`) as well as enables **Automatic workflow triggers**.

For more information - see our [Smart Commits^](/git-integration-for-jira-cloud/smart-commits-gij-cloud) or [Automatic workflow triggers](/git-integration-for-jira-cloud/automatic-workflow-triggers-gij-cloud) documentation.

&nbsp;

### Enable Git Integration app Smart Commits

The _**Enable Git Integration app Smart Commits**_ setting engages BigBrassBand's Git Integration Smart Commit processing (`#time`, `#comment`, `#transitions`, and `#label`).

For more information - see our [Smart Commit documentation](/git-integration-for-jira-cloud/smart-commits-gij-cloud).

&nbsp;

### Advanced: Clear Development Information

Behind the "Advanced" link is a function button that gives the Jira administrator the ability to clear out all Development Information associated with the Git Integration for Jira app.

Note that this action takes some time to process and Development Information may be visible in places until the process finishes. Expect the process to take up to 1 hour.

