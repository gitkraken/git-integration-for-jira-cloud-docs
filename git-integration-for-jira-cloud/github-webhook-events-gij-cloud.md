---
title: "GitHub webhook events"
description: "Reference documentation for GitHub webhook event types supported by Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "GitHub webhook events"
content_type: "reference"
audience: "developer"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["GitHub"]
role_required: "User"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "reference", "developer", "GitHub"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

This page documents the GitHub webhook event types that Git Integration for Jira Cloud supports.

| GitHub event type | Use when | Key header | Typical Jira impact |
| :--- | :--- | :--- | :--- |
| Push | You need commit and branch indexing after repository updates | `X-GitHub-Event: push` | Reindexes commit-related activity |
| Pull request | You need pull request indexing updates | `X-GitHub-Event: pull_request` | Reindexes pull request-related activity |
| Repository | You need repository-level change notifications | `X-GitHub-Event: repository` | Updates repository-level indexing behavior when supported |

## When to use the GitHub push event

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

## When to use the GitHub pull request event

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

## When to use the GitHub repository event

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

## Related webhook event references

- [GitLab webhook events](/git-integration-for-jira-cloud/gitLab-webhook-events-gij-cloud)
- [Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events-gij-cloud)
- [AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events-gij-cloud)
- [Bitbucket webhook events](/git-integration-for-jira-cloud/bitbucket-webhook-events-gij-cloud)

