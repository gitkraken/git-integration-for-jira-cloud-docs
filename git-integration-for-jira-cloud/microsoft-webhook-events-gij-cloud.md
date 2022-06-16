---

title: Microsoft webhook events
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
We detect a type of integration by header in webhook requests (except Microsoft), Microsoft doesn't send a header by default.

### Microsoft (Push Events)
_Type_  <br>`"^push"`
_Request URI_  <br>`/api/1/webhook/reindex/install/`**<secret\_key>**`/web`
_Request headers_  <br>**Content-type:** `application/json`<br><br>Microsoft doesn’t return a header by default.
_**Request payload example:**_<br><br>```java<br>{<br>  "eventType": "git.push",<br>  ...<br>  "resource": {<br>    ...<br>    "repository": {<br>      "id": "f0234cc5-5891-4044-a45e-c1d9d4b33562",<br>      "name": "TestWebHook",<br>      "url": "https://dev.azure.com/johnsmith/_apis/git/repositories/f0234cc5-5891-4044-a45e-c1d9d4b33562",<br>      "project": {<br>        "id": "f12f9cc9-387e-43f7-9023-e871c94bfebc",<br>        ....<br>       ...<br>      },<br>     ....<br>      "remoteUrl": "https://dev.azure.com/johnsmith/TestWebHook/_git/WebHook"<br>    },<br>	...<br>}<br>```

### Microsoft (Pull Request Created Events)
_Type_  <br>**pullRequestEvents:** `"^git\.pullrequest\.created$"`
_Request URI_  <br>`/api/1/webhook/reindex/install/`**<secret\_key>**`/web`
_Request headers_  <br>**Content-type:** `application/json`<br><br>Microsoft doesn’t return a header by default.
_**Request payload example:**_<br><br>```java<br>{  <br>  "publisherId": "tfs",<br>  "resourceContainers": {<br>    "project": {<br>      "baseUrl": "https://dev.azure.com/jsmith0806/",<br>      "id": "67836bbd-b388-4afe-8b8a-105ea137e46e"<br>    },<br>    "collection": {<br>      "baseUrl": "https://dev.azure.com/jsmith0806/",<br>      "id": "d017770c-312c-4495-ba35-62e4dd65c031"<br>    },<br>    "account": {<br>      "baseUrl": "https://dev.azure.com/jsmith0806/",<br>      "id": "7b7c74dd-d911-4b37-8a96-9b629140cff6"<br>    }<br>  },<br>  "resource": {<br>    "mergeId": "61ea7c1d-06bd-4bd4-80d4-64e63e5224b6",<br>    "_links": {<br>      "web": {"href": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks/pullrequest/1"}<br>    },  <br>    ---   <br>    "repository": {<br>      "sshUrl": "git@ssh.dev.azure.com:v3/jsmith0806/Webhooks/Webhooks",<br>      "webUrl": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",<br>      "name": "Webhooks",<br>      "remoteUrl": "https://natalya0806@dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",<br>      "url": "https://dev.azure.com/jsmith0806/67836bbd-b388-4afe-8b8a-105ea137e46e/_apis/git/repositories/a125ea5e-b64d-4ddc-b0ef-f926caa5cd0d"<br>    },<br>    "pullRequestId": 1,<br>    "title": "PROJ-4: Merge test-branch to master",<br>    "url": "https://dev.azure.com/jsmith0806/67836bbd-b388-4afe-8b8a-105ea137e46e/_apis/git/repositories/a125ea5e-b64d-4ddc-b0ef-f926caa5cd0d/pullRequests/1",<br>    ...    <br>  }, <br>  "eventType": "git.pullrequest.created",<br>  ...<br>}<br>```

### Microsoft (Pull Request Updated Events)
_Type_  <br>**pullRequestEvents:** `"^git\.pullrequest\.updated$"`
_Request URI_  <br>`/api/1/webhook/reindex/install/`**<secret\_key>**`/web`
_Request headers_  <br>**Content-type:** `application/json`<br><br>Microsoft doesn’t return a header by default.
_**Request payload example:**_<br><br>```java<br>{  <br>  "publisherId": "tfs",<br>  "resourceContainers": {<br>    "project": {<br>      "baseUrl": "https://dev.azure.com/jsmith0806/",<br>      "id": "67836bbd-b388-4afe-8b8a-105ea137e46e"<br>    },<br>    "collection": {<br>      "baseUrl": "https://dev.azure.com/jsmith0806/",<br>      "id": "d017770c-312c-4495-ba35-62e4dd65c031"<br>    },<br>    "account": {<br>      "baseUrl": "https://dev.azure.com/jsmith0806/",<br>      "id": "7b7c74dd-d911-4b37-8a96-9b629140cff6"<br>    }<br>  },<br>  "resource": {<br>    "mergeId": "61ea7c1d-06bd-4bd4-80d4-64e63e5224b6",<br>    "_links": {<br>      "web": {"href": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks/pullrequest/1"}<br>    },<br>    ...<br>    "repository": {<br>      "sshUrl": "git@ssh.dev.azure.com:v3/jsmith0806/Webhooks/Webhooks",<br>      "webUrl": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",<br>      "name": "Webhooks",<br>      "remoteUrl": "https://natalya0806@dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",<br>      "url": "https://dev.azure.com/jsmith0806/67836bbd-b388-4afe-8b8a-105ea137e46e/_apis/git/repositories/a125ea5e-b64d-4ddc-b0ef-f926caa5cd0d"<br>    },<br>    "pullRequestId": 1,<br>    "title": "PROJ-4: Merge test-branch to master",    <br>    "url": "https://dev.azure.com/jsmith0806/67836bbd-b388-4afe-8b8a-105ea137e46e/_apis/git/repositories/a125ea5e-b64d-4ddc-b0ef-f926caa5cd0d/pullRequests/1",<br>    "artifactId": "vstfs:///Git/PullRequestId/67836bbd-b388-4afe-8b8a-105ea137e46e%2fa125ea5e-b64d-4ddc-b0ef-f926caa5cd0d%2f1"<br>  },<br>  "eventType": "git.pullrequest.updated",<br>  ...<br>}<br>```

