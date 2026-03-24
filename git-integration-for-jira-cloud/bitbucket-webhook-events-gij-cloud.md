---
title: "Bitbucket webhook events"
description: "Reference documentation for Bitbucket webhook event types supported by Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Bitbucket webhook events"
content_type: "reference"
audience: "developer"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["Bitbucket"]
role_required: "User"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "reference", "developer", "Bitbucket"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

This page documents the Bitbucket webhook event types that Git Integration for Jira Cloud supports.

| Bitbucket event type | Use when | Key header | Typical Jira impact |
| :--- | :--- | :--- | :--- |
| Repository push | You need commit and branch indexing after repository updates | `X-Event-Key: repo:push` | Reindexes commit-related activity |
| Pull request created | You need new pull request indexing updates | `X-Event-Key: pullrequest:created` | Reindexes newly created pull requests |
| Commit comment created | You need commit comment-related webhook handling | `X-Event-Key: repo:commit_comment_created` | Handles commit-comment activity where supported |

## When to use the Bitbucket repository push event

| Property | Value |
|----------|-------|
| Type | `"^repo:push$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |
| X-Event-Key | `repo:push` |

**Payload example:**

```json
{
  "repository": {
    "full_name": "johnsmith/test-bitbucket",
    "name": "Test Bitbucket",
    "links": {
      "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket"}
    },
    "scm": "git",
    "type": "repository"
  }
}
```

## When to use the Bitbucket pull request created event

| Property | Value |
|----------|-------|
| Type | `"^pullrequest:.*$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |
| X-Event-Key | `pullrequest:created` |

**Payload example:**

```json
{
  "pullrequest": {
    "destination": {
      "repository": {
        "full_name": "johnsmith/test-bitbucket",
        "name": "Test Bitbucket",
        "links": {
          "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket"}
        }
      },
      "branch": {"name": "P5-1-second-issue-for-progect5"}
    },
    "source": {
      "repository": {
        "links": {
          "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket"}
        }
      },
      "branch": {"name": "master"}
    },
    "type": "pullrequest",
    "title": "TES-1 Master",
    "close_source_branch": false,
    "state": "OPEN"
  }
}
```

## When to use the Bitbucket commit comment created event

| Property | Value |
|----------|-------|
| Type | `"^repo:commit_comment_created$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/web` |
| Content-Type | `application/json` |
| X-Event-Key | `repo:commit_comment_created` |

**Payload example:**

```json
{
  "comment": {
    "commit": {
      "links": {
        "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket/commits/6d32f7643bfffdea17e8c498454971508fbdd5b1"}
      },
      "hash": "6d32f7643bfffdea17e8c498454971508fbdd5b1"
    },
    "id": 8917242,
    "type": "commit_comment",
    "content": {
      "markup": "markdown",
      "raw": "Comment",
      "html": "<p>This is a comment</p>",
      "type": "rendered"
    }
  }
}
```

&nbsp;

## Related webhook event references

- [GitHub webhook events](/git-integration-for-jira-cloud/github-webhook-events-gij-cloud)
- [GitLab webhook events](/git-integration-for-jira-cloud/gitlab-webhook-events-gij-cloud)
- [AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events-gij-cloud)
- [Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events-gij-cloud)

