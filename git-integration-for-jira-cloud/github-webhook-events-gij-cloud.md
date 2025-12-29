---
title: GitHub webhook events
description: Reference documentation for GitHub webhook event types supported by Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This page documents the GitHub webhook event types that Git Integration for Jira Cloud supports.

## Push Events

| Property | Value |
|----------|-------|
| Type | `"^push$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/x-www-form-urlencoded` |
| X-GitHub-Event | `push` |

**Payload example:**

```json
{
  "repository": {
    "id": 224819315,
    "git_url": "git://github.com/acme/test1.git",
    "ssh_url": "git@github.com:acme/test1.git",
    "clone_url": "https://github.com/acme/test1.git",
    "svn_url": "https://github.com/acme/test1"
  }
}
```

## Pull Request Events

| Property | Value |
|----------|-------|
| Type | `"^pull_request$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/x-www-form-urlencoded` |
| X-GitHub-Event | `pull_request` |

**Payload example:**

```json
{
  "repository": {
    "id": 224819315,
    "git_url": "git://github.com/acme/test1.git",
    "ssh_url": "git@github.com:acme/test1.git",
    "clone_url": "https://github.com/acme/test1.git",
    "svn_url": "https://github.com/acme/test1"
  }
}
```

## Repository Events

| Property | Value |
|----------|-------|
| Type | `"^repository$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/x-www-form-urlencoded` |
| X-GitHub-Event | `repository` |

**Payload example:**

```json
{
  "repository": {
    "id": 224819315,
    "git_url": "git://github.com/acme/test1.git",
    "ssh_url": "git@github.com:acme/test1.git",
    "clone_url": "https://github.com/acme/test1.git",
    "svn_url": "https://github.com/acme/test1"
  }
}
```

&nbsp;

## Related Webhook Events

- [GitLab webhook events](/git-integration-for-jira-cloud/gitLab-webhook-events-gij-cloud)
- [Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events-gij-cloud)
- [AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events-gij-cloud)
- [Bitbucket webhook events](/git-integration-for-jira-cloud/bitbucket-webhook-events-gij-cloud)

<kbd>Last updated: December 2025</kbd>
