---

title: Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
GITHUB ENTERPRISE GITLAB CE/EE

When connecting to a private HTTPS git repository, a problem may be caused by a custom (self-signed) certificate. See below for the steps to workaround this issue:

1.  Configure the repository to disable verification of the SSL certificate:

    *   Run `git config http.sslVerify false` in the repository folder.

        **Example:**

        ```java
        cd project.git
        git config http.sslVerify false
        ```

2.  Add the repository via Connect wizard on the Manage Git repository page.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024437/gitcloud-gitmgr-connect-wizard-button-sel(c3).png?version=1&modificationDate=1631096879883&cacheVersion=1&api=v2)
    1.  If there’s an SSL verification error, click **Ignore certificate errors and continue connection**.

    2.  Enter credentials on the following screen.

3.  Click **Connect** and continue to the end to complete this setup.



There are alternative solutions to make Java trust this certificate. Refer to the good articles from Atlassian which focuses on helping to resolve SSL Verification Issues:

1.  [**Unable to Connect to SSL Services due to PKIX Path Building Failed**](https://confluence.atlassian.com/kb/unable-to-connect-to-ssl-services-due-to-pkix-path-building-failed-779355358.html)

2.  [**Connecting to SSL services**](https://confluence.atlassian.com/jira/connecting-to-ssl-services-117455.html)


For related topics on connecting repositories from other git hosts, see [Integration Guide](/git-integration-for-jira-cloud/Integration-Guide).

[« Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/wiki/spaces/GITCLOUD/pages/1923024398/Automatically+connect+to+HTTPS+git+repositories+with+self-signed+SSL+certificates+or+other+SSL+issues)

[Managing repository or integration configuration »](/wiki/spaces/GITCLOUD/pages/1923024455/Managing+integration+or+repository+configuration)

### Related topics

*   Page:

    [Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/wiki/spaces/GITCLOUD/pages/1923024398/Automatically+connect+to+HTTPS+git+repositories+with+self-signed+SSL+certificates+or+other+SSL+issues) (Git Integration for Jira Cloud)

*   Page:

    [Self-signed HTTPS integration](/wiki/spaces/GITCLOUD/pages/1923024386/Self-signed+HTTPS+integration) (Git Integration for Jira Cloud)

*   Page:

    [Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/wiki/spaces/GITCLOUD/pages/1923024437/Manually+connect+to+HTTPS+git+repositories+with+self-signed+SSL+certificates+or+other+SSL+issues) (Git Integration for Jira Cloud)