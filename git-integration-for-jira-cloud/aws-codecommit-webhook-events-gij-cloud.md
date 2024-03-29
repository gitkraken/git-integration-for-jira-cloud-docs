---

title: AWS CodeCommit webhook events
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        In the CodeCommit webhook, the <code>message</code> field is parsed.
    </div>
    </div>
</div>


The following are the supported types of AWS CodeCommit events for triggering webhooks:

### AWS CodeCommit (Notifications Event)
_Type_<br>**pushEvents:** `"^Notifications$"`

_Request URL_<br>
`/api/1/webhook/reindex/install/<secret-key>/repo/<repo-uid>/web`

_Request headers_<br>
**Content-Type:** `text/plain; charset=UTF-8`<br>
**x-amz-sns-message-id:** \--<br>
**x-amz-sns-message-type:** `Notification`<br>
**x-amz-sns-subscription-arn:** \--<br>
**x-amz-sns-topic-arn:** \--

_Request payload example_

```json
{
    "SignatureVersion": "1",
    "Type": "Notification",
    "TopicArn": "arn:aws:sns:us-east-1:552887875838:git-for-jira-cloud-webhook-6bsuxx79skn7n8kfpgse5qb58-entd68eq86k9frrp2rxg6xkcpppek5h4",
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
            \"eventId\":\"e6317415-5a45-41a8-8234-fa90742d2c66\",    \"eventName\":\"ReferenceChanges\",\"eventPartNumber\":1,
            \"eventSource\":\"aws:codecommit\",
            \"eventSourceARN\":\"arn:aws:codecommit:us-east-1:552887875838:acme_test\",
            \"eventTime\":\"2020-06-03T08:28:16.625+0000\",
            \"eventTotalParts\":1,
            \"eventTriggerConfigId\":\"b5b69ba9-8d48-436f-97d2-e5609d4039c8\",
            \"eventTriggerName\":\"git-for-jira-cloud-webhook-6bsuxx79skn7n8kfpgse5qb58-entd68eq86k9frrp2rxg6xkcpppek5h4\",
            \"eventVersion\":\"1.0\",            \"userIdentityARN\":\"arn:aws:iam::552887875838:user/johnsmith\"
        }]
    }",
    "Timestamp": "2020-06-03T08:28:16.882Z",    
    "SigningCertURL": "https://sns.us-east-1.amazonaws.com/SimpleNotificationService-hnhffstgav9qvvskm2py3c4b43e6dczm.pem",    
    "Subject": "UPDATE: AWS CodeCommit us-east-1 push: acme_test",
    "MessageId": "3179bd00-3741-583a-a6a7-ea5156211a57"
}
```

&nbsp;

### Other webhook type events

[GitHub webhook events](/git-integration-for-jira-cloud/gitHub-webhook-events)

[GitLab webhook events](/git-integration-for-jira-cloud/gitlab-webhook-events)

[Microsoft webhook events](/git-integration-for-jira-cloud/microsoft-webhook-events)

[Bitbucket webhook events](/git-integration-for-jira-cloud/aws-codecommit-webhook-events)

