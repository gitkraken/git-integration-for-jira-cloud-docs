---

title: Email Notifications from Atlassian for Smart Commits
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
**What’s on this page:**

## Background

Sometimes users make mistakes in constructing smart commits syntax or tries to use the name of the transition which is not available for the current issue status. Thus, receiving smart commit errors and get email notifications about the said issue.

## Prerequisite

Users should have a matched email address for Jira and the integrated git host.

## Test Cases

Smart Commits fail due to a wrong command.

For some example insights:

*   For a valid issue key, intentionally make an error in the smart commit command. This will cause Jira to still ensure that the command reaches the destination and will show it on the Commits tab in the Development panel.

*   For an invalid issue-key, the notification should be triggered for the failure of any command used.


## Examples of Smart Commits Messages that Fail

#### **1\. Smart commits without any value after the command**
For example, **JIRA-1** **#time**  or **TES-1** **#comment**
![smart commits error email notification example 1](https://bigbrassband.atlassian.net/wiki/download/attachments/805437441/sc-error01-example.png?version=1&modificationDate=1602060911583&cacheVersion=1&api=v2)
![smart commits error email notification example 2](https://bigbrassband.atlassian.net/wiki/download/attachments/805437441/sc-error01-example2.png?version=1&modificationDate=1602061171866&cacheVersion=1&api=v2)

#### **2\. Smart commits with an invalid issue-key**
For example, **JIRA-700000** **#time** **4h 30m**
![](https://bigbrassband.atlassian.net/wiki/download/attachments/805437441/sc-error02-example.png?version=1&modificationDate=1602061437954&cacheVersion=1&api=v2)

#### **3\. Smart commits with a non-editable workflow state**
Example:
![](https://bigbrassband.atlassian.net/wiki/download/attachments/805437441/bitbucket-non-editable-workflow-state.png?version=1&modificationDate=1602061633086&cacheVersion=1&api=v2)

## Examples of Smart Commits Messages that are Processed Correctly

#### **1\. Smart commits with a command and a value for it**
Example:  <br>**JIRA-1** **#time** **1w 2d 4h 30m**
_The above example adds the time of 1 week, 2 days, 4 hours and 30 minutes (220.5 hours) to the Jira issue._

#### **2\. Smart commits with a correct transition name**
Example:  <br>**JIRA-1** **#close**
_The above example will move the stage of the Jira issue as_ CLOSED.