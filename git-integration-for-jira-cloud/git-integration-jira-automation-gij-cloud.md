---

title: Git Integration + Jira Automation
description: Learn how to configure Jira automation rules with Git Integration for Jira Cloud triggers for branches, commits, and pull requests.
taxonomy:
    category: git-integration-for-jira-cloud

---

<b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>JIRA CLOUD</b> &mdash; <b>AVAILABLE!</b><br>
<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>JIRA SERVER / DATA CENTER</b> &mdash; <b>AVAILABLE!</b>

Jira automation allows teams and groups to control processes and workflows using rules to automate actions within Jira based on specific criteria.

Automation rules have three parts:

- **Triggers** – Listen for events and start executing a rule when a set condition is met.
- **Conditions** – Set the scope of a rule with specific events tailored for your team.
- **Actions** – Set automated tasks to perform when a condition is met.


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

Any user with Browse Project permissions can create a rule.

&nbsp;

## Git Integration for Jira app supported triggers

Git Integration for Jira currently supports the following triggers:

- Branch created
- Commit created
- Pull request created
- Pull request merged
- Pull request declined

Additional triggers will be supported in future releases.

## How to set up automation templates

Create a rule to configure triggers and actions for automating tasks. You can create rules at two levels:

### Project level (projects)

1. Open a project, open the sidebar, click the (...) icon, then go to ![](/wp-content/uploads/actions-icon.png) **Space settings**.

    ![](/wp-content/uploads/gij-gitcloud-automation-proj-level-2025.png)

2. On the sidebar, click **Automation**.

3. Click the ![](/wp-content/uploads/gij-jira-cloud-automation-New-Rule-2025.png) **Create Rule** button, then select **Create from Scratch**.

4. The Automation creation wizard opens.

    ![](/wp-content/uploads/gij-jira-cloud-automation-start-2025.png)

5. Click the **DevOps** category to display the Git Integration for Jira triggers. Use these triggers as the basis for your automations.

    ![](/wp-content/uploads/gij-jira-cloud-automation-triggers-2025.png)

6. Configure triggers, conditions, and actions for this rule:

    ![](/wp-content/uploads/gij-jira-cloud-automation-example-rule-2025.png)

    a. **TRIGGER** – This rule triggers when a pull request is created.

    b. **CONDITION** – When the status of the Jira issue is To Do, the rule performs the actions below.

    c. **ACTIONS** – If the conditions are met, the rule assigns the issue to a specific user and transitions the Jira issue to In Progress.

7. Enter a descriptive name for this rule in the provided box.

8. Click **Turn it on** to publish and activate the rule. The new rule appears in the automation list.


<img src='/wp-content/uploads/gij-jira-cloud-automation-list-2025.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

### Global administration level (system)

1. On your Jira dashboard, go to menu **Jira Settings** ➜ **System**.

    ![](/wp-content/uploads/gij-jira-cloud-administration-settings-menu-2025.png)

2. On the left sidebar, scroll to the bottom (Automation) and click **Automation rules**.

3. Click **Create rule**, then **Create from Scratch** to create a new automation rule.

    ![](/wp-content/uploads/gij-gitcloud-automation-global-level-2025.png)

    ![](/wp-content/uploads/gij-jira-cloud-automation-start-2025.png)

4. Click the **DevOps** category to display the Git Integration for Jira triggers. Use these triggers as the basis for your automations.

    ![](/wp-content/uploads/gij-jira-cloud-automation-triggers-2025.png)

5. Configure triggers, conditions, and actions for this rule:

    ![](/wp-content/uploads/gij-jira-cloud-automation-example-rule-2025.png)

    a. **TRIGGER** – This rule triggers when a pull request is created.

    b. **CONDITION** – When the status of the Jira issue is To Do, the rule performs the actions below.

    c. **ACTIONS** – If the conditions are met, the rule assigns the issue to a specific user and transitions the Jira issue to In Progress.

6. Enter a descriptive name for this rule in the provided box.

7. Click **Turn it on** to publish and activate the rule. The new rule appears in the automation list.


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

Let automation handle repetitive tasks while your developers focus on what matters. Automation Templates for Git Integration for Jira help you get started quickly without creating rules from scratch. We've provided templates for common workflows.

All templates from [Atlassian's template library](https://www.atlassian.com/software/jira/automation-template-library/bitbucket-github-gitlab) work with Git Integration for Jira.

<img src='/wp-content/uploads/gij-automation-library-template.png' style='margin:25px auto;max-width:100%;display:block;height:auto;width:470px;' />

With Git Integration for Jira, you can integrate any Git repository with Jira and use any of these automation templates or create your own using [Atlassian's no-code Jira automation engine](https://www.atlassian.com/software/jira/features/automation).

&nbsp;

### Available templates from Atlassian for Git Integration for Jira users

Use these templates from Atlassian as a guide for common use cases:

- [When a commit is created, then transition the Jira issue](https://www.atlassian.com/software/jira/automation-template-library/rules#/rule/1357202)
- [When a PR is created, add a comment to the Jira issue](https://www.atlassian.com/software/jira/automation-template-library/rules#/rule/1357211)
- [When a commit is created, then send Slack message based on assignee](https://www.atlassian.com/software/jira/automation-template-library/rules#/rule/1357149)

&nbsp;

### Common use cases for automation with Git Integration for Jira

- Transition issue state when a commit arrives.
- Transition issue state when a pull/merge request is merged (for example, from IN PROGRESS to DONE).

&nbsp;

### For more powerful conditions

Use [Jira Automation Smart Values](https://support.atlassian.com/jira-software-cloud/docs/what-are-smart-values/) to extract data from your commits and branches for use in automation actions:

- **Take actions based on branch name.** For example:
    - Only transition branches that contain a specific keyword like "WIP" (Work In Progress).
    - Add a comment to an issue when a branch contains a certain keyword.

- **Extract the pullRequest state** (Open vs Merged vs Declined) from a pull request and use it in an [advanced compare condition](https://support.atlassian.com/jira-software-cloud/docs/automation-conditions/).

- **Verify commit messages** contain required elements, like issue keys.

- **Filter by repository** to ensure only certain repos trigger the automation.

- See the full list of [available smart values](https://support.atlassian.com/jira-software-cloud/docs/smart-values-development/).

&nbsp;

### Supported triggers

Git Integration for Jira currently supports the five highlighted triggers shown below. Additional triggers will be supported in future releases.

<img src='/wp-content/uploads/gij-jira-cloud-automation-triggers-2025.png' style='margin:25px auto;width:566px;height:auto;display:block;max-width:100%;' />

&nbsp;

### More Jira automation information

- [Automation basics](https://www.atlassian.com/software/jira/guides/expand-jira/automation)
- [What are smart values?](https://support.atlassian.com/jira-software-cloud/docs/what-are-smart-values/)
- [Automation conditions](https://support.atlassian.com/jira-software-cloud/docs/automation-conditions/)

<kbd>Last updated: December 2025</kbd>
