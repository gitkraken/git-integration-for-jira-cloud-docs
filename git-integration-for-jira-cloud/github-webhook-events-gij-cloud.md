---

title: GitHub webhook events

description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The following are the supported types of GitHub events for triggering webhooks:

## GitHub (Push Events)

_Type_<br>
**pushEvents:** `"^push$"`

_Request URI_<br>
`/api/1/webhook/reindex/install/`**\<secret\_key\>**`/web`

_Request headers_<br>
**Content-type:** `application/x-www-form-urlencoded`<br>
**X-GitHub-Event:** `push`

_Request payload example_<br>
```json
*{
  ...
  "repository": {
    "id": 224819315,
    "git_url": "git://github.com/acme/test1.git",
    "ssh_url": "git@github.com:acme/test1.git",
    "clone_url": "https://github.com/acme/test1.git",
    "svn_url": "https://github.com/acme/test1",
  },
  ...
}
```

## GitHub (Pull Request Events)

_Type_<br>
**pullRequestEvents:** `"^pull_request$"`

_Request URI_<br>
`/api/1/webhook/reindex/install/`**\<secret\_key\>**`/web`

_Request headers_<br>
**Content-type:** `application/x-www-form-urlencoded`  <br>
**X-GitHub-Event:** `pull_request`

_Request payload_<br>
```json
*{
  ...
  "repository": {
    "id": 224819315,
    "git_url": "git://github.com/acme/test1.git",
    "ssh_url": "git@github.com:acme/test1.git",
    "clone_url": "https://github.com/acme/test1.git",
    "svn_url": "https://github.com/acme/test1",
  },
  ...
}
```

## GitHub (Repository Events)

_Type_<br>
**repositoryEvents:** "^repository$"

_Request URI_<br>
`/api/1/webhook/reindex/install/`**\<secret\_key\>**`/web`

_Request headers_<br>
**Content-Type:** `application/x-www-form-urlencoded`  <br>
**X-GitHub-Event:** `repository`

_Request payload_<br>
```json
*{
  ...
  "repository": {
    "id": 224819315,
    "git_url": "git://github.com/acme/test1.git",
    "ssh_url": "git@github.com:acme/test1.git",
    "clone_url": "https://github.com/acme/test1.git",
    "svn_url": "https://github.com/acme/test1",
  },
  ...
}
```

## Other webhook type events

[GitLab webhook events](/git-integration-for-jira-cloud/gitLab-webhook-events)

[Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events)

[AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events)

[Bitbucket webhook events](/git-integration-for-jira-cloud/bitbucket-webhook-events)

