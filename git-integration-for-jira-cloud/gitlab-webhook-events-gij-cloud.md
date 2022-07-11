---

title: GitLab webhook events
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

The following are the supported types of GitLab events for triggering webhooks:

## GitLab (Push Events)

_Type_<br>
**pushEvents:** `"^push$"`

_Request URI_<br>
/api/1/webhook/reindex/install/**<secret\_key>**/web

_Request headers_<br>
**Content-type:** `application/json`<br>
**X-GitHub-Event:** `push hook`

_Request payload example_<br>
```json
{
  "object_kind": "push",
  "project_id": 15,
  ...
  "repository":{
    "name": "test1",
    "url": "git@example.com:acme/test1.git",
    "description": "",
    "homepage": "http://example.com/acme/test1",
    "git_http_url":"http://example.com/acme/test1.git",
    "git_ssh_url":"git@example.com:acme/test1.git",
  },
  ...
  "total_commits_count": 4
}
```

## GitLab (Merge Request Events)

_Type_<br>
`"^merge_request$"`

_Request URI_<br>
/api/1/webhook/reindex/install/**\<secret\_key\>**/web

_Request headers_<br>
**Content-type:** `application/json`<br>
**X-GitHub-Event:** `merge request hook`

_Request payload example_<br>
```json
{
  "event_type": "merge_request",
  ...  
  "project": {
    "description": "",
    "git_http_url": "https://gitlab.com/johnsmith/test1.git",
    "git_ssh_url": "git@gitlab.com:johnsmith/test1.git",
    "url": "git@gitlab.com:ntalalova/test1.git",
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
  },
  ... 
  "object_kind": "merge_request",
  "labels": []
}
```

## GitLab (Repository Project Create Events)

_Type_<br>
**repositoryEvents:** `"^project_create$"`

_Request URI_<br>
/api/1/webhook/reindex/install/**\<secret\_key\>**/web

_Request headers_<br>
**Content-type:** `application/json`<br>
**X-GitHub-Event:** `system hook`

_Request payload example_<br>
```json
{
  "owner_email": "admin@example.com",
  "path": "jsmith_4",
  "owner_name": "Administrator",
  "project_id": 85,
  "path_with_namespace": "root/jsmith_4",
  "name": "JohnSmith_4",
  "project_visibility": "private",
  "event_name": "project_create",
}
```

 ## GitLab (Repository Project Update Events)

_Type_<br>
**repositoryEvents:** `"^project_update$"`

_Request URI_<br>
/api/1/webhook/reindex/install/**\<secret\_key\>**/web

_Request headers_<br>
**Content-type:** `application/json`<br>
**X-GitHub-Event:** `system hook`

_Request payload example_<br>
```json
{
  "owner_email": "admin@example.com",
  "path": "jsmith_4",
  "owner_name": "Administrator",
  "project_id": 85,
  "path_with_namespace": "root/jsmith_4",
  "name": "JohnSmith_5",
  "project_visibility": "private",
  "event_name": "project_update",
}
```

## GitLab (Repository Project Destroy Events)

_Type_<br>
**repositoryEvents:** `"^project_destroy$"`

_Request URI_<br>
/api/1/webhook/reindex/install/**\<secret\_key\>**/web

_Request headers_<br>
**Content-type:** `application/json`<br>
**X-GitHub-Event:** `system hook`

_Request payload example_<br>
```json
{
  "owner_email": "admin@example.com",
  "path": "jsmith_4",
  "owner_name": "Administrator",
  "project_id": 85,
  "path_with_namespace": "root/jsmith_4",
  "name": "JohnSmith_5",
  "project_visibility": "private",
  "event_name": "project_destroy",
}
```

## Other webhook type events

[GitHub webhook events](/git-integration-for-jira-cloud/github-webhook-events)

[Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events)

[AWS CodeCommit webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events)

[Bitbucket webhook events](/git-integration-for-jira-cloud/bitbucket-webhook-events)

