---

title: Automatic Workflow Triggers
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Use your development activity to make automatic changes in your Jira project workflows. For example:

*   you can configure your Jira workflow to automatically send a Jira issue to IN REVIEW status when a pull request is pushed and associated with the issue, or

*   you can send a Jira issue to IN PROGRESS when a commit is pushed and associated with a Jira issue.


Available triggers through the [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) and [**Dev Info for Jira**](https://marketplace.atlassian.com/1219270) apps:

*   Commit created

*   Branch created

*   Pull request created

*   Pull request merged

*   Pull request declined (closed)

*   Pull request reopened



To configure automatic workflow triggers for your project:

1.  Go to ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Project settings**.

2.  Select **Workflow** on the sidebar.

3.  Click ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Edit** on the _**Actions**_ column.

4.  Click **Text** to display the Diagram in text mode.

5.  Under _**Transitions**_ column, click a transition item.

6.  Click **Add trigger**. The Add trigger dialog is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1940783182/gitcloud-automatic-workflow-trigger-add-trigger(c).png?version=1&modificationDate=1631336969766&cacheVersion=1&api=v2)
7.  Click **Commit created**.

8.  Click **Add trigger**. This trigger will automatically transition the issue when a related commit is made in a connected repository.

9.  Click **Publish Draft**. This action will publish the currently edited workflow. Create a backup or set it to _**No**_ then click **Publish**.


The automatic workflow trigger is now configured. You can also view this entire process by watching the demo video below.

## Demo video: Configuring Automatic Workflow Trigger

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/r8fm0tbrcs) _and open this demo video in a new tab for more viewing options._

[**More information from Atlassian**](https://confluence.atlassian.com/jirasoftwarecloud/configuring-development-tools-764478056.html#Configuringdevelopmenttools-Workflowtriggers)

### More related topics about Jira Cloud smart commits and workflow triggers

*   Page:

    [Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers](/wiki/spaces/GITCLOUD/pages/1940455528/Enable+Jira+Cloud+Smart+Commits%2C+Automation+for+Jira+and+Workflow+Triggers) (Git Integration for Jira Cloud)

*   Page:

    [How can a Jira administrator enable or disable the Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers?](/wiki/spaces/GITCLOUD/pages/1940914229) (Git Integration for Jira Cloud)

*   Page:

    [Automatic Workflow Triggers](/wiki/spaces/GITCLOUD/pages/1940783182/Automatic+Workflow+Triggers) (Git Integration for Jira Cloud)