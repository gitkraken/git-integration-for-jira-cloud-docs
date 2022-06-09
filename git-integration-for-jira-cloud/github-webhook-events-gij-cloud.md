---

title: GitHub webhook events

description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The following are the supported types of GitHub events for triggering webhooks:

|     |
| --- |
| ### GitHub (Push Events) |
| _Type_  <br>**pushEvents:** `"^push$"` |
| _Request URI_  <br>`/api/1/webhook/reindex/install/`**<secret\_key>**`/web` |
| _Request headers_  <br>**Content-type:** `application/x-www-form-urlencoded`  <br>**X-GitHub-Event:** `push` |
| _Request payload example_<br><br>```java<br>*{<br>  ...<br>  "repository": {<br>    "id": 224819315,<br>    "git_url": "git://github.com/acme/test1.git",<br>    "ssh_url": "git@github.com:acme/test1.git",<br>    "clone_url": "https://github.com/acme/test1.git",<br>    "svn_url": "https://github.com/acme/test1",<br>  },<br>  ...<br>}<br>``` |

|     |
| --- |
| ### GitHub (Pull Request Events) |
| _Type_  <br>**pullRequestEvents:** `"^pull_request$"` |
| _Request URI_  <br>`/api/1/webhook/reindex/install/`**<secret\_key>**`/web` |
| _Request headers_  <br>**Content-type:** `application/x-www-form-urlencoded`  <br>**X-GitHub-Event:** `pull_request` |
| _Request payload_<br><br>```java<br>*{<br>  ...<br>  "repository": {<br>    "id": 224819315,<br>    "git_url": "git://github.com/acme/test1.git",<br>    "ssh_url": "git@github.com:acme/test1.git",<br>    "clone_url": "https://github.com/acme/test1.git",<br>    "svn_url": "https://github.com/acme/test1",<br>  },<br>  ...<br>}<br>``` |

|     |
| --- |
| ### GitHub (Repository Events) |
| Type  <br>**repositoryEvents:** "^repository$" |
| _Request URI_  <br>`/api/1/webhook/reindex/install/`**<secret\_key>**`/web` |
| _Request headers_  <br>**Content-Type:** `application/x-www-form-urlencoded`  <br>**X-GitHub-Event:** `repository` |
| _Request payload_<br><br>```java<br>*{<br>  ...<br>  "repository": {<br>    "id": 224819315,<br>    "git_url": "git://github.com/acme/test1.git",<br>    "ssh_url": "git@github.com:acme/test1.git",<br>    "clone_url": "https://github.com/acme/test1.git",<br>    "svn_url": "https://github.com/acme/test1",<br>  },<br>  ...<br>}<br>``` |

