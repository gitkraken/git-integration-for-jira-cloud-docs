---

title: GitLab webhook events
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

The following are the supported types of GitLab events for triggering webhooks:

|     |
| --- |
| ### GitLab (Push Events) |
| _Type_  <br>**pushEvents:** `"^push$"` |
| _Request URI_  <br>/api/1/webhook/reindex/install/**<secret\_key>**/web |
| _Request headers_  <br>**Content-type:** `application/json`  <br>**X-GitHub-Event:** `push hook` |
| _Request payload example_<br><br>```java<br>{<br>  "object_kind": "push",<br>  "project_id": 15,<br>  ...<br>  "repository":{<br>    "name": "test1",<br>    "url": "git@example.com:acme/test1.git",<br>    "description": "",<br>    "homepage": "http://example.com/acme/test1",<br>    "git_http_url":"http://example.com/acme/test1.git",<br>    "git_ssh_url":"git@example.com:acme/test1.git",<br>  },<br>  ...<br>  "total_commits_count": 4<br>}<br>``` |

|     |
| --- |
| ### GitLab (Merge Request Events) |
| _Type_  <br>`"^merge_request$"` |
| _Request URI_  <br>/api/1/webhook/reindex/install/**<secret\_key>**/web |
| _Request headers_  <br>**Content-type:** `application/json`  <br>**X-GitHub-Event:** `merge request hook` |
| _Request payload example_<br><br>```java<br>{<br>  "event_type": "merge_request",<br>  ...  <br>  "project": {<br>    "description": "",<br>    "git_http_url": "https://gitlab.com/johnsmith/test1.git",<br>    "git_ssh_url": "git@gitlab.com:johnsmith/test1.git",<br>    "url": "git@gitlab.com:ntalalova/test1.git",<br>    "http_url": "https://gitlab.com/johnsmith/test1.git",<br>    "name": "test1",<br>    "default_branch": "master",<br>    "id": 16244007,<br>    "homepage": "https://gitlab.com/johnsmith/test1"<br>  },<br>  "repository": {<br>    "name": "test1",<br>    "description": "",<br>    "url": "git@gitlab.com:johnsmith/test1.git",<br>    "homepage": "https://gitlab.com/johnsmith/test1"<br>  },<br>  ... <br>  "object_kind": "merge_request",<br>  "labels": []<br>}<br>``` |

|     |
| --- |
| ### GitLab (Repository Project Create Events) |
| _Type_  <br>**repositoryEvents:** `"^project_create$"` |
| _Request URI_  <br>/api/1/webhook/reindex/install/**<secret\_key>**/web |
| _Request headers_  <br>**Content-type:** `application/json`  <br>**X-GitHub-Event:** `system hook` |
| _Request payload example_<br><br>```java<br>{<br>  "owner_email": "admin@example.com",<br>  "path": "jsmith_4",<br>  "owner_name": "Administrator",<br>  "project_id": 85,<br>  "path_with_namespace": "root/jsmith_4",<br>  "name": "JohnSmith_4",<br>  "project_visibility": "private",<br>  "event_name": "project_create",<br>}<br>``` |

|     |
| --- |
| ### GitLab (Repository Project Update Events) |
| _Type_  <br>**repositoryEvents:** `"^project_update$"` |
| _Request URI_  <br>/api/1/webhook/reindex/install/**<secret\_key>**/web |
| _Request headers_  <br>**Content-type:** `application/json`  <br>**X-GitHub-Event:** `system hook` |
| _Request payload example_<br><br>```java<br>{<br>  "owner_email": "admin@example.com",<br>  "path": "jsmith_4",<br>  "owner_name": "Administrator",<br>  "project_id": 85,<br>  "path_with_namespace": "root/jsmith_4",<br>  "name": "JohnSmith_5",<br>  "project_visibility": "private",<br>  "event_name": "project_update",<br>}<br>``` |

|     |
| --- |
| ### GitLab (Repository Project Destroy Events) |
| _Type_  <br>**repositoryEvents:** `"^project_destroy$"` |
| _Request URI_  <br>/api/1/webhook/reindex/install/**<secret\_key>**/web |
| _Request headers_  <br>**Content-type:** `application/json`  <br>**X-GitHub-Event:** `system hook` |
| _Request payload example_<br><br>```java<br>{<br>  "owner_email": "admin@example.com",<br>  "path": "jsmith_4",<br>  "owner_name": "Administrator",<br>  "project_id": 85,<br>  "path_with_namespace": "root/jsmith_4",<br>  "name": "JohnSmith_5",<br>  "project_visibility": "private",<br>  "event_name": "project_destroy",<br>}<br>``` |

### Other webhook type events

*   Page:

    [GitHub webhook events](/wiki/spaces/GITCLOUD/pages/1921482779/GitHub+webhook+events) (Git Integration for Jira Cloud)

*   Page:

    [GitLab webhook events](/wiki/spaces/GITCLOUD/pages/1922465801/GitLab+webhook+events) (Git Integration for Jira Cloud)

*   Page:

    [Microsoft webhook events](/wiki/spaces/GITCLOUD/pages/1921876015/Microsoft+webhook+events) (Git Integration for Jira Cloud)

*   Page:

    [AWS CodeCommit webhook events](/wiki/spaces/GITCLOUD/pages/1922203671/AWS+CodeCommit+webhook+events) (Git Integration for Jira Cloud)

*   Page:

    [Bitbucket webhook events](/wiki/spaces/GITCLOUD/pages/1921548328/Bitbucket+webhook+events) (Git Integration for Jira Cloud)