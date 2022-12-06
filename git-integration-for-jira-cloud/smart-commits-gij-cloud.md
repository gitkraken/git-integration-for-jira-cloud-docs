---

title: Smart commits
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Smart commits allows your team to perform actions on Jira issues from a single commit. Users can enter the issue key and the desired action such as time tracking or closing an issue.

## Getting started

The smart commit processing is **active by default** and can be enabled/disabled one of the following access locations:

*   Manage repositories page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit repository ➜ **Feature settings**.

*   Manage repositories page ➜ click a repository -- to open its **Feature Settings** page.

&nbsp;

<img src='/wp-content/uploads/gij-gitcloud-repo-cfg-smart-commits.png' style='margin:5px auto 10px auto;max-width:100%;display:block' />

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

![](/wp-content/uploads/gij-smart-commit-message-basic-syntax.png)


To know more about syntax, commands and examples on Smart Commits, see [**Processing Jira Software Issues with Smart Commit Messages**](https://support.atlassian.com/bitbucket-cloud/docs/use-smart-commits/) at the Atlassian website or proceed to the next page.

&nbsp;

## See next topics below

[**Prev:** Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud)

[**Next:** Smart commit - Basic commands](/git-integration-for-jira-cloud/basic-commands-gij-cloud)

