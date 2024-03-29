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

*   `x-bbb-webhook-id` -- Can be any string representing the _id_ of the request to be used.

<br>

**Usage examples:**

```powershell
curl -H 'x-bbb-webhook-type: push' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url
```

```powershell
curl -H 'x-bbb-webhook-type: push' -H 'x-bbb-webhook-id: id-string' -H 'content-type: application/json' -X POST -d @payload.json https://webhook/url
```

**Payload.json**

```json
{
    "origin": "repository-origin"
}
```

