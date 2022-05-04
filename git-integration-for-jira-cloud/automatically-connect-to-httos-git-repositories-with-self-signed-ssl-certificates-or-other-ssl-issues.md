---

title: Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923024398/Automatically+connect+to+HTTPS+git+repositories+with+self-signed+SSL+certificates+or+other+SSL+issues>

* * *

GITHUB ENTERPRISE GITLAB CE/EE

Perform full feature integration with HTTPS git repositories that have self-signed SSL certificates or other SSL issues.

For this guide, we will use GitLab as an example:

1.  On your Jira dashboard, go to menu Apps ➜ **Git Integration: Manage Git repositories**. The following page is displayed.
    
    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024398/gitcloud-gitmgr-gitlab-sel-sslverify(c).png?version=1&modificationDate=1631095982506&cacheVersion=1&api=v2)
2.  On the Full feature integrations panel, click **GitLab**.
    
3.  For External service, select **GitLab Server (CE/EE) v4**.
    
4.  Enter the remote URL of the private git server.
    
5.  Enter Personal access token for this server (APIv4). Support for APIv3 is deprecated.
    
6.  Click **Next** to continue. If there is an indication of an SSL error, the following screen is displayed.
    
    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923024398/gitserver-gitlab-server-bad-ssl-example(c).png?version=1&modificationDate=1630063605235&cacheVersion=1&api=v2&width=646&height=428)
7.  Click **Ignore certificate errors and continue connection**. This will ignore SSL verification if it's self-signed or expired.
    
8.  Import the detected repositories and then click **Finish** to complete the setup.
    

[« Self-signed HTTPS connections](/wiki/spaces/GITCLOUD/pages/1923024386/Self-signed+HTTPS+integration)

[Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues »](/wiki/spaces/GITCLOUD/pages/1923024437/Manually+connect+to+HTTPS+git+repositories+with+self-signed+SSL+certificates+or+other+SSL+issues)

### More related topics about self-signed HTTPS connection

*   Page:
    
    [Automatically connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/wiki/spaces/GITCLOUD/pages/1923024398/Automatically+connect+to+HTTPS+git+repositories+with+self-signed+SSL+certificates+or+other+SSL+issues) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Self-signed HTTPS integration](/wiki/spaces/GITCLOUD/pages/1923024386/Self-signed+HTTPS+integration) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Manually connect to HTTPS git repositories with self-signed SSL certificates or other SSL issues](/wiki/spaces/GITCLOUD/pages/1923024437/Manually+connect+to+HTTPS+git+repositories+with+self-signed+SSL+certificates+or+other+SSL+issues) (Git Integration for Jira Cloud)