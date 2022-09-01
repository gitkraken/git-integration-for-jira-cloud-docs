---

title: Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
* * *

<b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>GITHUB ENTERPRISE</b> <b style='background-color:#FFE3B2; padding:1px 5px; color:#A35F00; border-radius:3px; margin: 0 5px; font-size: small;'>GITLAB CE/EE</b>

Perform full feature integration with HTTPS git repositories that have self-signed SSL certificates or other SSL issues.

For this guide, we will use GitLab as an example:

1.  On your Jira dashboard, go to menu Apps ➜ **Git Integration: Manage Git repositories**. The following page is displayed.

    <img src='/wp-content/uploads/gij-gitcloud-gitmgr-gitlab-sel-sslverify-c.png' style='height:auto;max-width:100%;margin-top:20px;margin-bottom:20px;' />

2.  On the Full feature integrations panel, click **GitLab**.

3.  For External service, select **GitLab Server (CE/EE) v4**.

4.  Enter the remote URL of the private git server.

5.  Enter Personal access token for this server (APIv4). Support for APIv3 is deprecated.

6.  Click **Next** to continue. If there is an indication of an SSL error, the following screen is displayed.

    <img src='/wp-content/uploads/gij-gitserver-gitlab-server-bad-ssl-example-c.png' style='height:auto;max-width:100%;margin-top:20px;margin-bottom:20px;' />    

7.  Click **Ignore certificate errors and continue connection**. This will ignore SSL verification if it's self-signed or expired.

8.  Import the detected repositories and then click **Finish** to complete the setup.


[Self-signed HTTPS connections](/git-integration-for-jira-cloud/self-signed-https-integration-gij-cloud)

[Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/git-integration-for-jira-cloud/manually-connect-to-https-git-repositories-with-self-signed-ssl-certificates-or-other-ssl-issues-gij-cloud)

