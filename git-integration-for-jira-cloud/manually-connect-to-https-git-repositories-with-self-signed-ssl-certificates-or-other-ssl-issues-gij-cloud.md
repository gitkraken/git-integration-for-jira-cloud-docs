---

title: Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>GITHUB ENTERPRISE</b> <b style='background-color:#FFE3B2; padding:1px 5px; color:#A35F00; border-radius:3px; margin: 0 5px; font-size: small;'>GITLAB CE/EE</b>

When connecting to a private HTTPS git repository, a problem may be caused by a custom (self-signed) certificate. See below for the steps to workaround this issue:

1.  Configure the repository to disable verification of the SSL certificate:

    *   Run `git config http.sslVerify false` in the repository folder.

        **Example:**

        ```bash
        cd project.git
        git config http.sslVerify false
        ```

2.  On the Manage integrations page, click on **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-integrations-page.png)

3.  Add the repository via **Plain Git integration** or **Quick start** on the Add integration page.

    ![](/wp-content/uploads/gij-add-new-integration-plain-git-sel.png)

4.  Enter **Host URL** and login credentials on the next screen. If 2FA is enabled on this account, enter PAT as the password.

5.  Click **Add integration** and continue to the end to complete this setup.

    ![](/wp-content/uploads/gij-gitserver-gitlab-server-bad-ssl-example-c.png)

6.  If there’s an SSL verification error, click **Ignore certificate errors and continue connection** to proceed.

There are alternative solutions to make Java trust this certificate. Refer to the good articles from Atlassian which focuses on helping to resolve SSL Verification Issues:

1.  [**Unable to Connect to SSL Services due to PKIX Path Building Failed**](https://confluence.atlassian.com/kb/unable-to-connect-to-ssl-services-due-to-pkix-path-building-failed-779355358.html)

2.  [**Connecting to SSL services**](https://confluence.atlassian.com/jira/connecting-to-ssl-services-117455.html)


For related topics on connecting repositories from other git hosts, see [Integration Guide](/git-integration-for-jira-cloud/integration-guide-gij-cloud).

&nbsp;
* * *
&nbsp;

[**Prev:** Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/git-integration-for-jira-cloud/automatically-connect-to-httos-git-repositories-with-self-signed-ssl-certificates-or-other-ssl-issues-gij-cloud)

[**Next:** Managing repository or integration configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud)

