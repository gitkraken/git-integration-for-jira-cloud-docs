---

title: Gerrit
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Using <b>Jira Server</b> or <b>Data Center</b>? <a href='/git-integration-for-jira-self-managed/gerrit-gij-self-managed'>See the corresponding article</a>.
    </div>
    </div>
</div>

&nbsp;

![](/wp-content/uploads/gerrit-banner-logo.png)

&nbsp;

# Integrate Gerrit with Jira Cloud

Quickly learn how to connect Gerrit git repositories via Git Integration for Jira Cloud.

**What's on this page:**
- [Integrate Gerrit with Jira Cloud](#integrate-gerrit-with-jira-cloud)
  - [Git service integration](#git-service-integration)
  - [Single repository (Manually connect via SSH/HTTP/HTTPS)](#single-repository-manually-connect-via-sshhttphttps)
  - [Setting up Gerrit web links](#setting-up-gerrit-web-links)
  - [Viewing git commits in Jira Cloud](#viewing-git-commits-in-jira-cloud)
  - [Default branch](#default-branch)
  - [More Integration Guides](#more-integration-guides)

<br>
<br>
<hr>
<br>
<br>

## Git service integration

1.  On your Jira side bar, go to Apps ➜ **Git Integration for Jira**, then **Settings** ➜ **Manage Integrations**

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c-2025.png)

2.  On the Manage integrations page, click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-2025.png)

3.  For the following screen, click **Gerrit (self-managed)** to start integration with this git service.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-gerrit-2025.png)

4.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-integration-type-gerrit-full-feature-2025.png)

5.  For this guide, continue with the default selected type for Gerrit integration.

    *   We recommend the default full feature integration for this git service.

    *   <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>UNDER CONSTRUCTION</b> For Gerrit webhook indexing integration, see <a href='/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud'>this article</a> instead.

    *   Enter the **Host URL** of your Gerrit server.

    *   Provide the **User name** and **Password/Token** for this Gerrit server.

6.  Click **Connect and select repositories** to proceed to the next step.

7.  On the following screen, the Git Integration for Jira app will read all available repositories from your Gerrit account.

    ![](/wp-content/uploads/gij-gitcloud-integration-gerrit-repo-sel.png)

    *   Repositories of the logged-in Gerrit user can be automatically connected to Jira Cloud. Repositories that are added or removed from GitLab will be likewise connected or disconnected from Jira Cloud. (_Connect all future repositories_)

    *   Use the search options to filter displayed repositories for the current screen.

    *   Connect all repositories and organizations or select specific repositories to connect for this integration.

8.  Click **Connect repositories** to complete this setup.

The Gerrit git repositories are now connected to Jira Cloud.


## Single repository (Manually connect via SSH/HTTP/HTTPS)

BigBrassBand recommends to use the Git service integration for Gerrit.

Use this section for setting up single repository connections or connecting single repositories via SSH.

Login to your Gerrit account. Obtain the repository URL from the Gerrit repository project page. Use either SSH or Anonymous HTTPS.

1.  On your Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Manage integrations**.

2.  On the following screen, click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-single-repo-http-ssh-gerrit-integration-2025.png)

4.  Paste the git clone URL from Gerrit web portal in the provided box.
    (For e_xample:_ `http(s)://<your.org.com>/<repo_name>`)

5.  Click **Connect** to proceed. The following screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-single-repo-http-ssh-gerrit-configure-2025.png)

    1.  Enter **Host URL** for this integration.

    2.  Enter **Username** on the provided box.

    3.  Enter **Password/Token** on the provided box.

6.  Click **Add integration** to complete this process.


The repository is now connected to Jira Cloud.

## Setting up Gerrit web links

Web links are automatically configured for Gerrit repositories connected via Git service integration. We recommend to use the Git service integration for Gerrit account connections. Note that if the repository is part of a Gerrit integration, web linking settings are not available.

For single repository connections, the web linking setup is optional (!Actions ➜ Edit integration ➜ **Feature settings**).

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level. 

For the case with Gerrit, the default main branch is always “master”.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Main branch for repositories within an integration can only be changed on the git server.
    </div>
    </div>
</div>
<br>

&nbsp;

## More Integration Guides

[GitHub.com](/git-integration-for-jira-cloud/github-com-gij-cloud)

[GitHub Enterprise Server](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud)

[GitLab.com](/git-integration-for-jira-cloud/gitlab-com-gij-cloud)

[GitLab CE/EE](/git-integration-for-jira-cloud/github-ce-ee-com-gij-cloud)

[Azure DevOps | Visual Studio Team Services (VSTS)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud)

[Azure DevOps Server | Team Foundation Services (TFS)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud)

[AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommmit-gij-cloud)

**Gerrit** (this page)

[Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-gij-cloud)

[Introduction to Git integration](/git-integration-for-jira-cloud/integration-guide-gij-cloud)

