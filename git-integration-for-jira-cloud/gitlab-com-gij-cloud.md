---

title: GitLab.com
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
        Using <b>Jira Server or Data Center</b>? <a href='/git-integration-for-jira-self-managed/gitlab-gij-self-managed'>See the corresponding article</a>.
    </div>
    </div>
</div>

&nbsp;

<img src='/wp-content/uploads/gitlab-mobile-custom1.png' style='margin:20px 0 30px 0;max-width:100%' />

## Integrate GitLab.com with Jira Cloud

GitLab introduced personal access tokens (PAT) since version 8.8 and now (v10+) prefers this type of authentication for accessing the git repositories.  Service users are strongly advised to switch from using username/password to using Personal Access Tokens (PAT) for GitLab.com.

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

Quickly learn how to connect GitLab.com git repositories via Git Integration for Jira Cloud app.

**What's on this page:**
- [Integrate GitLab.com with Jira Cloud](#integrate-gitlabcom-with-jira-cloud)
  - [Permissions](#permissions)
  - [Creating a personal access token](#creating-a-personal-access-token)
    - [Automatic token rotation](#automatic-token-rotation)
  - [Using Git service integration](#using-git-service-integration)
  - [Single git repository integration](#single-git-repository-integration)
  - [Setting up GitLab web links](#setting-up-gitlab-web-links)
  - [Viewing git commits in Jira Cloud](#viewing-git-commits-in-jira-cloud)
  - [Working with branches and merge requests with GitLab](#working-with-branches-and-merge-requests-with-gitlab)
    - [Default branch](#default-branch)
    - [Creating branches](#creating-branches)
    - [Creating merge requests](#creating-merge-requests)
  - [More Integration Guides](#more-integration-guides)

&nbsp;
<hr>
&nbsp;

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/hi45vum4yp?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:40px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/hi45vum4yp'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i><br> <i>(Updated video coming soon)</i>
</div>

&nbsp;

### Permissions

GitLab can have users with different access level to a group or project. If the user's connected GitLab repositories to Jira are not accessible or commits are not showing for that user -- it's related to permission issues. This can be a per user, repository or a project level restriction.

If you encounter access permission issues, you will need to ask your Git administrator to grant you the required level of access to specific projects. If you are a Git administrator, you will need to setup a GitLab user with the minimum required permissions to view GitLab projects from Jira.

Take the following cases for example:

*   The personal access token (PAT) that the GitLab user provided doesn't have the correct permissions within GitLab to view source code for specific repositories.

*   The GitLab user doesn't have access privileges to a GitLab repository or is not a member of a group that has access to specific repositories.


We recommend creating a specific GitLab user for the integration. This way, the GitLab user can have specific permissions to do the given tasks.

![gitlab user permissions or repository permissions](/wp-content/uploads/gij-gitlab-user-permissions-or-repository-permissions.png)

**For minimum access (read-only) permissions:**

1.  Set the user account profile's PAT scope to `read_repository`.

2.  The GitLab user is set to only **read** a specific repository. Set to **Reporter** role.


This level of access allows the user to view commits for the specific repository.

<br>

**For users who will be tasked with creating branches and merge requests:**

1.  Set the user account profile's PAT scope to `api`.

2.  The GitLab user should be set to **read/write** access for the specific repository. Set to **Developer** role.


This level of access allows the user to create/delete branches and create merge requests.

For more information, see [**GitLab Permissions »**](https://docs.gitlab.com/ee/user/permissions.html).

&nbsp;

### Creating a personal access token

There are several [Gitlab token types](https://docs.gitlab.com/ee/security/token_overview.html):

*   [Personal access token](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html)

*   [Project access token](https://docs.gitlab.com/ee/user/project/settings/project_access_tokens.html)

*   [Group access token](https://docs.gitlab.com/ee/user/group/settings/group_access_tokens.html)

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If two-factor authentication is enabled for your GitLab account, you will need to create a personal access token (PAT) to access your git repositories. Enable two-factor authentication in your GitLab.com account for increased security.
    </div>
    </div>
</div>

While instructions from GitLab works just fine, [follow this article](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) for a quick step-by-step guide to get you started.

Starting May 14, 2024, Gitlab is removing support for non-expiring personal access tokens (PATs) where all existing unlimited tokens will suddenly expire. To maintain integration connections with your GitLab repositories, create a new token and manually enter it into the corresponding field in the integration connection properties in Git Integration for Jira app (GIJ).

#### Automatic token rotation

GIJ can [automatically rotate tokens](https://docs.gitlab.com/ee/api/personal_access_tokens.html#rotate-a-personal-access-token) but we still encourage users to manually enter their tokens before or as soon as it expires.

The automatic rotation occurs only for the tokens used to connect Gitlab integrations. Any user PATs (used to create PRs) for Gitlab integrations aren't automatically rotated, and must be manually updated by each user themselves.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If a PAT is used to connect several Gitlab integrations – only the integration that rotates the PAT first will still work. All other integrations will fail as they don’t know the new PAT, and the old PAT has been revoked by the rotation. The Jira admin will have to generate new PATs for each failed integration and manually update them.
    </div>
    </div>
</div>

&nbsp;

### Using Git service integration

This process requires an existing GitLab.com account. Multiple git repositories in a GitLab.com account will be connected via Git Integration for Jira Cloud app.

While instructions from GitLab works just fine, here are some specific instructions to get you up and running.

We recommend using the Git service integration panel[1](#logo) to connect multiple repositories from your GitLab.com account.

1.  On your Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  For the following screen, click **GitLab.com** to start integration with this git service.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-type-gitlab-com.png)

4.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-gitlab-integration-oauth-sel.png)

5.  For this guide, click on the OAuth integration to select it.

    *   We recommend the OAuth integration which is outlined like a setup wizard — making it more easier for users to connect GitLab integrations.

    *   For PAT integration, use personal access tokens (PAT) to setup your GitLab integrations. Users will have to configure their own PAT from GitLab to use for this setup.

    *   For GitLab webhook indexing integration, see [this article](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud) instead.

    *   Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed. These settings are used with integration to retrieve the list of tracked repositories. Set a filter that will only load some cloned repositories which can be viewed in the Manage repositories page.

        ![](/wp-content/uploads/gij-gitcloud-integration-advanced-options-wo-sslverify-c.png)

        *   **Custom API Path**  –  this is a relative path that starts with "/". The maximum allowed length is 2000 characters or less. The integration will use the relative REST API path to retrieve the list of tracked repositories.

            For more information on GitLab custom API paths, see [GitLab API](https://docs.gitlab.com/ee/api/projects.html).

            For more examples, see article [Jira Cloud: Working with Custom API Path](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud).

            ```java
            GitLab version API support:
            -------------------------------------------
            Gitlab v9.5 and above -- only API v4.            
            ```

            <div class="bbb-callout bbb--note">
                <div class="irow">
                <div class="ilogobox">
                    <span class="logoimg"></span>
                </div>
                <div class="imsgbox">
                    <b>Remember:</b><br>
                    The GitLab.com API can see all the public projects. For GitLab.com, we recommend using JMESPath over the Custom API path when possible.
                </div>
                </div>
            </div>

        *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is 2000 characters or less.

            Read about JMESPath expressions on their [website](http://jmespath.org/). For help with writing expressions, please contact [support](mailto:support@gitkraken.com).

            To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

    *   While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

    

6.  Click **Connect to GitLab.com** to proceed to the next step.

7.  Sign in to your GitLab account, if prompted. When connecting to your GitLab account using OAuth for the first time, the user will be presented with a grant authorization screen.

    ![](/wp-content/uploads/gij-gitlab-autoconnect-grant-auth-screen-c.png)

    *   Grant organization access to a group to also have its repositories listed in the Manage repositories page.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b>&nbsp; If access is not granted, the repositories within those organizations (and even the orgs themselves) will not show up in the Git Integration for Jira app repositories list. The only way to see these repos/orgs is to return to the GitLab web portal using admin interface and specifically grant such permissions (Profile settings ➜ Developer settings ➜ OAuth Apps).

    *   Below are the differences between the three authentication options for GitLab:

        ```java
        Authentication Method       When are group repositories connected?
        ----------------------------------------------------------------------------
        OAuth                       Users should press "Authorize" on the grant
                                    authorization screen.
        ----------------------------------------------------------------------------
        PAT                         Group repositories are connected immediately.
        ----------------------------------------------------------------------------
        Username/Password           Group repositories are connected immediately.
        ```

    *   Click **Authorize...** to continue.

8.  On the following screen, the Git Integration for Jira app will read all available repositories from your GitLab account.

    ![](/wp-content/uploads/gij-gitcloud-integration-gitlab-repo-sel-c.png)

    *   Repositories of the logged-in GitLab user can be automatically connected to Jira Cloud. Repositories that are added or removed from GitLab will be likewise connected or disconnected from Jira Cloud.

    *   Use the search options to filter displayed repositories for the current screen.

    *   Connect all repositories and organizations or select specific repositories to connect for this integration.

9.  Click **Connect repositories** to complete this setup.


The GitLab.com git repositories are now connected to Jira Cloud.

There will be a slight delay in adding 2FA-enabled repositories compared to others. These will show in the git configuration list eventually.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Administrators</b><br>
        If you need to require users PAT for creating branches or merge requests, turn on this setting via the selected integration in Manage integrations page ➜ Actions ➜ Edit integration** ➜ <b>Feature settings</b>.
        <div style='margin:8px auto;margin-bottom:0px !important'><img src='/wp-content/uploads/gij-gitcloud-edit-integration-feature-cfg-req-user-PAT.png' /></div>
    </div>
    </div>
</div>

&nbsp;

### Single git repository integration

This process requires an existing GitLab git repository. Look for the the GitLab repository clone URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the GitLab git repository to your Jira Cloud via Git Integration for Jira app:

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

&nbsp;

### Setting up GitLab web links

The Git Integration for Jira app automatically configures web linking for GitLab git repositories.

For single repository connections, web link setup is optional. However, git links will become available in Git Commits tab when configured.

For more information on this feature, see [Documentation: Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud).

&nbsp;

### Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This action will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue on your Jira instance.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

&nbsp;

### Working with branches and merge requests with GitLab

This process requires a GitLab git repository and a PAT with `api` scope.

For GitLab Group, the user must have the **Write** permissions and the `api` PAT scope.

#### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master". This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level.

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

#### Creating branches

On your Jira Cloud instance, open a Jira issue. On the Jira Git integration development panel, click **Open Git integration** then click **Create branch**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-gitlab-com-dev-panel-create-branch-dlg.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab owner name. For example, `johnsmith/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a> page.

2.  Choose a **Source branch**. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one connected repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  Click **Create branch** to complete this process.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For more detailed information on this feature, see <a href='/git-integration-for-jira-cloud/create-branch-gij-cloud'>Create branch</a>.
    </div>
    </div>
</div>
<br>

The newly-created branch is now listed in the developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

#### Creating merge requests

The merge request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the Jira Git integration development panel, click **Open Git integration** then click **Create merge request**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-gitlab-com-dev-panel-create-mergereq-dlg.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab group name. For example, `BigBrassBand/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

2.  Choose the newly-created branch as the **Source branch**.
    
    <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one connected repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.

5.  Click **Create pull request** to complete this process. Follow the link to the PR to setup for review and approval.

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
        <b>Preview</b> allows you to see the comparison view of the current changes in the selected <b>Source branch</b> vs <b>Target branch</b> (<i>usually master</i>).
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For more detailed information on this feature, see <a href='/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud'>Create pull/merge request</a>.
    </div>
    </div>
</div>

The merge request is listed on the developer panel of the Jira issue page.

The merge request is also ready for approval by the reviewers in your GitLab web portal.

&nbsp;

### More Integration Guides

[GitHub.com](/git-integration-for-jira-cloud/github-com-gij-cloud) (Git Integration for Jira Cloud)

[GitHub Enterprise Server](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud) (Git Integration for Jira Cloud)

**GitLab.com** (this page)

[GitLab CE/EE](/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud) (Git Integration for Jira Cloud)

[Azure DevOps \| Visual Studio Team Services (VSTS)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud) (Git Integration for Jira Cloud)

[Azure DevOps Server \| Team Foundation Services (TFS)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud) (Git Integration for Jira Cloud)

[AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommmit-gij-cloud) (Git Integration for Jira Cloud)

[Gerrit](/git-integration-for-jira-cloud/gerrit-gij-cloud) (Git Integration for Jira Cloud)

[Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-gij-cloud) (Git Integration for Jira Cloud)

[Introduction to Git integration](/git-integration-for-jira-cloud/integration-guide-gij-cloud) (Git Integration for Jira Cloud)

&nbsp;

<br>

&nbsp;

<div style='border-top: 1px solid #456; width: 40%; padding-bottom: 12px'></div>
<div style='font-size: 12px;'>
    <sup>1</sup> <i>Logo owned by <a href='https://gitlab.com/'>GitLab Inc</a> used under <a href='https://creativecommons.org/licenses/by-nc-sa/4.0/'>license</a>.
    <p>&nbsp;&nbsp;All product names, logos, and brands are property of their respective owners.<p><i>
</div>

