---

title: GitLab CE/EE
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
        Using <b>Jira Server or Data Center</b>? <a href='/git-integration-for-jira-self-managed/gitlab-ce-ee-gij-self-managed'>See the corresponding article</a>.
    </div>
    </div>
</div>
<br><br>

<img src='/wp-content/uploads/gitlab-ceee-integration-banner-logo.png' style='max-width:100%;margin-bottom:40px' width=408 height=93 />

# Integrate GitLab CE/EE with Jira Cloud

This feature tracks added or deleted repositories from a remote GitLab server (EE/CE) and automatically imports those Git repository references into Jira.

GitLab v10+ stopped accepting username/password credentials for API access and will only recognize Personal Access Tokens (PAT) and OAuth authentications. Service users are strongly advised to switch from using username/password for newer versions of GitLab Server (CE/EE) to using PAT.

For GitLab Server service users, they won't see the issue until they upgrade their GitLab Servers to version 10 and higher. Git Integration for Jira app offers pre-v10 GitLab Server service users as a Legacy connection option.

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Support for Gitlab API v3 is deprecated. We recommend to use <b>GitLab API v4</b> when adding new integrations for increased security.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        BigBrassBand recommends a dedicated user for this integration which has access permissions to the GitLab CE/EE git repositories.
    </div>
    </div>
</div>
<br>

Quickly learn how to connect GitLab CE/EE git repositories via Git Integration for Jira Server app.

