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

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/i21p45xb5y?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:12px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/i21p45xb5y'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

&nbsp;
## How to set up automation templates

Create a rule to configure triggers and actions for automating tasks. There are two levels:

### Project level (projects)

1.  Open a project to work on, then go to ![](/wp-content/uploads/actions-icon.png) **Project settings**.

    ![](/wp-content/uploads/gij-gitcloud-automation-proj-level.png)

2.  On the sidebar, click **Automation**.

3.  Click the ![zap](/wp-content/uploads/gij-zap-icon.png) **Rules** tab.

4.  Click **Create rule** to create a new automation rule.

    ![](/wp-content/uploads/gij-jira-cloud-automation-start.png)

5.  Configure triggers, conditions and actions for this rule:

    ![](/wp-content/uploads/gij-jira-cloud-automation-example-rule.png)

    a.  **TRIGGER** – This rule will trigger when a pull request is created.

    b.  **CONDITION** – When the status of the Jira issue is IN PROGRESS, it will perform the actions below.

    c.  **ACTIONS** – If the condition(s) are met, the rule will fire up the actions, assign the issue to a specific user and transitions the Jira issue to IN REVIEW.

6.  Enter a descriptive name for this rule in the provided box.

7.  Click **Turn it on** to publish and activate it. The new rule is added to the automation list.


<img src='/wp-content/uploads/gij-jira-cloud-automation-list.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

### Global administration level (system)

1.  On your Jira dashboard, go to menu **Jira Settings** ➜ **System**.

    ![](/wp-content/uploads/gij-jira-cloud-administration-settings-menu.png)

2.  On the left sidebar, scroll to the bottom (Automation) and click **Automation rules**.

    ![](/wp-content/uploads/gij-gitcloud-automation-proj-level.png)

3.  Click the **Rules** tab.

4.  Click **Create rule** to create a new automation rule.

    ![](/wp-content/uploads/gij-jira-cloud-automation-start.png)

5.  Configure triggers, conditions and actions for this rule:

    ![](/wp-content/uploads/gij-jira-cloud-automation-example-rule.png)
    
    a.  **TRIGGER** – This rule will trigger when a pull request is created.

    b.  **CONDITION** – When the status of the Jira issue is IN PROGRESS, it will perform the actions below.

    c.  **ACTIONS** – If the condition(s) are met, the rule will fire up the actions, assign the issue to a specific user and transitions the Jira issue to IN REVIEW.

6.  Enter a descriptive name for this rule in the provided box.

7.  Click **Turn it on** to publish and activate it. The new rule is added to the automation list.


<img src='/wp-content/uploads/gij-jira-cloud-automation-list.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

## Known issue

![(info)](/wp-content/uploads/bbb-info-20.png) The limitation of Git Integration for Jira (GIJ) app not working with Automation for Jira (A4J) Lite is not a GIJ limitation but an Atlassian limitation.

&nbsp;
## Advanced Examples

For advanced examples, see sub-page [Automation Advanced Examples](/git-integration-for-jira-cloud/git-integration-jira-automation-advanced-examples-gij-cloud).

