---

title: Workflow transitions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The simple Jira workflow does not contain explicit transition names. These kind of workflow with no explicit transition names are becoming more popular as Atlassian is suggesting them to administrators upon project creation.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025389/gitcloud-jira-workflow-chart.png?version=1&modificationDate=1634729137964&cacheVersion=1&api=v2&width=217&height=241)

The name of the status is the transition. So, using the basic example above, the valid transitions from DONE are:

*   **#to-do**

*   **#in-progress**

*   **#in-review**


**Transition names**
The workflow transition names must be unique.

**Absence of transition names**
When there are no transition names — just use the status names. If there is a space, replace it with "–" (hyphens). For example, `CODE REVIEW` becomes `#code-review`.

**Commit authors**
Only letters and "-" (dash) are valid for workflow transition names for smart commits. Any other characters are treated as invalid. Smart commits will ONLY use the valid characters before the occurrence of an invalid character for processing.

**Jira Administrators**
When adding transitions in the Workflow editor, make transition names simple and easy to remember. Only use letters and only one space between words.

[« Advanced examples](/git-integration-for-jira-cloud/Advanced-examples-gij-cloud/)

[Viewing workflows »](/git-integration-for-jira-cloud/Viewing-workflows-gij-cloud/)