**What's on this page:**
- [Integrate GitLab CE/EE with Jira Cloud](#integrate-gitlab-ceee-with-jira-cloud)
  - [Permissions](#permissions)
  - [Creating a personal access token](#creating-a-personal-access-token)
  - [Using Git service integration](#using-git-service-integration)
  - [Single git repository integration](#single-git-repository-integration)
  - [Setting up GitLab web links](#setting-up-gitlab-web-links)
  - [Viewing git commits in Jira Cloud](#viewing-git-commits-in-jira-cloud)
  - [Working with branches and merge requests with GitLab CE/EE](#working-with-branches-and-merge-requests-with-gitlab-ceee)
    - [Default branch](#default-branch)
    - [Creating Branches](#creating-branches)
    - [Creating merge requests](#creating-merge-requests)
  - [More Integration Guides](#more-integration-guides)

<br>
<hr>
<br>

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/q9q0zg3rug?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px;margin-bottom:40px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/q9q0zg3rug'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

## Permissions

GitLab can have users with different access level to a group or project. If the user's connected GitLab repositories to Jira are not accessible or commits are not showing for that user -- it's related to permission issues. This can be a per user, repository or a project level restriction.

If you encounter access permission issues, you will need to ask your Git administrator to grant you the required level of access to specific projects. If you are a Git administrator, you will need to setup a GitLab user with the minimum required permissions to view GitLab projects from Jira.

Take the following cases for example:

*   The personal access token (PAT) that the GitLab user provided doesn't have the correct permissions within GitLab to view source code for specific repositories.

*   The GitLab user doesn't have access privileges to a GitLab repository or is not a member of a group that has access to specific repositories.


We recommend creating a specific GitLab user for the integration. This way, the GitLab user can have specific permissions to do the given tasks.

![gitlab user permissions or repository permissions](/wp-content/uploads/gij-gitlab-user-permissions-or-repository-permissions.png)

**For minimum access (read-only) permissions:**

1.  Set the user account profile's PAT scope to **read\_repository**.

2.  The GitLab user is set to only **read** a specific repository. Set to **Reporter** role.


This level of access allows the user to view commits for the specific repository.

**For users who will be tasked with creating branches and merge requests:**

1.  Set the user account profile's PAT scope to **api**.

2.  The GitLab user should be set to **read/write** access for the specific repository. Set to **Developer** role.


This level of access allows the user to create/delete branches and create merge requests.

For more information, see <a href='https://docs.gitlab.com/ee/user/permissions.html' target='_blank'><b>GitLab Permissions »</b></a>.

## Creating a personal access token

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If two-factor authentication is enabled for your GitLab Server account, you will need to create a personal access token (PAT) to access your git repositories. Enable two-factor authentication in your GitLab Server account for increased security.
    </div>
    </div>
</div>
<br>

While instructions from GitHub works just fine, [follow this article](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) for a quick step-by-step guide to get you started.

## Using Git service integration

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Support for Gitlab API v3 is deprecated. We recommend to use <b>GitLab API v4</b> when adding new integrations for increased security.
    </div>
    </div>
</div>
<br>

This process requires an existing GitLab Server EE or GitLab Server CE. If your GitLab Server version is 10.2 or newer, a [personal access token](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) must be configured.

We recommend using the Full feature integrations panel to connect multiple repositories from your GitLab CE/EE account.

1.  On the Jira Cloud dashboard menu, go to **Apps** ➜ **Git Integration: Manage integrations**. The git configuration page for connecting repositories is displayed.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-service-sel-c.png)

4.  The following screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-gitlab-ceee-git-service-sel-c.png)

    *   Choose <b>GitLab</b><a href='#gitlab-logo-license'><sup>1</sup></a> **Server CE/EE (APIv4)** from the Git hosting service list.

    *   Enter the **Host URL** of the GitLab Server

    *   Enter the **Personal Access Token** for server authentication. 2FA must be enabled in your GitLab Server and [PAT has been configured](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud).

    *   Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed. These settings are used with integration to retrieve the list of tracked repositories. Set a filter that will only load some cloned repositories which can be viewed in the Manage repositories page.

        ![](/wp-content/uploads/gij-gitcloud-integration-advanced-options-wo-sslverify-c.png)

        *   **Custom API Path**  –  this is a relative path that starts with "/". The maximum allowed length is 2000 characters or less. The integration will use the relative REST API path to retrieve the list of tracked repositories. For more information on GitLab custom API paths, see [GitLab API](https://docs.gitlab.com/ee/api/projects.html). For more examples, see article [Jira Cloud: Working with Custom API Path](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud).

            ```java
            GitLab version API support:
            -------------------------------------------
            Gitlab v9.5 and above -- only API v4.
            Gitlab v9.0 to v9.4.x -- API v3 and API v4.
            ```

        *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is 2000 characters or less.

            Read about JMESPath expressions on their [website](http://jmespath.org/). For help with writing expressions, please contact [support](mailto:support@bigbrassband.com).

            To know more examples, see article [Jira Cloud: Working with JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

    *   While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

5.  Click **Connect and select repositories**. The Git Integration for Jira app will import detected GitLab CE/EE repositories.

    *   Currently, the Git Integration for Jira app scans only the repositories visible to the user which is used for scanning. The repositories which are publicly visible _(shared for all members or visible to the member with the admin rights)_ will not be scanned. This will be supported in a future release.

6.  On the following screen, the Git Integration for Jira app will read all available repositories from your GitLab account.

    ![](/wp-content/uploads/gij-gitcloud-gitlab-ceee-repo-sel-c.png)

7.  Click **Connect** **repositories** to complete this setup.


GitLab CE/EE repositories are now connected to Jira Cloud. The GitLab server is added to the repositories list as a connected server and is automatically reindexed.

Repositories added or removed from GitLab server will be likewise added or removed from Jira Cloud. There will be a slight delay in adding 2FA-enabled repositories compared to others. These will show in the git configuration list eventually.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Git Integration for Jira app supports GitLab API v4 (in both Jira Cloud and Jira Server/Data Center).
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For newer GitLab authentication - in order to access a Git repository over HTTP, use the username as the username and the PAT for the password.
    </div>
    </div>
</div>

<table>
    <tr>
        <td>
            <div class="bbb-callout bbb--alert" style='margin-top:0px !important'>
                <div class="irow">
                <div class="ilogobox">
                    <span class="logoimg"></span>
                </div>
                <div class="imsgbox">
                    <b>Administrators</b><br>
                    If you need to require users PAT for creating branches or merge requests, turn on this setting via the selected integration in Manage integrations page ➜ Actions ➜ <b>Edit integration</b>.
                </div>
                </div>
            </div>
            <p style='margin-bottom:0px !important'><img src='/wp-content/uploads/gij-gitcloud-edit-integration-feature-cfg-req-user-PAT.png' width=702 height=78 style='margin:20px auto 0px auto !important;max-width:100%;display:block;' /></p>
        </td>
    </tr>
</table>

## Single git repository integration

This process requires an existing GitLab CE/EE git repository. Look for the the GitLab CE/EE repository clone URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the GitLab CE/EE git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

[Single git repository integration (SSH)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-ssh-gij-cloud)

There will be a slight delay in adding 2FA-enabled repositories compared to others. These will show in the git configuration list eventually.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        In order to access a Git repository over HTTP, use the username as the username and the PAT for the password.
    </div>
    </div>
</div>
<br>

## Setting up GitLab web links

The Git Integration for Jira app automatically configures web linking for GitLab git repositories.

For single repository connections, web link setup is optional. However, git links will become available in Git Commits tab when configured.

For more information on this feature, see [Documentation: Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud).

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This action will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue on your Jira instance.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View Full Commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Working with branches and merge requests with GitLab CE/EE

For GitLab CE/EE (Legacy or newer), the user must have the **Write** permissions and the `api` PAT scope.

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex.  Auto-connected integrations support this feature where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level.

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

### Creating Branches

On your Jira Cloud, open a Jira issue. On the [Jira Git integration development panel](/git-integration-for-jira-cloud/jira-git-integration-development-panel-gij-cloud), click **Open Git Integration** then click **Create branch**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-gitlab-ceee-create-branch-dlg.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab owner name. For example, `johnsmith/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

2.  Choose a **Source branch**.

    <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one connected repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  Click **Create branch** to complete this process.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For more detailed information on this feature, see <a href='/git-integration-for-jira-cloud/create-branch-gij-cloud'>Create Branch</a>.
    </div>
    </div>
</div>
<br>

The newly-created branch is now listed in the developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

### Creating merge requests

The merge request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the Jira Git integration development panel, click **Open Git integration** then click **Create merge request**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-ceee-dev-panel-create-merge-req-dlg.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab group name. For example, `BigBrassBand/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/gitlab-com-gij-cloud) page.

2.  Choose the newly-created branch as the **Source branch**.

    <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one connected repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.

5.  Click **Create merge request** to complete this process. Follow the link to the PR to setup for review and approval.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Merge requests are still indexed based on branch name even if the MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Preview</b> allows you to see the comparison view of the current changes in the selected <b>Source branch</b>> vs <b>Target branch</b> (<i>usually master</i>).
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For more detailed information on this feature, see <a href='/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud'>Creating merge requests</a>.
    </div>
    </div>
</div>
<br>

The merge request is listed on the developer panel of the Jira issue page.

The merge request is also ready for approval by the reviewers in your GitLab web portal.

## More Integration Guides

[GitHub.com (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/github-com-gij-cloud)

GitLab CE/EE (this page)

[GitHub Enterprise Server (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud)

[GitLab.com (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/gitlab-com-gij-cloud)

[Azure DevOps | Visual Studio Team Services (VSTS) (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud)

[Azure DevOps Server | Team Foundation Services (TFS) (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud)

[AWS CodeCommit (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/aws-codecommmit-gij-cloud)

[Gerrit (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/gerrit-gij-cloud)

[Bitbucket Cloud (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/bitbucket-gij-cloud)

[Introduction to Git integration (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/integration-guide-gij-cloud)


<br>
<br>
<div style='border-top: 1px solid #456; width: 40%; padding-bottom: 12px'></div>
<div style='font-size: 12px;' id='gitlab-logo-license'>
    <sup>1</sup> <i>Logo owned by <a href='https://gitlab.com/'>GitLab Inc</a> used under <a href='https://creativecommons.org/licenses/by-nc-sa/4.0/'>license</a>.
    <p>&nbsp;&nbsp;All product names, logos, and brands are property of their respective owners.<p><i>
</div>

