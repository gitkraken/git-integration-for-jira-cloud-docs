---

title: Git Integration + Jira Automation
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
JIRA CLOUD - AVAILABLE
JIRA SERVER / DC - COMING SOON


Jira automation allows teams and groups to control processes and workflows using a rule to automate actions within Jira based on criteria.

Automation rules have 3 parts:

*   **Triggers** - Listens for events and starts the execution of a rule when a set condition is met.

*   **Conditions** - Set the scope of a rule with specific events tailored for your team.

*   **Actions** - Set automated tasks to perform when a condition is met.


## Permissions

Any user with Browser Project permissions can create a rule.

## Git Integration for Jira app supported triggers

We currently support the following triggers:

*   Branch created

*   Commit created

*   Pull request created

*   Pull request merged

*   Pull request declined


And thus, we will support all of these triggers in the coming releases.

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/i21p45xb5y) _to open this video in a new tab/window for more viewing options._

## How to set up automation templates

Create a rule to configure triggers and actions for automating tasks. There are two levels:

### Project level (projects)

1.  Open a project to work on, then go to ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Project settings**.

2.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1698922497/gitcloud-automation-proj-level-02(c).png?version=2&modificationDate=1632383594084&cacheVersion=1&api=v2)

    On the sidebar, click **Automation**.

3.  Click the ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Rules** tab.

4.  Click **Create rule** to create a new automation rule.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1698922497/jira-cloud-automation-start(c).png?version=1&modificationDate=1622629776860&cacheVersion=1&api=v2)
5.  Configure triggers, conditions and actions for this rule:

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1698922497/jira-cloud-automation-example-rule(c).png?version=1&modificationDate=1622629344027&cacheVersion=1&api=v2)
    1.  **TRIGGER** – This rule will trigger when a pull request is created.

    2.  **CONDITION** – When the status of the Jira issue is IN PROGRESS, it will perform the actions below.

    3.  **ACTIONS** – If the condition(s) are met, the rule will fire up the actions, assign the issue to a specific user and transitions the Jira issue to IN REVIEW.

6.  Enter a descriptive name for this rule in the provided box.

7.  Click **Turn it on** to publish and activate it. The new rule is added to the automation list.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1698922497/jira-cloud-automation-list.png?version=1&modificationDate=1622632132559&cacheVersion=1&api=v2&width=680&height=274)

### Global administration level (system)

1.  On your Jira dashboard, go to menu **Jira Settings** ➜ **System**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1698922497/jira-cloud-administration-settings-menu(c).png?version=2&modificationDate=1622643907973&cacheVersion=1&api=v2)
2.  On the left sidebar, scroll to the bottom (Automation) and click **Automation rules**.

3.  ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1698922497/gitcloud-automation-proj-level-02(c).png?version=2&modificationDate=1632383594084&cacheVersion=1&api=v2)

    Click the ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Rules** tab.

4.  Click **Create rule** to create a new automation rule.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1698922497/jira-cloud-automation-start(c).png?version=1&modificationDate=1622629776860&cacheVersion=1&api=v2)
5.  Configure triggers, conditions and actions for this rule:

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1698922497/jira-cloud-automation-example-rule(c).png?version=1&modificationDate=1622629344027&cacheVersion=1&api=v2)
    1.  **TRIGGER** – This rule will trigger when a pull request is created.

    2.  **CONDITION** – When the status of the Jira issue is IN PROGRESS, it will perform the actions below.

    3.  **ACTIONS** – If the condition(s) are met, the rule will fire up the actions, assign the issue to a specific user and transitions the Jira issue to IN REVIEW.

6.  Enter a descriptive name for this rule in the provided box.

7.  Click **Turn it on** to publish and activate it. The new rule is added to the automation list.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1698922497/jira-cloud-automation-list.png?version=1&modificationDate=1622632132559&cacheVersion=1&api=v2&width=680&height=274)

## Known issue

![(info)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/information.png) The limitation of Git Integration for Jira (GIJ) app not working with Automation for Jira (A4J) Lite is not a GIJ limitation but an Atlassian limitation.

## Advanced Examples

For advanced examples, see sub-page [Automation Advanced Examples](/git-integration-for-jira-cloud/git-integration-jira-automation-advanced-examples/).

