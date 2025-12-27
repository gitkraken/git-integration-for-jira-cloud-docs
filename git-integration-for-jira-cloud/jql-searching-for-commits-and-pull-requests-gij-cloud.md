---

title: JQL Searching for Commits and Pull Requests
description: Learn how to use JQL syntax to search for Jira issues based on commit and pull request activity.
taxonomy:
    category: git-integration-for-jira-cloud

---

<!-- FEATURES -->

Access JQL searching via _Issues and Filters_ ➜ **Search Issues**.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Limitation</b><br>
Only Jira <b><i>Company-managed</i></b> projects support development JQL searching. <b><i>Team-managed</i></b> projects are not currently supported.
    </div>
    </div>
</div>

&nbsp;

## JQL: Commits

Use the following JQL syntax to locate all Jira issues with at least one commit:

```java
development[commits].all > 0
```

![JQL to find issues with at least one commit](/wp-content/uploads/gij-gitcloud-jql-seach-commit-issues.png)

**Example:** Find all issues with more than 15 commits:

```java
development[commits].all > 15
```

&nbsp;

## JQL: Pull Requests

Use the following JQL syntax to locate all Jira issues with at least one pull request:

```java
development[pullrequests].all > 0
development[pullrequests].open > 0 (to search for open pull requests only)
```

![JQL to find issues with at least one pull request](/wp-content/uploads/gij-gitcloud-jql-seach-pull-requests.png)

&nbsp;

### Examples

Find all issues with more than 5 open or merged pull requests:

```java
development[pullrequests].all > 5
```

Find all issues with any open pull requests:

```java
development[pullrequests].open > 0
```

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <a href='https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-developer-reference-967312910.html'><b>More information from Atlassian</b></a>
    </div>
    </div>
</div>

&nbsp;

## More related topics on Jira Development Information

- [Development Information Views](/git-integration-for-jira-cloud/development-information-views-gij-cloud)
- **JQL searching for commits and pull requests** (this page)
- [Jira Cloud Smart Commits and Workflow Triggers](/git-integration-for-jira-cloud/jira-cloud-smart-commits-and-workflow-triggers-gij-cloud/)
- [Jira Development Information general settings](/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud)

<kbd>Last updated: December 2025</kbd>
