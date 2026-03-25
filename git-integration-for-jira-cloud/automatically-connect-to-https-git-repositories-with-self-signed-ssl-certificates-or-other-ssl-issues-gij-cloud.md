---
title: "Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues"
description: "How to set up integrations with self-signed SSL certificates using automatic connection"
product: "Git Integration for Jira Cloud"
feature: "Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues"
content_type: "security"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "deprecated"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "security", "admin", "deprecated"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

<b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>GITHUB ENTERPRISE</b> <b style='background-color:#FFE3B2; padding:1px 5px; color:#A35F00; border-radius:3px; margin: 0 5px; font-size: small;'>GITLAB CE/EE</b>

Perform full feature integration with HTTPS git repositories that have self-signed SSL certificates or other SSL issues.

For this guide, we use GitLab Server as an example:

1.  On your Jira dashboard, go to menu Apps ➜ **Git Integration: Manage Git repositories**. The following page appears.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-integrations-page-2025.png)

2.  On the Git host service selection screen, click **GitLab server**, then click **GitLab Server (CE/EE) APIv4** to select this integration type.

    ![](/wp-content/uploads/gij-gitcloud-add-integration-type-gitlab-server-sel-2025.png)

    *   Enter the **Host URL** of the private git server.
    *   Enter **Personal access token** for this server (APIv4). _Support for APIv3 is deprecated._

3.  Click **Connect and select repositories**.

4.  If there is an indication of an SSL error, the following screen appears.

    ![](/wp-content/uploads/gij-gitserver-gitlab-server-bad-ssl-example-c.png)

5.  Click **Ignore certificate errors and continue connection**. This ignores SSL verification if the certificate is self-signed or expired.

6.  Select repositories or import all of them, then click **Connect repositories** to complete the setup.

This integration appears in the Manage integrations list. Go to ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit integration** to make changes to the repository settings.

&nbsp;
* * *

[**Prev:** Self-signed HTTPS connections (index)](/git-integration-for-jira-cloud/self-signed-https-integration-gij-cloud)

[**Next:** Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/git-integration-for-jira-cloud/manually-connect-to-https-git-repositories-with-self-signed-ssl-certificates-or-other-ssl-issues-gij-cloud)

<p>&nbsp;</p>
