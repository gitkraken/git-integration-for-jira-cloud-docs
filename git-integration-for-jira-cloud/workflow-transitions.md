---

title: Workflow transitions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Workflow transitions

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025389/Workflow+transitions>

* * *

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

[« Advanced examples](/wiki/spaces/GITCLOUD/pages/1923025375/Advanced+examples)

[Viewing workflows »](/wiki/spaces/GITCLOUD/pages/1923025415/Viewing+workflows)

### More related topics about smart commits

*   Page:
    
    [Smart commits](/wiki/spaces/GITCLOUD/pages/1923025332/Smart+commits) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Basic commands](/wiki/spaces/GITCLOUD/pages/1923025355/Basic+commands) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Workflow transitions](/wiki/spaces/GITCLOUD/pages/1923025389/Workflow+transitions) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Advanced examples](/wiki/spaces/GITCLOUD/pages/1923025375/Advanced+examples) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Viewing workflows](/wiki/spaces/GITCLOUD/pages/1923025415/Viewing+workflows) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Smart commits general settings](/wiki/spaces/GITCLOUD/pages/1923025462/Smart+commits+general+settings) (Git Integration for Jira Cloud)