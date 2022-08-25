---

title: Microsoft webhook events
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
We detect a type of integration by header in webhook requests (except Microsoft).

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Microsoft doesn't send a header by default.
    </div>
    </div>
</div>
<br>

## Microsoft (Push Events)

_Type_<br>
`"^push"`

_Request URI_<br>
`/api/1/webhook/reindex/install/`**\<secret\_key\>**`/web`

_Request headers_<br>
**Content-type:** `application/json`

_**Request payload example:**_<br>
```json
{
  "eventType": "git.push",
  ...
  "resource": {
    ...
    "repository": {
      "id": "f0234cc5-5891-4044-a45e-c1d9d4b33562",
      "name": "TestWebHook",
      "url": "https://dev.azure.com/johnsmith/_apis/git/repositories/f0234cc5-5891-4044-a45e-c1d9d4b33562",
      "project": {
        "id": "f12f9cc9-387e-43f7-9023-e871c94bfebc",
        ....
       ...
      },
     ....
      "remoteUrl": "https://dev.azure.com/johnsmith/TestWebHook/_git/WebHook"
    },
	...
}
```

## Microsoft (Pull Request Created Events)

_Type_<br>
**pullRequestEvents:** `"^git\.pullrequest\.created$"`

_Request URI_<br>
`/api/1/webhook/reindex/install/`**\<secret\_key\>**`/web`

_Request headers_<br>
**Content-type:** `application/json`

_**Request payload example:**_<br>
```json
{  
  "publisherId": "tfs",
  "resourceContainers": {
    "project": {
      "baseUrl": "https://dev.azure.com/jsmith0806/",
      "id": "67836bbd-b388-4afe-8b8a-105ea137e46e"
    },
    "collection": {
      "baseUrl": "https://dev.azure.com/jsmith0806/",
      "id": "d017770c-312c-4495-ba35-62e4dd65c031"
    },
    "account": {
      "baseUrl": "https://dev.azure.com/jsmith0806/",
      "id": "7b7c74dd-d911-4b37-8a96-9b629140cff6"
    }
  },
  "resource": {
    "mergeId": "61ea7c1d-06bd-4bd4-80d4-64e63e5224b6",
    "_links": {
      "web": {"href": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks/pullrequest/1"}
    },  
    ---   
    "repository": {
      "sshUrl": "git@ssh.dev.azure.com:v3/jsmith0806/Webhooks/Webhooks",
      "webUrl": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",
      "name": "Webhooks",
      "remoteUrl": "https://natalya0806@dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",
      "url": "https://dev.azure.com/jsmith0806/67836bbd-b388-4afe-8b8a-105ea137e46e/_apis/git/repositories/a125ea5e-b64d-4ddc-b0ef-f926caa5cd0d"
    },
    "pullRequestId": 1,
    "title": "PROJ-4: Merge test-branch to master",
    "url": "https://dev.azure.com/jsmith0806/67836bbd-b388-4afe-8b8a-105ea137e46e/_apis/git/repositories/a125ea5e-b64d-4ddc-b0ef-f926caa5cd0d/pullRequests/1",
    ...    
  }, 
  "eventType": "git.pullrequest.created",
  ...
}
```

## Microsoft (Pull Request Updated Events)

_Type_<br>
**pullRequestEvents:** `"^git\.pullrequest\.updated$"`

_Request URI_<br>
`/api/1/webhook/reindex/install/`**\<secret\_key\>**`/web`

_Request headers_<br>
**Content-type:** `application/json`<br>

_**Request payload example:**_<br>
```json
{  
  "publisherId": "tfs",
  "resourceContainers": {
    "project": {
      "baseUrl": "https://dev.azure.com/jsmith0806/",
      "id": "67836bbd-b388-4afe-8b8a-105ea137e46e"
    },
    "collection": {
      "baseUrl": "https://dev.azure.com/jsmith0806/",
      "id": "d017770c-312c-4495-ba35-62e4dd65c031"
    },
    "account": {
      "baseUrl": "https://dev.azure.com/jsmith0806/",
      "id": "7b7c74dd-d911-4b37-8a96-9b629140cff6"
    }
  },
  "resource": {
    "mergeId": "61ea7c1d-06bd-4bd4-80d4-64e63e5224b6",
    "_links": {
      "web": {"href": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks/pullrequest/1"}
    },
    ...
    "repository": {
      "sshUrl": "git@ssh.dev.azure.com:v3/jsmith0806/Webhooks/Webhooks",
      "webUrl": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",
      "name": "Webhooks",
      "remoteUrl": "https://natalya0806@dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",
      "url": "https://dev.azure.com/jsmith0806/67836bbd-b388-4afe-8b8a-105ea137e46e/_apis/git/repositories/a125ea5e-b64d-4ddc-b0ef-f926caa5cd0d"
    },
    "pullRequestId": 1,
    "title": "PROJ-4: Merge test-branch to master",    
    "url": "https://dev.azure.com/jsmith0806/67836bbd-b388-4afe-8b8a-105ea137e46e/_apis/git/repositories/a125ea5e-b64d-4ddc-b0ef-f926caa5cd0d/pullRequests/1",
    "artifactId": "vstfs:///Git/PullRequestId/67836bbd-b388-4afe-8b8a-105ea137e46e%2fa125ea5e-b64d-4ddc-b0ef-f926caa5cd0d%2f1"
  },
  "eventType": "git.pullrequest.updated",
  ...
}
```

## Other webhook type events

[GitHub webhook events](/git-integration-for-jira-cloud/gitHub-webhook-events)

[GitLab webhook events](/git-integration-for-jira-cloud/gitlab-webhook-events)

[AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events)

[Bitbucket webhook events](/git-integration-for-jira-cloud/bitbucket-webhook-events)

