---

title: Bitbucket webhook events
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
GIT INTEGRATION: JIRA CLOUD

The following are the supported types of Bitbucket events for triggering webhooks:

|     |
| --- |
| ### Bitbucket (Repository Push Events) |
| _Type_  <br>**pushEvents:** `"^repo:push$"` |
| _Request URI_  <br>`/api/1/webhook/reindex/install/`**<secret\_key>**`/web` |
| _Request headers_  <br>**Content-Type:** `application/json`  <br>**X-Event-Key:** `repo:push` |
| _Request payload example_<br><br>```java<br>{  <br>  "repository": {<br>    "full_name": "johnsmith/test-bitbucket",<br>    "name": "Test Bitbucket",<br>    "links": {<br>      "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket"},<br>    },<br>    "scm": "git",<br>    "type": "repository",<br>  },<br>}<br>``` |

|     |
| --- |
| ### Bitbucket (Pullrequest Created Events) |
| _Type_  <br>`"^pullrequest:.*$"` |
| _Request URI_  <br>`/api/1/webhook/reindex/install/`**<secret\_key>**`/web` |
| _Request headers_  <br>**Content-Type:** `application/json`  <br>**X-Event-Key:** `pullrequest:created` |
| _Request payload example_<br><br>```java<br>{<br>  "pullrequest": {<br>    "destination": {<br>      "repository": {<br>        "full_name": "johnsmith/test-bitbucket",<br>        "name": "Test Bitbucket",<br>        "links": {<br>          "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket"}<br>        },<br>      },<br>      "branch": {"name": "P5-1-second-issue-for-progect5"}<br>    },<br>    "source": {<br>      "repository": {<br>        "links": {<br>          "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket"},                  },<br>        },<br>      },<br>      "branch": {"name": "master"}<br>    },<br>    "type": "pullrequest",<br>    "title": "TES-1 Master",     <br>    "close_source_branch": false,<br>    "state": "OPEN"    <br>  },  <br>}<br>``` |

|     |
| --- |
| ### Bitbucket (Repository Commit Comment Created Events) |
| _Type_  <br>`"^repo:commit_comment_created$"` |
| _Request URI_  <br>`/api/1/webhook/reindex/install/`**<secret\_key>**`/web` |
| _Request headers_  <br>**Content-type:** `application/json`  <br>**X-Event-Key:** `repo:commit_comment_created` |
| _Request payload example_<br><br>```java<br>{<br>  "comment": {<br>    "commit": {<br>      "links": {<br>        "html": {"href": "https://bitbucket.org/johnsmith/test-bitbucket/commits/6d32f7643bfffdea17e8c498454971508fbdd5b1"}<br>      },<br>      "hash": "6d32f7643bfffdea17e8c498454971508fbdd5b1"<br>    },<br>    "id": 8917242,<br>    "type": "commit_comment",    <br>    "content": {<br>      "markup": "markdown",<br>      "raw": "Comment",<br>      "html": "<p>This is a comment<\/p>",<br>      "type": "rendered"<br>    },  <br>  },<br>}<br>``` |

