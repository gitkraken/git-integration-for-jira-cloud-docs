---
title: AWS CodeCommit webhook events
description: Reference documentation for AWS CodeCommit webhook event types supported by Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This page documents the AWS CodeCommit webhook event types that Git Integration for Jira Cloud supports.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        AWS CodeCommit webhooks use SNS (Simple Notification Service). The <code>Message</code> field in the SNS notification contains the CodeCommit event data.
    </div>
    </div>
</div>

## Notifications Event

| Property | Value |
|----------|-------|
| Type | `"^Notifications$"` |
| Request URI | `/api/1/webhook/reindex/install/<secret_key>/repo/<repo_uid>/web` |
| Content-Type | `text/plain; charset=UTF-8` |
| x-amz-sns-message-type | `Notification` |

**Payload example:**

```json
{
    "SignatureVersion": "1",
    "Type": "Notification",
    "TopicArn": "arn:aws:sns:us-east-1:552887875838:git-for-jira-cloud-webhook",
    "Message": "{
        \"Records\":[{
            \"awsRegion\":\"us-east-1\",
            \"codecommit\":{
                \"references\":[{
                    \"commit\":\"5f6a956f2560836bb085a5d1bfdde4a0f9bc12a5\",
                    \"ref\":\"refs/heads/master\"
                }]
            },
            \"customData\":null,
            \"eventId\":\"e6317415-5a45-41a8-8234-fa90742d2c66\",
            \"eventName\":\"ReferenceChanges\",
            \"eventSource\":\"aws:codecommit\",
            \"eventSourceARN\":\"arn:aws:codecommit:us-east-1:552887875838:acme_test\",
            \"eventTime\":\"2020-06-03T08:28:16.625+0000\"
        }]
    }",
    "Timestamp": "2020-06-03T08:28:16.882Z",
    "Subject": "UPDATE: AWS CodeCommit us-east-1 push: acme_test",
    "MessageId": "3179bd00-3741-583a-a6a7-ea5156211a57"
}
```

&nbsp;

## Related Webhook Events

- [GitHub webhook events](/git-integration-for-jira-cloud/github-webhook-events-gij-cloud)
- [GitLab webhook events](/git-integration-for-jira-cloud/gitlab-webhook-events-gij-cloud)
- [Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events-gij-cloud)
- [Bitbucket webhook events](/git-integration-for-jira-cloud/bitbucket-webhook-events-gij-cloud)

<kbd>Last updated: December 2025</kbd>
