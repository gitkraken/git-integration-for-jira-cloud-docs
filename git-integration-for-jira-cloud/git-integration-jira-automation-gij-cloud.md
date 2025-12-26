---

title: Git Integration + Jira Automation
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>JIRA CLOUD</b> &mdash; <b>AVAILABLE!</b><br>
<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>JIRA SERVER / DATA CENTER</b> &mdash; <b>AVAILABLE!</b>

Jira automation allows teams and groups to control processes and workflows using a rule to automate actions within Jira based on criteria.

Automation rules have 3 parts:

*   **Triggers** - Listens for events and starts the execution of a rule when a set condition is met.

*   **Conditions** - Set the scope of a rule with specific events tailored for your team.

*   **Actions** - Set automated tasks to perform when a condition is met.


<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>On this page:</b><br>
        <ul style='margin-bottom:0px;'>
            <li><a href='#permissions'>Permissions</a></li>
            <li><a href='#git-integration-for-jira-app-supported-triggers'>Git Integration for Jira app supported triggers</a></li>
            <li><a href='#how-to-set-up-automation-templates'>How to set up automation templates</a></li>
            <li><a href='#known-issue'>Known issue</a></li>
            <li><a href='#advanced-examples'>Advanced examples</a></li>
            <li><a href='#automation-template-library'>Automation template library</a></li>
        </ul>
    </div>
    </div>
</div>

&nbsp;

## Permissions

Any user with Browser Project permissions can create a rule.

&nbsp;

## Git Integration for Jira app supported triggers

We currently support the following triggers:

*   Branch created

*   Commit created

*   Pull request created

*   Pull request merged

*   Pull request declined


And thus, we will support all of these triggers in the coming releases.

## How to set up automation templates

Create a rule to configure triggers and actions for automating tasks. There are two levels:

### Project level (projects)

1.  Open a project to work on, Open the Side Bar, click the ( ... ) Icon then go to ![](/wp-content/uploads/actions-icon.png) **Space settings**.

    ![](/wp-content/uploads/gij-gitcloud-automation-proj-level-2025.pngg)

2.  On the sidebar, click **Automation**.

3.  Click the ![](/wp-content/uploads/gij-jira-cloud-automation-New-Rule-2025.png) **Create Rule** button, then 'Create from Scratch'.

4.  This will take you to the Automation creation wizard.

    ![](/wp-content/uploads/gij-jira-cloud-automation-start-2025.png)

5. Clicking the 'DevOps' category will display the GIJ provided triggers. These are the triggers that you will base your automations on.
    ![](/wp-content/uploads/gij-jira-cloud-automation-triggers-2025.png)

6.  Configure triggers, conditions and actions for this rule:

    ![](/wp-content/uploads/gij-jira-cloud-automation-example-rule-2025.png)

    a.  **TRIGGER** – This rule will trigger when a pull request is created.

    b.  **CONDITION** – When the status of the Jira issue is To Do, it will perform the actions below.

    c.  **ACTIONS** – If the condition(s) are met, the rule will fire up the actions, assign the issue to a specific user and transitions the Jira issue to In Progress.

7.  Enter a descriptive name for this rule in the provided box.

8.  Click **Turn it on** to publish and activate it. The new rule is added to the automation list.


<img src='/wp-content/uploads/gij-jira-cloud-automation-list-2025.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

### Global administration level (system)

1.  On your Jira dashboard, go to menu **Jira Settings** ➜ **System**.

    ![](/wp-content/uploads/gij-jira-cloud-administration-settings-menu-2025.png)

2.  On the left sidebar, scroll to the bottom (Automation) and click **Automation rules**.

3.  Click **Create rule** , the 'Create from Scratch' to create a new automation rule.

    ![](/wp-content/uploads/gij-gitcloud-automation-global-level-2025.png)

    ![](/wp-content/uploads/gij-jira-cloud-automation-start-2025.png)

5. Clicking the 'DevOps' category will display the GIJ provided triggers. These are the triggers that you will base your automations on.
    ![](/wp-content/uploads/gij-jira-cloud-automation-triggers-2025.png)

6.  Configure triggers, conditions and actions for this rule:

    ![](/wp-content/uploads/gij-jira-cloud-automation-example-rule-2025.png)

    a.  **TRIGGER** – This rule will trigger when a pull request is created.

    b.  **CONDITION** – When the status of the Jira issue is To Do, it will perform the actions below.

    c.  **ACTIONS** – If the condition(s) are met, the rule will fire up the actions, assign the issue to a specific user and transitions the Jira issue to In Progress.

