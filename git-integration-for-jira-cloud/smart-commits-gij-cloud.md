---

title: Smart commits GIJ Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Smart commits allows your team to perform actions on Jira issues from a single commit. Users can enter the issue key and the desired action such as time tracking or closing an issue.

## Getting started

The smart commit processing is **active by default** and can be enabled/disabled via the repository settings:

*   Manage integrations page **➜** _Git repo type_ **➜** ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions **➜** Edit integration **➜** **Feature settings**.

*   Manage repositories page **➜** ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions **➜** Edit repository **➜** **Feature settings**.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025332/gitcloud-repo-cfg-smart-commits.png?version=1&modificationDate=1650252785364&cacheVersion=1&api=v2&width=312&height=108)

Smart commits support for project keys that has an underscore "\_" character.
Smart commits support for all alphabet characters.
Smart commits support for case-insensitive smart commits.


Smart commits configuration checklist:

*   **The Jira DVCS Connector Plugin is not required.**
    The Git Integration for Jira app has the functions of the connector plugin plus more integration support and features.

*   **Your Jira e-mail address and Git commit e-mail address matches.** IMPORTANT
    The commit author's email should match exactly with a user's email in Jira. If they do not match, the application will add the commit as the app.

*   **E-mail address is not shared by other Jira users.**
    Verify that this email address is used by only one Jira user.

*   **Advanced:** Verify that the workflow conditions and validators are able to process successfully.



The Git Integration app supports smart commit by adding a simple syntax to a commit message.

The basic syntax for a Smart commit message is:

```java
<ISSUE_KEY> <ignored text> #<command> <optional command_params>
```


To know more about syntax, commands and examples on Smart Commits, see [**Processing Jira Software Issues with Smart Commit Messages**](https://support.atlassian.com/bitbucket-cloud/docs/use-smart-commits/) at the Atlassian website or proceed to the next page.

[« Linking git commits to Jira issues](/wiki/spaces/GITCLOUD/pages/1923025229/Linking+git+commits+to+Jira+issues)

[Smart commit: Basic commands »](/git-integration-for-jira-cloud/Basic-commands)

