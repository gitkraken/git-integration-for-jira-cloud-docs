---

title: JQL Searching for Commits and Pull Requests
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Access JQL searching via _Issues and Filters_ > **Search Issues**.

**Limitation**
Only Jira _**Company-managed**_ projects support development JQL searching. _**Team-managed**_ projects are not currently supported.

## JQL: Commits

Use the following JQL syntax to locate all Jira issues with more than one commit:
```java<br>development[commits].all > 0<br>```

![JQL to find issues with at least one commit](https://bigbrassband.atlassian.net/wiki/download/attachments/643596299/jql-seach-commit-issues.png?version=2&modificationDate=1595583094730&cacheVersion=1&api=v2)


**Example:** Find all issues with more than 15 commits:
```java<br>development[commits].all > 15<br>```

## JQL: Pull Requests

Use the following JQL syntax to locate all Jira issues with more than one pull request:

```java
 development[pullrequests].all > 0
 development[pullrequests].open > 0 (to only search for open pull requests)
```

![](https://bigbrassband.atlassian.net/wiki/download/attachments/643596299/image-20200724-094910.png?version=1&modificationDate=1595584161928&cacheVersion=1&api=v2)

### Examples:

Find all issues with more than 5 open or merged pull requests:
```java<br>development[pullrequests].all > 5<br>```

Find all issues with any open pull requests: |
```java<br>development[pullrequests].open > 0<br>```

[**More information from Atlassian**](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-developer-reference-967312910.html)

