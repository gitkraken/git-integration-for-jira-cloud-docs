---
title: "Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues"
description: "How to manually set up git repository connections with self-signed SSL certificates"
product: "Git Integration for Jira Cloud"
feature: "Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues"
content_type: "troubleshooting"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "troubleshooting", "admin"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

<b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>GITHUB ENTERPRISE</b> <b style='background-color:#FFE3B2; padding:1px 5px; color:#A35F00; border-radius:3px; margin: 0 5px; font-size: small;'>GITLAB CE/EE</b>

Git Integration for Jira Cloud can connect to private HTTPS repositories with self-signed certificates, but certificate validation may block the initial connection. Use this workaround when automatic connection fails for GitHub Enterprise or GitLab CE/EE over HTTPS and a Jira administrator needs to finish the repository setup in Jira Cloud.

**Requirements**

- Jira Cloud with Git Integration for Jira Cloud installed
- Jira Administrator access to manage integrations
- A private HTTPS repository that uses a self-signed certificate
- Local access to the repository so you can run `git config`

## How to disable SSL verification in the local repository

When connecting to a private HTTPS git repository, a custom (self-signed) certificate may cause problems. Follow these steps to work around this issue:

1.  Configure the repository to disable verification of the SSL certificate:

    *   Run `git config http.sslVerify false` in the repository folder.

        **Example:**

        ```bash
        cd project.git
        git config http.sslVerify false
        ```

## How to add the repository in Git Integration for Jira Cloud

1.  On the Manage integrations page, click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-integrations-page-2025.png)

2.  Add the repository via **Plain Git integration** or **Quick start** on the Add integration page.

    ![](/wp-content/uploads/gij-add-new-integration-plain-git-sel-2025.png)

3.  Enter **Host URL** and login credentials on the next screen. If 2FA is enabled on this account, enter PAT as the password.

4.  Click **Add integration** and continue to completion.

    ![](/wp-content/uploads/gij-gitserver-gitlab-server-bad-ssl-example-c.png)

5.  If there's an SSL verification error, click **Ignore certificate errors and continue connection** to proceed.

## Other ways to trust the certificate

Alternative solutions exist for making Java trust this certificate. Refer to these Atlassian articles about resolving SSL verification issues:

1.  [**Unable to Connect to SSL Services due to PKIX Path Building Failed**](https://confluence.atlassian.com/kb/unable-to-connect-to-ssl-services-due-to-pkix-path-building-failed-779355358.html)

2.  [**Connecting to SSL services**](https://confluence.atlassian.com/jira/connecting-to-ssl-services-117455.html)

For related topics on connecting repositories from other git hosts, see [Integration Guide](/git-integration-for-jira-cloud/integration-guide-gij-cloud).

&nbsp;
* * *

[**Prev:** Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/git-integration-for-jira-cloud/automatically-connect-to-https-git-repositories-with-self-signed-ssl-certificates-or-other-ssl-issues-gij-cloud)

[**Next:** Managing repository or integration configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud)

<p>&nbsp;</p>

