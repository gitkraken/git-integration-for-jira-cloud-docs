---

title: Smart commits
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Smart commits allows your team to perform actions on Jira issues from a single commit. Users can enter the issue key and the desired action such as time tracking or closing an issue.

&nbsp;

**On this page:**
- [Getting started](#getting-started)
- [Basic commands](#basic-commands)
- [Advanced examples](#advanced-examples)
- [Workflow transitions](#workflow-transitions)
- [Viewing workflows](#viewing-workflows)
- [General settings](#general-settings)
- [Jira Cloud Smart Commits and Workflow Triggers](#jira-cloud-smart-commits-and-workflow-triggers)
- [Automatic Workflow Triggers](#automatic-workflow-triggers)
- [Email notifications for Smart Commits](#email-notifications-for-smart-commits)

&nbsp;

* * *

&nbsp;

## Getting started

The smart commit processing is **active by default** and can be enabled/disabled via the following access locations:

*   Manage repositories page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit repository ➜ **Feature settings**.
*   Manage repositories page ➜ click a repository to open its **Feature Settings** page.

<img src='/wp-content/uploads/gij-gitcloud-repo-cfg-smart-commits.png' style='margin:5px auto 10px auto;max-width:100%;display:block' />

<div align=center>In Jira Cloud, Smart Commits is a toggle setting in the repository settings.</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Smart commits support for project keys that has an underscore "_" character.<br>
        Smart commits support for all alphabet characters.<br>
        Smart commits support for case-insensitive smart commits.
    </div>
    </div>
</div>

### Smart commits configuration checklist

*   **The Jira DVCS Connector Plugin is not required.**
    The Git Integration for Jira app has the functions of the connector plugin plus more integration support and features.

*   **Your Jira e-mail address and Git commit e-mail address matches.** <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b>
    The commit author's email should match exactly with a user's email in Jira. If they do not match, the application will add the commit as the app.

*   **E-mail address is not shared by other Jira users.**
    Verify that this email address is used by only one Jira user.

*   **Advanced:** Verify that the workflow conditions and validators are able to process successfully.

### Basic syntax

The basic syntax for a Smart commit message is:

![](/wp-content/uploads/gij-smart-commit-message-basic-syntax.png)

&nbsp;

* * *

&nbsp;

## Basic commands

There are smart commits commands that you can use in your commit messages.

### \#comment

This command works both in Jira Server/Cloud.

The `#comment` command will add a comment to a Jira issue.

**Syntax:**
`ISSUE_KEY #comment [your comment text]`

**Examples:**
`GIT-264 #comment Resolved conflicts.`
`GIT-1720 #comment Plugin version change from 2.8.2 to 2.8.3. Build number change from 69 to 70.`

The above examples will add the specified comment text against the Jira issues.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The committers' email address in the git configuration must match with the email address of the corresponding Jira user (or vice versa) to comment on issues.
    </div>
    </div>
</div>

### \#time

This command works both in Jira Server/Cloud.

The `#time` command will record time tracking information against a Jira issue.

**Syntax:**
`ISSUE_KEY #time [Some amount in Jira time syntax] [Your worklog comment text]`

**Examples:**
`GIT-264 #time 1w 6d 13h 52m Total work logged.`
`GIT-1720 #time 1h 20m Merged to master. Released to marketplace.`

The above examples will add the respective time and worklog comment text against the Jira issues.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Jira time tracking feature allows users to log the length of time spent working on issues. Jira administrators must have enabled this feature for this smart commit to work.
    </div>
    </div>
</div>

### \#\<transition-name\>

This command works both in Jira Server/Cloud.

The `#<transition-name>` command will move the Jira issue to a particular workflow state.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Jira user must have the appropriate project permissions to be able to transition issues.
    </div>
    </div>
</div>

**Syntax:**
`ISSUE_KEY #<transition-name> [Your commit comment text]`

**Examples:**
`GIT-264 #code-review For review.`
`GIT-1720 #close Closing ticket. #comment Tasks completed.`

The first example will transition the Jira issue to the specified workflow state and adds the comment message to the commit.

The second example will transition the Jira issue to the specified workflow state, adds the comment "_**Closing ticket**_" to the Comment tab and adds the specified comment, "_**Task completed**_" to the mentioned Jira issue.

For more information on transitions and workflow names, see the [Workflow Transitions](#workflow-transitions) section.

### \#assign

This command works both in Jira Server/Cloud.

The `#assign` command will assign the particular issue to the specified Jira user.

**Syntax:**
`ISSUE_KEY #assign [Jira username or email of Jira user]`

**Examples:**
`GIT-1925 #assign johnsmith`
`GIT-1961 #assign johnsmith@example.com`

### \#label

This command works both in Jira Server/Cloud.

The `#label` command will add a new label to a Jira issue. If more than one Jira issue is referenced, the labels are added to all mentioned Jira issues. Multiple labels can be created by putting spaces between words.

**Syntax:**
`ISSUE_KEY(S) #label [label1] .. [labeln]`

**Examples:**
`GITCL-443 #label bucketbreakfix bucketenhancement`
`GITCL-443 GITCL-247 GITCL-214 #label admin@example.com user1@example.com requested-feature new-feature #comment Return email when implemented`

&nbsp;

* * *

&nbsp;

## Advanced examples

### A single action on a single issue

**Example:**
`TEST-100 #time 2w 1d 4h 30m This is a time log comment`

Records the specified worklog `#time` of **2 weeks, 1 day, 4 hours and 30 minutes** and adds worklog comment "_This is a time log comment_" to the issue, TEST-100.

### Multiple actions on a single issue

**Example:**
`TEST-100 #time 4h 30m Fix null pointers #comment Fixed code #resolve`

Logs specified `#time` of **4 hours and 30 minutes** and add worklog comment "_Fixed null pointers_" to the issue, TEST-100; adds the `#comment` "Fixed code" and resolves the issue.

### A single action on multiple issues

**Example:**
`TEST-100 TEST-101 TEST-102 #resolve`

Resolves specified issues.

### Multiple actions on multiple issues

**Example:**
`TEST-100 TEST-101 TEST-102 #resolve #time 2d 4h #comment Fixed code`

Resolves specified issues; logs specified `#time` of **2 days and 4 hours** and adds `#comment` "Fixed code" against the issues.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>VERSION 2.6.33+</b><br>
        Implemented support for multi-line commit messages with smart commits.
    </div>
    </div>
</div>

### Multi-line commit messages

The following examples show correct usage of the smart commit message:

```bash
TST-1 implemented feature 1
TST-1 #comment some comment
in Jira
on several lines
TST-1 #resolve
TST-2 #time 1h 30m
```

_In this example, an issue key that is present on every line is a valid multi-line commit message._

```bash
TST-1 implemented feature 1
#comment some comment
in Jira on several lines
#resolve TST-2
#time 1h 30m
```

_This is the equivalent smart commit message based from the above example._

```bash
TEST-3 Background color of settings should be lighter
TEST-3 #in-progress #time 1h
TEST-4 resolve TEST-2 #resolve
```

_This example, containing several issue keys, is also a valid multi-line smart commit message._

&nbsp;

* * *

&nbsp;

## Workflow transitions

The simple Jira workflow does not contain explicit transition names. These kind of workflow with no explicit transition names are becoming more popular as Atlassian is suggesting them to administrators upon project creation.

<img src='/wp-content/uploads/gij-gitcloud-jira-workflow-chart.png' width=217 height=241 style='margin:25px auto;display:block;' />

The name of the status is the transition. So, using the basic example above, the valid transitions from <b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>DONE</b> are:

*   **\#to-do**
*   **\#in-progress**
*   **\#in-review**

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Transition names</b><br>
        The workflow transition names must be unique.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Absence of transition names</b><br>
        When there are no transition names — just use the status names. If there is a space, replace it with "–" (hyphens). For example, <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>CODE REVIEW</b> becomes <code>#code-review</code>.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Commit authors</b><br>
        Only letters and "-" (dash) are valid for workflow transition names for smart commits. Any other characters are treated as invalid. Smart commits will ONLY use the valid characters before the occurrence of an invalid character for processing.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira Administrators</b><br>
        When adding transitions in the Workflow editor, make transition names simple and easy to remember. Only use letters and only one space between words.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Viewing workflows

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Accessing the view workflow feature on the Jira issue page requires a user or user group to have the <b>View Read-Only Workflow</b> project permissions.
    </div>
    </div>
</div>

![](/wp-content/uploads/gij-gitcloud-jira-workflow-access-location.png)

You can see the available custom workflow transition commands for use with smart commits by doing the following:

1.  Open an issue and click **View Workflow** from the context of the issue's status.

2.  Hover a status.

    When you hover a status – it will highlight available transitions. This is the transition name that is used in smart commits and not the status name.

    ![](/wp-content/uploads/gij-gitcloud-jira-workflow-issue-hover.png)

Below is an example using the above workflow where the issue is in IN PROGRESS status and want to send it to CODE REVIEW status:

```bash
<ISSUE_KEY> #send-to-code-review or,
<ISSUE_KEY> #send-to-code and even,
<ISSUE_KEY> #send (yes, this works, as long as it does not conflict with another transition name)
```

Do note that invalid characters can be used in the transition name. Jira accepts most of them and they can be used. However, smart commits will only process letters and dash characters.

Thus, the part of the transition name up to the invalid character can be used for transitions; where spaces become "-".

### Transition name examples

| Transition name | Smart Commit transition |
| :--- | :--- |
| `SEND_TO_QA` | **SEND** |
| `SEND-TO_QA` | **SEND-TO** |
| `SEND TO_QA` | **SEND-TO** |

There must be at least one unique way to call each transition name. If you have multiple transition names from a single status that use the same word, the smart commits will fail.

**Example:** An issue status NEW has these two transition paths:
*   `SEND_TO_DEVELOPMENT`
*   `SEND_TO_BACKLOG`

The invalid characters are used before unique transition names are possible. Both will become "**\#SEND**". Therefore, they are not unique and these transitions will fail.

**Better example:** The transition names have spaces instead:
*   `SEND TO DEVELOPMENT`
*   `SEND TO BACKLOG`

Both of these transitions are smart commit-friendly and the possible transitions are:
*   **\#SEND-TO-D...**
*   **\#SEND-TO-B...**

The "..." indicates the truncation with the least character length to have the transition names be recognized as unique by Smart Commits.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If a smart commit fails, an email notification is sent to either the Jira user, or to the Git user if a Jira user can't be identified.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## General settings

<img src='/wp-content/uploads/gij-gitcloud-smart-commits-general-setting.png' style='display:block;margin:25px auto;max-width:100%' />

<b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>JIRA CLOUD</b> <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>DEV INFO</b>

**Max commit age** – This setting is a hidden feature in Git Integration for Jira Cloud and Dev Info for Jira Cloud. All commits which are older than this setting (in seconds) shall be ignored for smart commits processing. The default value is **1209600** seconds (14 days).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        In case <a href="/git-integration-for-jira-cloud/jira-issue-page-gij-cloud#jira-development-information">when DevInfo for Jira Cloud is enabled</a>, commits shall be sent with <b><i>disabledTransition</i></b> flag.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Jira Cloud Smart Commits and Workflow Triggers

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Administrator note</b><br>
        Both <b>Send Development Information to Jira Cloud</b> and <b>Enable Dev Info Smart Commits & Workflow</b> settings must be enabled for automatic workflow triggers to be enabled.
        <img src='/wp-content/uploads/gij-gitcloud-jira-dev-info-smart-commits-req-sel.png' style='display:block;margin:25px auto 0 auto;max-width:100%' />
    </div>
    </div>
</div>

### General settings effect on Smart Commits commands

Please take note that the following settings will affect availability of specific smart commit commands as outlined below:

| When this General setting is enabled | \#time | \#label |
|:---|:---|:---|
| Jira Cloud Smart Commits | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-not-red.png) |
| Git Integration app Smart Commits | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
|Both Jira Cloud Smart and GIJ app Smart commits | ![](/wp-content/uploads/gij-matrix-open-check-green.png)<br>(doubled \#time and \#comment) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |

### How to enable or disable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers

1.  Install the [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) or the [**Dev Info for Jira**](https://marketplace.atlassian.com/1219270) app.

2.  Navigate to the **General settings** page of the application (_Jira Settings_ ➜ _Apps_ ➜ (sidebar) _General settings_).

3.  Click the **Send Development Information to Jira Cloud** checkbox to mark and enable it. This also allows access to the **Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers** setting.

4.  Click the **Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers** checkbox to mark and enable this setting.

5.  Click **Update** to save the settings.

![](/wp-content/uploads/gij-gitcloud-gencfg-jira-devinfo-options-02.png)

This setting engages the native Jira Cloud Smart Commit processing (only `#time`, `#comment`, and `#transitions`) as well as enables [Automatic Workflow Triggers](#automatic-workflow-triggers).

For more information, see Atlassian's [**Smart Commits**](https://confluence.atlassian.com/adminjiracloud/enable-smart-commits-776830276.html) or [**Automatic Workflow Triggers**](https://confluence.atlassian.com/adminjiracloud/configuring-workflow-triggers-776636696.html) documentation.

&nbsp;

* * *

&nbsp;

## Automatic Workflow Triggers

Use your development activity to make automatic changes in your Jira project workflows. For example:

*   you can configure your Jira workflow to automatically send a Jira issue to <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IN REVIEW</b> status when a pull request is pushed and associated with the issue, or

*   you can send a Jira issue to <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>IN PROGRESS</b> when a commit is pushed and associated with a Jira issue.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Available triggers through the <a href='https://marketplace.atlassian.com/4984' target='_blank'><b>Git Integration for Jira</b></a> and <a href='https://marketplace.atlassian.com/1219270' target='_blank'><b>Dev Info for Jira</b></a> apps:
        <ul>
            <li>Commit created</li>
            <li>Branch created</li>
            <li>Pull request created</li>
            <li>Pull request merged</li>
            <li>Pull request declined (closed)</li>
            <li>Pull request reopened</li>
        </ul>
    </div>
    </div>
</div>

### Configuring automatic workflow triggers

To configure automatic workflow triggers for your project:

1.  Go to <img src='/wp-content/uploads/actions-icon.png' /> **Project settings**.

2.  Select **Workflow** on the sidebar.

3.  Click <img src='/wp-content/uploads/gij-edit-icon-dark.png' /> **Edit** on the _**Actions**_ column.

4.  Click **Text** to display the Diagram in text mode.

5.  Under _**Transitions**_ column, click a transition item.

6.  Click **Add trigger**. The Add trigger dialog is displayed.

    ![](/wp-content/uploads/gij-gitcloud-automatic-workflow-trigger-add-trigger-c.png)

7.  Click **Commit created**.

8.  Click **Add trigger**. This trigger will automatically transition the issue when a related commit is made in a connected repository.

9.  Click **Publish Draft**. This action will publish the currently edited workflow. Create a backup or set it to _**No**_ then click **Publish**.

The automatic workflow trigger is now configured.

### Demo video: Configuring Automatic Workflow Trigger

<div class='embed-container' style='padding-bottom:65%'>
    <iframe width='709' height='461' src='https://fast.wistia.com/embed/iframe/r8fm0tbrcs?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/r8fm0tbrcs'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

&nbsp;

* * *

&nbsp;

## Email notifications for Smart Commits

Sometimes users make mistakes in constructing smart commits syntax or try to use the name of the transition which is not available for the current issue status. In these cases, users receive smart commit errors via email notifications.

### Prerequisite

Users should have a matched email address for Jira and the integrated git host.

### Examples of Smart Commits Messages that Fail

**1. Smart commits without any value after the command**

For example, **JIRA-1** **#time** or **TES-1** **#comment**

![smart commits error email notification example 1](/wp-content/uploads/gij-sc-error01-example.png)

![smart commits error email notification example 2](/wp-content/uploads/gij-sc-error01-example2.png)

**2. Smart commits with an invalid issue-key**

For example, **JIRA-700000** **#time** **4h 30m**

![](/wp-content/uploads/gij-sc-error02-example.png)

**3. Smart commits with a non-editable workflow state**

![](/wp-content/uploads/gij-sc-bitbucket-non-editable-workflow-state.png)

### Examples of Smart Commits Messages that are Processed Correctly

**1. Smart commits with a command and a value for it**

Example: **JIRA-1** **#time** **1w 2d 4h 30m**

_The above example adds the time of 1 week, 2 days, 4 hours and 30 minutes (220.5 hours) to the Jira issue._

**2. Smart commits with a correct transition name**

Example: **JIRA-1** **#close**

_The above example will move the stage of the Jira issue as CLOSED._

&nbsp;

* * *

&nbsp;

[**Prev:** Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud)

[**Next:** Repository Browser](/git-integration-for-jira-cloud/repository-browser-gij-cloud)

