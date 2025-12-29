---
title: Microsoft webhook events
description: Reference documentation for Microsoft (Azure DevOps/VSTS/TFS) webhook event types supported by Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This page documents the Microsoft webhook event types that Git Integration for Jira Cloud supports.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Microsoft doesn't send a header by default. Integration type is detected from the payload.
    </div>
    </div>
</div>

## Push Events

| Property | Value |
|----------|-------|
| Type | `"^push"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |

**Payload example:**

```json
{
  "eventType": "git.push",
  "resource": {
    "repository": {
      "id": "f0234cc5-5891-4044-a45e-c1d9d4b33562",
      "name": "TestWebHook",
      "url": "https://dev.azure.com/johnsmith/_apis/git/repositories/f0234cc5-5891-4044-a45e-c1d9d4b33562",
      "project": {
        "id": "f12f9cc9-387e-43f7-9023-e871c94bfebc"
      },
      "remoteUrl": "https://dev.azure.com/johnsmith/TestWebHook/_git/WebHook"
    }
  }
}
```

## Pull Request Created Events

| Property | Value |
|----------|-------|
| Type | `"^git\.pullrequest\.created$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |

**Payload example:**

```json
{
  "publisherId": "tfs",
  "eventType": "git.pullrequest.created",
  "resource": {
    "mergeId": "61ea7c1d-06bd-4bd4-80d4-64e63e5224b6",
    "_links": {
      "web": {"href": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks/pullrequest/1"}
    },
    "repository": {
      "sshUrl": "git@ssh.dev.azure.com:v3/jsmith0806/Webhooks/Webhooks",
      "webUrl": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",
      "name": "Webhooks",
      "remoteUrl": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks"
    },
    "pullRequestId": 1,
    "title": "PROJ-4: Merge test-branch to master"
  }
}
```

## Pull Request Updated Events

| Property | Value |
|----------|-------|
| Type | `"^git\.pullrequest\.updated$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |

**Payload example:**

```json
{
  "publisherId": "tfs",
  "eventType": "git.pullrequest.updated",
  "resource": {
    "mergeId": "61ea7c1d-06bd-4bd4-80d4-64e63e5224b6",
    "_links": {
      "web": {"href": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks/pullrequest/1"}
    },
    "repository": {
      "sshUrl": "git@ssh.dev.azure.com:v3/jsmith0806/Webhooks/Webhooks",
      "webUrl": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks",
      "name": "Webhooks",
      "remoteUrl": "https://dev.azure.com/jsmith0806/Webhooks/_git/Webhooks"
    },
    "pullRequestId": 1,
    "title": "PROJ-4: Merge test-branch to master"
  }
}
```

&nbsp;

## Related Webhook Events

- [GitHub webhook events](/git-integration-for-jira-cloud/github-webhook-events-gij-cloud)
- [GitLab webhook events](/git-integration-for-jira-cloud/gitlab-webhook-events-gij-cloud)
- [AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events-gij-cloud)
- [Bitbucket webhook events](/git-integration-for-jira-cloud/bitbucket-webhook-events-gij-cloud)

<kbd>Last updated: December 2025</kbd>
