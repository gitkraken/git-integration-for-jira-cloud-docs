---

title: Bitbucket webhook events
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
**GIT INTEGRATION: JIRA CLOUD**

The following are the supported types of Bitbucket events for triggering webhooks:

## Bitbucket (Repository Push Events)

_Type_<br>
**pushEvents:** `"^repo:push$"`

_Request URI_<br>
`/api/1/webhook/reindex/install/`**\<secret\_key\>**`/web`

_Request headers_<br>
**Content-Type:** `application/json`<br>
**X-Event-Key:** `repo:push`

_Request payload example_<br>
```json
{  
  "repository": {
    "full_name": "johnsmith/test-bitbucket",
    "name": "Test Bitbucket",
    "links": {
      "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket"},
    },
    "scm": "git",
    "type": "repository",
  },
}
```

## Bitbucket (Pullrequest Created Events)

_Type_<br>
`"^pullrequest:.*$"`

_Request URI_<br>
`/api/1/webhook/reindex/install/`**\<secret\_key\>**`/web`

_Request headers_<br>
**Content-Type:** `application/json`<br>
**X-Event-Key:** `pullrequest:created`

_Request payload example_<br>
```json
{
  "pullrequest": {
    "destination": {
      "repository": {
        "full_name": "johnsmith/test-bitbucket",
        "name": "Test Bitbucket",
        "links": {
          "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket"}
        },
      },
      "branch": {"name": "P5-1-second-issue-for-progect5"}
    },
    "source": {
      "repository": {
        "links": {
          "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket"},                  },
        },
      },
      "branch": {"name": "master"}
    },
    "type": "pullrequest",
    "title": "TES-1 Master",     
    "close_source_branch": false,
    "state": "OPEN"    
  },  
}
```

## Bitbucket (Repository Commit Comment Created Events)

_Type_<br>
`"^repo:commit_comment_created$"`

_Request URI_<br>
`/api/1/webhook/reindex/install/`**\<secret\_key\>**`/web`

_Request headers_<br>
**Content-type:** `application/json`<br>
**X-Event-Key:** `repo:commit_comment_created`

_Request payload example_<br>
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
      "html": "<p>This is a comment<\/p>",
      "type": "rendered"
    },  
  },
}
```

## Other webhook type events

[GitHub webhook events](/git-integration-for-jira-cloud/gitHub-webhook-events)

[GitLab webhook events](/git-integration-for-jira-cloud/gitlab-webhook-events)

[AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events)

[Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events)

