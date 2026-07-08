---
title: "Gerrit webhook indexing integration"
description: "Configure webhook indexing integration for Gerrit to work with Git Integration for Jira Cloud behind firewalls."
product: "Git Integration for Jira Cloud"
feature: "Gerrit webhook indexing integration"
content_type: "reference"
audience: "all"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["Gerrit"]
role_required: "all"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "reference", "Gerrit"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
    Webhooks are not built into Gerrit by default. You must install and configure the Gerrit webhook plugin before using webhooks with Git Integration for Jira Cloud.        
    </div>
    </div>
</div>

**On this page:**
- [Install the webhook plugin](#install-the-webhook-plugin)
- [Configure webhooks](#configure-webhooks)
- [Trigger webhooks manually](#trigger-webhooks-manually)

&nbsp;
* * *
&nbsp;

## Install the Webhook Plugin

Install Gerrit with the webhook plugin from [https://gerrit.googlesource.com/plugins/webhooks/](https://gerrit.googlesource.com/plugins/webhooks/).

&nbsp;

## Configure Webhooks

### List Projects (Repositories)

```powershell
curl http(s)://your.org.com:8080/projects/?d
```

### Check Enabled Webhooks

```powershell
curl http(s)://your.org.com:8080/config/server/webhooks~projects/MyTestRepo/remotes
```

### Add a Webhook

```powershell
curl --user username:password -H 'Content-Type: application/json' -X PUT -d @webhook.json http(s)://your.org.com:8080/a/config/server/webhooks~projects/MyTestRepo/remotes/bbb-webhook
```

Create a `webhook.json` file:

```json
{
   "url" : "https://example.com/webhook/url",
   "maxTries" : 3,
   "sslVerify": true
}
```

Replace `https://example.com/webhook/url` with your webhook URL from Git Integration for Jira Manage Integration page ➜ **Gerrit Webhook Indexing Integration** ➜ &#9881; ➜ Edit Integration ➜ 'Webhook URL'.

&nbsp;


&nbsp;

## Related Articles

- [GitHub webhook indexing integration](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud)
- [GitLab webhook indexing integration](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud)
- [Microsoft webhook indexing integration](/git-integration-for-jira-cloud/microsoft-webhook-indexing-integration-gij-cloud)
