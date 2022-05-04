---

title: JQL Searching for Commits and Pull Requests
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# JQL Searching for Commits and Pull Requests

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/643596299/JQL+Searching+for+Commits+and+Pull+Requests>

* * *

Access JQL searching via _Issues and Filters_ > **Search Issues**.

**Limitation**  
Only Jira _**Company-managed**_ projects support development JQL searching. _**Team-managed**_ projects are not currently supported.

## JQL: Commits

|     |
| --- |
| Use the following JQL syntax to locate all Jira issues with more than one commit: |
| ```java<br>development[commits].all > 0<br>``` |

![JQL to find issues with at least one commit](https://bigbrassband.atlassian.net/wiki/download/attachments/643596299/jql-seach-commit-issues.png?version=2&modificationDate=1595583094730&cacheVersion=1&api=v2)

|     |
| --- |
| **Example:** Find all issues with more than 15 commits: |
| ```java<br>development[commits].all > 15<br>``` |

## JQL: Pull Requests

Use the following JQL syntax to locate all Jira issues with more than one pull request:

```java
 development[pullrequests].all > 0
 development[pullrequests].open > 0 (to only search for open pull requests)
```

![](https://bigbrassband.atlassian.net/wiki/download/attachments/643596299/image-20200724-094910.png?version=1&modificationDate=1595584161928&cacheVersion=1&api=v2)

### Examples:

|     |
| --- |
| Find all issues with more than 5 open or merged pull requests: |
| ```java<br>development[pullrequests].all > 5<br>``` |

|     |
| --- |
| Find all issues with any open pull requests: |
| ```java<br>development[pullrequests].open > 0<br>``` |

[**More information from Atlassian**](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-developer-reference-967312910.html)

### More related topics about Jira development information

*   Page:
    
    [How can a Jira administrator enable or disable Jira Development Information?](/wiki/spaces/GITCLOUD/pages/1941373145) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Jira Development Information settings](/wiki/spaces/GITCLOUD/pages/1941373113/Jira+Development+Information+settings) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Development Information Views](/wiki/spaces/GITCLOUD/pages/643203115/Development+Information+Views) (Git Integration for Jira Cloud)
    
*   Page:
    
    [JQL Searching for Commits and Pull Requests](/wiki/spaces/GITCLOUD/pages/643596299/JQL+Searching+for+Commits+and+Pull+Requests) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Jira Cloud Smart Commits and Workflow Triggers](/wiki/spaces/GITCLOUD/pages/144310383/Jira+Cloud+Smart+Commits+and+Workflow+Triggers) (Git Integration for Jira Cloud)