---

title: Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>GITHUB ENTERPRISE</b> <b style='background-color:#FFE3B2; padding:1px 5px; color:#A35F00; border-radius:3px; margin: 0 5px; font-size: small;'>GITLAB CE/EE</b>

Perform full feature integration with HTTPS git repositories that have self-signed SSL certificates or other SSL issues.

For this guide, we will use GitLab Server as an example:

1.  On your Jira dashboard, go to menu Apps ➜ **Git Integration: Manage Git repositories**. The following page is displayed.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-integrations-page.png)

2.  On the Git host service selection screen, click on **GitLab server** then click on **GitLab Server (CE/EE) APIv4** to select this integration type.

    ![](/wp-content/uploads/gij-gitcloud-add-integration-type-gitlab-server-sel.png)

    *   Enter the **Host URL** of the private git server.
    *   Enter **Personal access token** for this server (APIv4). _Support for APIv3 is deprecated._

3.  Click **Connect and select repositories**.

4.  If there is an indication of an SSL error, the following screen is displayed.

    ![](/wp-content/uploads/gij-gitserver-gitlab-server-bad-ssl-example-c.png)

5.  Click **Ignore certificate errors and continue connection**. This will ignore SSL verification if it's self-signed or expired.

8.  Select repositories or import all of them and then click **Connect repositories** to complete the setup.

This integration is displayed on the Manage integrations list. Go to ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit integration** if desired to make some changes to the repository settings.

&nbsp;
* * *

[**Prev:** Self-signed HTTPS connections (index)](/git-integration-for-jira-cloud/self-signed-https-integration-gij-cloud)

[**Next:** Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/git-integration-for-jira-cloud/manually-connect-to-https-git-repositories-with-self-signed-ssl-certificates-or-other-ssl-issues-gij-cloud)

