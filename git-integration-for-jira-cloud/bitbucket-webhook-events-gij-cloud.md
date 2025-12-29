---
title: Bitbucket webhook events
description: Reference documentation for Bitbucket webhook event types supported by Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This page documents the Bitbucket webhook event types that Git Integration for Jira Cloud supports.

## Repository Push Events

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

## Pull Request Created Events

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

## Commit Comment Created Events

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

## Related Webhook Events

- [GitHub webhook events](/git-integration-for-jira-cloud/github-webhook-events-gij-cloud)
- [GitLab webhook events](/git-integration-for-jira-cloud/gitlab-webhook-events-gij-cloud)
- [AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events-gij-cloud)
- [Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events-gij-cloud)

<kbd>Last updated: December 2025</kbd>
