---

title: New GitLab v10+ authentication
description:
taxonomy:
    category: git-integration-for-jira-cloud

---


# New GitLab v10+ authentication

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923023311>

* * *

GitLab v10+ stopped accepting username/password credentials for API access and will only recognize Personal Access Tokens (PAT) and OAuth authentications. Service users are strongly advised to switch from using username/password for GitLab.com and newer versions of GitLab Server (CE/EE) to using Personal Access Tokens.

For GitLab Server service users, they won't see the issue until they upgrade their GitLab Servers to version 10 and higher. Git Integration for Jira app offers pre-v10 GitLab Server users as a Legacy connection option.

To access a Git repository over HTTP, use the username as the _username_ and the PAT for the _password_.

To pass the private access token (for example: `XpigzF1JxMnAZ7mn9qgN`) to an API call with GitLab.com:

```java
curl --header "Private-Token: XpigzF1JxMnAZ7mn9qgN" https://gitlab.com/api/v4/projects?membership=true
```

  
For more information on GitLab personal access token, see [**GitLab: Personal Access Token**](https://docs.gitlab.com/ce/user/profile/personal_access_tokens.html).

[« Setup GitLab Server to respond to incoming network API calls](/wiki/spaces/GITCLOUD/pages/1923023297/Setup+GitLab+Server+to+respond+to+incoming+network+API+calls)

[General settings: Improving Jira performance »](/wiki/pages/createpage.action?spaceKey=GITCLOUD&title=General%20settings%3A%20Improving%20Jira%20performance&linkCreation=true&fromPageId=1923023311)

### More related topics about getting started for Jira admins

*   Page:
    
    [New GitLab v10+ authentication](/wiki/spaces/GITCLOUD/pages/1923023311) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Setup GitLab Server to respond to incoming network API calls](/wiki/spaces/GITCLOUD/pages/1923023297/Setup+GitLab+Server+to+respond+to+incoming+network+API+calls) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Setting up web linking](/wiki/spaces/GITCLOUD/pages/1923023467/Setting+up+web+linking) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Setting up indexing triggers](/wiki/spaces/GITCLOUD/pages/1923023481/Setting+up+indexing+triggers) (Git Integration for Jira Cloud)