7.  Enter a descriptive name for this rule in the provided box.

8.  Click **Turn it on** to publish and activate it. The new rule is added to the automation list.


<img src='/wp-content/uploads/gij-jira-cloud-automation-list-global-2025.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

* * *

&nbsp;

## Advanced examples

| Examples | Examples |
| :---: | :---: |
| <img src='/wp-content/uploads/gij-automation-branch-01.png' width=321 height=413 style='vertical-align:top;' /> | <img src='/wp-content/uploads/gij-automation-commit-01.png' width=313 height=411 style='vertical-align:top;' /> |
| <img src='/wp-content/uploads/gij-automation-pullreq-01.png' width=324 height=447 style='vertical-align:top;' /> | <img src='/wp-content/uploads/gij-automation-pullreq-02.png' width=340 height=462 style='vertical-align:top;' /> |
| <img src='/wp-content/uploads/gij-automation-branch-conditional-01.png' width=330 height=636 style='vertical-align:top;' /> | <img src='/wp-content/uploads/gij-automation-issue-condition-01.png' width=322 height=563 style='vertical-align:top;' /> |

&nbsp;

* * *

&nbsp;

## Automation template library

Let automation do the work while your developers focus on what's important. Automation Templates for Git Integration for Jira can be implemented so you never need to start from scratch. We've provided some templates we think are useful so you don't need to create your own automation rules from scratch.

\*All of the templates from [Atlassian's template library](https://www.atlassian.com/software/jira/automation-template-library/bitbucket-github-gitlab) will work with Git Integration for Jira

<img src='/wp-content/uploads/gij-automation-library-template.png' style='margin:25px auto;max-width:100%;display:block;height:auto;width:470px;' />

**With Git Integration for Jira you can integrate any Git repository with Jira. And better yet, you can make use of any of our handy automation templates, or use Atlassian's!**

You can write your own templates using [Atlassian's no-code Jira automation engine](https://www.atlassian.com/software/jira/features/automation).

&nbsp;

### Available templates from Atlassian for Git Integration for Jira users

Here are some templates from Atlassian you can use as a guide for some of the most common uses:

*   [When a commit is created, then transition the Jira issue](https://www.atlassian.com/software/jira/automation-template-library/rules#/rule/1357202).

*   [When a PR is created, add a comment to the Jira issue](https://www.atlassian.com/software/jira/automation-template-library/rules#/rule/1357211).

*   [When a commit is created then send Slack message based on assignee](https://www.atlassian.com/software/jira/automation-template-library/rules#/rule/1357149).

&nbsp;

### Handy use cases for automation for Git Integration for Jira users

*   Transition issue state when a commit arrives.

*   Transition issue state when pull/merge request is merged. For example: from IN PROGRESS to DONE.

&nbsp;

### For more powerful conditions

*   Use [Jira Automation Smart Values](https://support.atlassian.com/jira-software-cloud/docs/what-are-smart-values/) to extract data from your commits and branches to be used in an automation action such as;

    *   Take actions based on the name of a branch. For example:

        *   only transition branches that contain a specific keyword like "WIP" (Work In Progress).

        *   add a comment to an issue when a branch contains a certain keyword.

    *   Extract the pullRequest state (Open vs Merged vs Declined) from a Pull request, and use it in an [advanced compare condition](https://support.atlassian.com/jira-software-cloud/docs/automation-conditions/)

    *   Ensure the commit message contains things you're looking for, like issue keys, etc.

    *   Verify that only certain repos trigger the automation

    *   See the full list of [available smart values](https://support.atlassian.com/jira-software-cloud/docs/smart-values-development/)

&nbsp;

### Supported triggers

We currently support the 5 highlighted triggers depicted below, and we will support all of these triggers in coming releases.

<img src='/wp-content/uploads/gij-jira-cloud-automation-triggers-2025.png' style='margin:25px auto;width:566px;height:auto;display:block;max-width:100%;' />

&nbsp;

### More Jira automation information

[Automation basics](https://www.atlassian.com/software/jira/guides/expand-jira/automation)

[What are smart values?](https://support.atlassian.com/jira-software-cloud/docs/what-are-smart-values/)

[Automation conditions](https://support.atlassian.com/jira-software-cloud/docs/automation-conditions/)

