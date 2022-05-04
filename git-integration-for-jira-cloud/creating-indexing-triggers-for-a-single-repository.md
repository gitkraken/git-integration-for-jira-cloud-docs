---

title: Creating indexing triggers for a single repository
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Creating indexing triggers for a single repository

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/171213231/Creating+indexing+triggers+for+a+single+repository>

* * *

Create an indexing trigger that can be initiated for any **individual** repository. It can be used with continuous integration service.

_**Required headers:**_

*   'x-bbb-webhook-type': `push`
    
*   'Content-Type': `application/json`
    

_**Optional headers:**_

*   'x-bbb-webhook-id' -- Can be any string representing the _id_ of the request to be used.
    

|     |
| --- |
| **Usage examples:** |
| ```java<br>curl -H 'x-bbb-webhook-type: push' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url<br>``` |
| ```java<br>curl -H 'x-bbb-webhook-type: push' -H 'x-bbb-webhook-id: id-string' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url<br>``` |

|     |
| --- |
| **Payload.json** |
| ```java<br>{<br>  "origin": "repository-origin"<br>}<br>``` |

## Webhook type events

*   Page:
    
    [GitHub webhook events](/wiki/spaces/GITCLOUD/pages/1921482779/GitHub+webhook+events) (Git Integration for Jira Cloud)
    
*   Page:
    
    [GitLab webhook events](/wiki/spaces/GITCLOUD/pages/1922465801/GitLab+webhook+events) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Microsoft webhook events](/wiki/spaces/GITCLOUD/pages/1921876015/Microsoft+webhook+events) (Git Integration for Jira Cloud)
    
*   Page:
    
    [AWS CodeCommit webhook events](/wiki/spaces/GITCLOUD/pages/1922203671/AWS+CodeCommit+webhook+events) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Bitbucket webhook events](/wiki/spaces/GITCLOUD/pages/1921548328/Bitbucket+webhook+events) (Git Integration for Jira Cloud)
    

### More related articles

*   Page:
    
    [Creating indexing triggers for a single repository](/wiki/spaces/GITCLOUD/pages/171213231/Creating+indexing+triggers+for+a+single+repository) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for GitHub repository](/wiki/spaces/GITCLOUD/pages/171377213/Adding+webhooks+for+GitHub+repository) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for GitLab repository](/wiki/spaces/GITCLOUD/pages/171377217/Adding+webhooks+for+GitLab+repository) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Webhook GitHub Organization support](/wiki/spaces/GITCLOUD/pages/171278791/Webhook+GitHub+Organization+support) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for Azure DevOps Repos | VSTS](/wiki/spaces/GITCLOUD/pages/172294150/Adding+webhooks+for+Azure+DevOps+Repos+%7C+VSTS) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for Azure DevOps Server | TFS](/wiki/spaces/GITCLOUD/pages/234782736/Adding+webhooks+for+Azure+DevOps+Server+%7C+TFS) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks for Bitbucket Cloud](/wiki/spaces/GITCLOUD/pages/467271681/Adding+webhooks+for+Bitbucket+Cloud) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding webhooks to AWS CodeCommit](/wiki/spaces/GITCLOUD/pages/864288787/Adding+webhooks+to+AWS+CodeCommit) (Git Integration for Jira Cloud)