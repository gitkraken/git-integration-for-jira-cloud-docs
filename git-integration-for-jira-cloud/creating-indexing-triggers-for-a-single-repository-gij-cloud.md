---

title: Creating indexing triggers for a single repository
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Create an indexing trigger that can be initiated for any **individual** repository. It can be used with continuous integration service.

_**Required headers:**_

*   'x-bbb-webhook-type': `push`

*   'Content-Type': `application/json`


_**Optional headers:**_

*   'x-bbb-webhook-id' -- Can be any string representing the _id_ of the request to be used.


|     |
| --- |
| **Usage examples:** |
| ```java<br>curl -H 'x-bbb-webhook-type: push' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url<br>``` |
| ```java<br>curl -H 'x-bbb-webhook-type: push' -H 'x-bbb-webhook-id: id-string' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url<br>``` |

|     |
| --- |
| **Payload.json** |
| ```java<br>{<br>  "origin": "repository-origin"<br>}<br>``` |

