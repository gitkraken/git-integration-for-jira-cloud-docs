---

title: Smart Commits Overview
description:
taxonomy:
    category: git-integration-for-jira-cloud

---


Git Integration for Jira. See Git commits in Jira.

**What's on this page:**
- [Introduction](#introduction)
- [Getting started](#getting-started)
- [Workflow Transitions](#workflow-transitions)
- [Viewing Workflows](#viewing-workflows)
- [Smart Commits General Setting](#smart-commits-general-setting)
  - [Max commit age](#max-commit-age)
- [Did You Know?](#did-you-know)

* * *

## Introduction

Smart commits allows your team to perform actions on Jira issues from a single commit.  Users can enter the issue key and the desired action such as time tracking or closing an issue.

The smart commit processing is **active by default** and can be enabled/disabled via the **Repository settings** _(Apps ➜ Git Integration: Manage integrations ➜ Actions ➜ Edit integration ➜ click a repository ➜ **Feature settings**)_:

![](https://bigbrassband.atlassian.net/wiki/download/attachments/109314182/gitcloud-edit-repo-feature-cfg-sel.png?version=1&modificationDate=1650363840596&cacheVersion=1&api=v2)

<br>

## Getting started

Smart commits configuration checklist:

*   The Jira DVCS Connector Plugin is not required.

*   Your Jira e-mail address and Git commit e-mail address matches.

*   E-mail address is not shared by other Jira users.

<br>

The basic syntax for a smart commit message is:

\<ISSUE\_KEY\> _\<ignored text\>_ \#\<command\> _\<optional command\_params\>_

Using the format above, the smart commit structure will actually look like this:

**TST-123** **\#comment** fixed bug **\#time** `1h 30m` Bug fixes 

In the above example, the commit is associated to **TST-123**, adds the comment "fixed bug" to the **Issue** ➜ **Comment** tab, logs the time of 1 hour and 30 minutes with worklog comment "Bug fixes" to the Jira issue.

For multi-line commit messages, the following examples show correct usage of the smart commit message:

**TST-1** implemented feature 1<br>
**\#comment** `some comment`<br>
`in Jira`<br>
`on several lines`<br>
**\#resolve**
**TST-2** **\#time** `1h 30m`

The above example is a valid multi-line commit message.

The **`#label`** command will add a new label to a Jira issue. If more than one Jira issue is referenced, the labels are added to all mentioned Jira issues. Multiple labels can be created by putting spaces between words.

**Usage:**

**GITCL-443 GITCL-247 GITCL-214 \#label** `admin@example.com user1@example.com requested-feature new-feature` **\#comment** `Return email when implemented`

**In the above example:**

The labels **admin@example.com**, **user1@example.com**, **requested-feature** and **new-feature** are applied to Jira issues **GITCL-443**, **GITCL-247** and **GITCL-214**. Also, the comment is added to each of the mentioned Jira issues.

* * *

## Workflow Transitions

<img src='https://bigbrassband.com/docimgs/jira-simple-workflow-144.png' style='margin:25px auto;max-width:100%;' alt='shows workflow transition names and arrow process' />

The name of the status is the transition. So, for the example above, the valid transitions from **DONE** are:

*   **\#to-do**
*   **\#in-progress**
*   **\#in-review**

## Viewing Workflows

1.  Open an issue and click **View Workflow** from the context of the issue (near the issue’s **Status**).

2.  Hover a status.

    ![shows workflow transition names process flow when mouse is hovered](https://bigbrassband.com/docimgs/jira-workflow-hover.png)

<br>

## Smart Commits General Setting

<img src='https://bigbrassband.com/docimgs/gen-cfg-smart-commits-max-age.png' style='max-width:100%;margin:25px auto;border:1px solid #ccc' alt='General Settings smart commits max age' />

### Max commit age

<b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>JIRA CLOUD</b> <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>DEV INFO</b>

This setting is a hidden feature in Git Integration for Jira Cloud and Dev Info for Jira Cloud. All commits which are older than this setting (in seconds) shall be ignored for smart commits processing.<br><br>The default value is **1209600** seconds (14 days).


* * *

## Did You Know?

**Jira User**<br>
The committers’ email address in the git configuration must match with the email address of the corresponding Jira user (or vice versa) for the smart commit to work.

**Project Permissions**<br>
The Jira user must have the appropriate project permissions to transition issues.

**Workflow Transition**<br>
When you hover a status on the Issue Workflow - it will highlight available transitions. This is the transition name that is used in Smart Commits.

**Email Notifications**<br>
If a smart commit fails, an email notification is sent to either the Jira user, or to the Git user if a Jira user cannot be identified.

**Transition Names**<br>
To avoid conflict when transitioning issues, give a unique name to a workflow transition.

**Multi-line Commits**<br>
The Git Integration for Jira app, support for multi-line commit messages for Smart Commits has been implemented.

**Smart Commit Status**<br>
The commit status shown on the Issue page depends on the Smart Commits setting that was set at the time the commits were processed.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Need to know more? Read further at <a href='/git-integration-for-jira-cloud/smart-commits-gij-cloud'>Documentation: Smart Commits</a>.
    </div>
    </div>
</div>

