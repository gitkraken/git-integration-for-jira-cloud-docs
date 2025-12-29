---
title: GitLab webhook events
description: Reference documentation for GitLab webhook event types supported by Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This page documents the GitLab webhook event types that Git Integration for Jira Cloud supports.

## Push Events

| Property | Value |
|----------|-------|
| Type | `"^push$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |
| X-GitLab-Event | `Push Hook` |

**Payload example:**

```json
{
  "object_kind": "push",
  "project_id": 15,
  "repository": {
    "name": "test1",
    "url": "git@example.com:acme/test1.git",
    "description": "",
    "homepage": "http://example.com/acme/test1",
    "git_http_url": "http://example.com/acme/test1.git",
    "git_ssh_url": "git@example.com:acme/test1.git"
  },
  "total_commits_count": 4
}
```

## Merge Request Events

| Property | Value |
|----------|-------|
| Type | `"^merge_request$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |
| X-GitLab-Event | `Merge Request Hook` |

**Payload example:**

```json
{
  "event_type": "merge_request",
  "object_kind": "merge_request",
  "project": {
    "description": "",
    "git_http_url": "https://gitlab.com/johnsmith/test1.git",
    "git_ssh_url": "git@gitlab.com:johnsmith/test1.git",
    "url": "git@gitlab.com:johnsmith/test1.git",
    "http_url": "https://gitlab.com/johnsmith/test1.git",
    "name": "test1",
    "default_branch": "master",
    "id": 16244007,
    "homepage": "https://gitlab.com/johnsmith/test1"
  },
  "repository": {
    "name": "test1",
    "description": "",
    "url": "git@gitlab.com:johnsmith/test1.git",
    "homepage": "https://gitlab.com/johnsmith/test1"
  }
}
```

## Project Create Events

| Property | Value |
|----------|-------|
| Type | `"^project_create$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |
| X-GitLab-Event | `System Hook` |

**Payload example:**

```json
{
  "owner_email": "admin@example.com",
  "path": "jsmith_4",
  "owner_name": "Administrator",
  "project_id": 85,
  "path_with_namespace": "root/jsmith_4",
  "name": "JohnSmith_4",
  "project_visibility": "private",
  "event_name": "project_create"
}
```

## Project Update Events

| Property | Value |
|----------|-------|
| Type | `"^project_update$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |
| X-GitLab-Event | `System Hook` |

**Payload example:**

```json
{
  "owner_email": "admin@example.com",
  "path": "jsmith_4",
  "owner_name": "Administrator",
  "project_id": 85,
  "path_with_namespace": "root/jsmith_4",
  "name": "JohnSmith_5",
  "project_visibility": "private",
  "event_name": "project_update"
}
```

## Project Destroy Events

| Property | Value |
|----------|-------|
| Type | `"^project_destroy$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |
| X-GitLab-Event | `System Hook` |

**Payload example:**

```json
{
  "owner_email": "admin@example.com",
  "path": "jsmith_4",
  "owner_name": "Administrator",
  "project_id": 85,
  "path_with_namespace": "root/jsmith_4",
  "name": "JohnSmith_5",
  "project_visibility": "private",
  "event_name": "project_destroy"
}
```

&nbsp;

## Related Webhook Events

- [GitHub webhook events](/git-integration-for-jira-cloud/github-webhook-events-gij-cloud)
- [Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events-gij-cloud)
- [AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events-gij-cloud)
- [Bitbucket webhook events](/git-integration-for-jira-cloud/bitbucket-webhook-events-gij-cloud)

<kbd>Last updated: December 2025</kbd>
