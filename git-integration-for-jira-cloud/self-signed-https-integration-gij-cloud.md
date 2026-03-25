---
title: "Self-signed HTTPS integration"
description: "How to integrate repositories using self-signed HTTPS certificates"
product: "Git Integration for Jira Cloud"
feature: "Self-signed HTTPS integration"
content_type: "security"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "security", "admin"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Self-signed certificates are common in HTTPS Git repositories that are hosted privately. Even for an administrator, setting the HTTP `sslVerify` option to connect to this repository can be challenging.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Jira administrators can now disable <code>sslVerify</code> for specific repositories from within Jira.
    </div>
    </div>
</div>

This feature is available in the **Connect to Git Repository** wizard and the **Full feature integration** panel for GitHub and GitLab.

Continue to the next topic for further information on setup and integration.

&nbsp;
* * *

[**Prev:** Using the Connect repository wizard](/git-integration-for-jira-cloud/using-the-single-git-integration-wizard-gij-cloud)

[**Next:** Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/git-integration-for-jira-cloud/automatically-connect-to-https-git-repositories-with-self-signed-ssl-certificates-or-other-ssl-issues-gij-cloud)

<p>&nbsp;</p>
