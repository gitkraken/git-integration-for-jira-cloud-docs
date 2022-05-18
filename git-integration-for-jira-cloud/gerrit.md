---

title: Gerrit
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Using **Jira Server or Data Center**? [See the corresponding article](https://bigbrassband.atlassian.net/wiki/x/AQDUB).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86474926/gerrit-banner-logo.png?version=1&modificationDate=1590827774620&cacheVersion=1&api=v2&width=272&height=112)

# Integrate Gerrit with Jira Cloud

Quickly learn how to connect Gerrit git repositories via Git Integration for Jira Cloud.

**What's on this page:**

* * *

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/eolraizc6s) _to open this video in a new browser tab for more viewing options._

## Full feature integration

1.  On your Jira Cloud dashboard, go to menu **Apps** ➜ **Git Integration: Manage Git repositories**.

2.  Click **Gerrit** on the Full feature integrations panel. The Full feature integration wizard appears.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86474926/gerrit-git-cloud-auto-connect-wiz-01(c).png?version=1&modificationDate=1590827775149&cacheVersion=1&api=v2&width=646&height=437)
    *   Enter your git server’s **Host URL**.

    *   Enter login credentials for username and password.

3.  Click **Next**. The Full feature integration wizard automatically reads git repositories for import into the git configuration.

4.  Click **Next**. The Project permissions screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86474926/gerrit-git-cloud-auto-connect-wiz-fin(c).png?version=2&modificationDate=1590827776120&cacheVersion=1&api=v2&width=646&height=438)
    *   Set **Project Permissions** by restricting it to specific projects or leave it as is (_associate with all projects_).

5.  Click **Connect** to complete this setup.


## Single repository (Manually connect via SSH/HTTP/HTTPS)

BigBrassBand recommends to use the Full feature integration for Gerrit.

Login to your Gerrit account. Obtain the repository URL from the Gerrit repository project page. Use SSH or HTTP/HTTPS.

1.  On your Jira Cloud dashboard menu, go to **Apps ➜ Git Integration: Manage Git repositories**.

2.  Click **Connect to Git Repository** to open the Connect Wizard.

3.  Paste the URL from Gerrit web portal in the provided box.
    (For e_xample:_ `http(s)://<your.org.com>/<repo_name>`)

4.  Click **Next**. The Project permissions page is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86474926/gerrit-git-cloud-auto-connect-wiz-fin(c).png?version=2&modificationDate=1590827776120&cacheVersion=1&api=v2&width=646&height=438)
    *   Set **Project Permissions** by restricting it to specific projects or leave it as is (_associate with all projects_).

5.  Click **Finish** to complete this process. 


The repository is now connected to Jira Cloud.

## Setting up Gerrit web links

Web links are automatically configured for Gerrit repositories with Full feature integration.

For single repository connections, web link setup is optional.

BigBrassBand recommends to use the Full feature integration for Gerrit.

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025229).

## Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level. 

For the case with Gerrit, the default main branch is always “master”.

Main branch for repositories within an integration can only be changed on the git server.