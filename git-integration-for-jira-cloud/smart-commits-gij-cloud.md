---

title: Smart commits
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Smart commits allows your team to perform actions on Jira issues from a single commit. Users can enter the issue key and the desired action such as time tracking or closing an issue.

## Getting started

The smart commit processing is **active by default** and can be enabled/disabled via the repository settings:

*   Manage integrations page **➜** _Git repo type_ **➜**Actions **➜** Edit integration **➜** **Feature settings**.

*   Manage repositories page **➜**Actions **➜** Edit repository **➜** **Feature settings**.

<br>

<img src='https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025332/gitcloud-repo-cfg-smart-commits.png' width=312 height=108 style='margin:5px auto;max-width:100%;border:1px solid #ccc' />

<div align=center>In Jira Cloud, Smart Commits is a toggle setting
in the repository settings.</div>

<br>

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
<br>

Smart commits configuration checklist:

*   **The Jira DVCS Connector Plugin is not required.**<br>
    The Git Integration for Jira app has the functions of the connector plugin plus more integration support and features.

*   **Your Jira e-mail address and Git commit e-mail address matches.** `IMPORTANT`<br>
    The commit author's email should match exactly with a user's email in Jira. If they do not match, the application will add the commit as the app.

*   **E-mail address is not shared by other Jira users.**<br>
    Verify that this email address is used by only one Jira user.

*   **Advanced:** Verify that the workflow conditions and validators are able to process successfully.

<br>

The Git Integration app supports smart commit by adding a simple syntax to a commit message.

The basic syntax for a Smart commit message is:

```powershell
<ISSUE_KEY> <ignored text> #<command> <optional command_params>
```


To know more about syntax, commands and examples on Smart Commits, see [**Processing Jira Software Issues with Smart Commit Messages**](https://support.atlassian.com/bitbucket-cloud/docs/use-smart-commits/) at the Atlassian website or proceed to the next page.

## See next topics below

[Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud)

[Smart commit: Basic commands](/git-integration-for-jira-cloud/basic-commands-gij-cloud)

