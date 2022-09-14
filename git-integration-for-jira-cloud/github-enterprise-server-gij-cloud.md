---

title: GitHub Enterprise Server
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        These instructions apply to self-hosted GitHub Enterprise Server.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For instructions to instances hosted on GitHub.com (Free, Team, Enterprise (including <a href='https://docs.github.com/en/enterprise-cloud@latest/admin/identity-and-access-management/managing-iam-with-enterprise-managed-users/about-enterprise-managed-users'><b>EMU</b></a>) plans), please go to <a href='/git-integration-for-jira-cloud/github-com-gij-cloud'>this page</a>.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Using <b>Jira Server</b> or <b>Data Center</b>? <a href='/git-integration-for-jira-data-center/github-enterprise-server-gij-self-managed'>See the corresponding article</a>.
    </div>
    </div>
</div>
<br>

&nbsp;

<img src='/wp-content/uploads/gij-github-ent-server-banner-logo.png' style='max-width:100%' width-615 height=71 />

<br>

# Integrate GitHub Enterprise Server with Jira Cloud

Quickly learn how to connect GitHub Enterprise Server git repositories via Git Integration for Jira Cloud.

**What's on this page:**
- [Integrate GitHub Enterprise Server with Jira Cloud](#integrate-github-enterprise-server-with-jira-cloud)
  - [Creating a personal access token](#creating-a-personal-access-token)
  - [Using Git service integration](#using-git-service-integration)
  - [Single git repository integration](#single-git-repository-integration)
  - [Setting up GitHub Enterprise Server permissions](#setting-up-github-enterprise-server-permissions)
    - [Default repository permission](#default-repository-permission)
    - [Teams and collaborators](#teams-and-collaborators)
  - [Setting up GitHub web links](#setting-up-github-web-links)
  - [Viewing git commits in Jira Cloud](#viewing-git-commits-in-jira-cloud)
  - [Working with branches and pull requests with GitHub Enterprise Server](#working-with-branches-and-pull-requests-with-github-enterprise-server)
    - [Default branch](#default-branch)
    - [Creating branches](#creating-branches)
    - [Creating pull requests](#creating-pull-requests)
  - [More Integration Guides](#more-integration-guides)

<br>
<hr>
<br>

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/vfwwqnn3mm?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px;margin-bottom:40px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/vfwwqnn3mm'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

## Creating a personal access token

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If two-factor authentication is enabled for your GitHub Enterprise Server account, you will need to create a personal access token (PAT) to access your git repositories. Enable two-factor authentication in your GitHub Enterprise Server account for increased security.
    </div>
    </div>
</div>
<br>

While instructions from GitHub works just fine, [follow this article](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) for a quick step-by-step guide to get you started.

## Using Git service integration

This process requires an existing GitHub Enterprise Server account. 

We recommend using the **Git service integration** panel to connect multiple repositories from your GitHub Enterprise Server account.

1.  On your Jira Cloud dashboard menu, go to **Apps ➜ Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c).png)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-service-sel-c.png)

4.  The following screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-integration-ghe-server-connect-service-c.png)

    *   Select **GitHub Enterprise Server (self-managed)** from the Git hosting service drop down list.

    *   For the **Host URL**, enter the address of the GitHub Enterprise Server.

    *   For admins/owners, repository managers, collaborators or users that have enabled 2FA, enter username to the **Login** field and enter the PAT on the **Token** field.

5.  Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed.

    ![](/wp-content/uploads/gij-gitcloud-integration-advanced-options-std-c.png)

    *   **SSL Verify** – The **SSL Verify** option is set to `Enabled` by default. If set to `Disabled`, the Git Integration for Jira Cloud app will ignore verification of SSL certificates when connecting to a git server. _This option is not available for non-fetched repositories._

    *   **Custom API Path**  –  this is a relative path that starts with "/". The maximum allowed length is 2000 characters or less. The integration will use the relative REST API path to retrieve the list of tracked repositories.

        To learn more examples, see article [Jira Cloud: Working with Custom API Path](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

    *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is 2000 characters or less.

        Read about JMESPath expressions on their [website](http://jmespath.org/). For help with writing expressions, please contact [support](mailto:support@bigbrassband.com).
        To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

    *   While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

6.  Click **Connect and select repositories**. The Git Integration for Jira app will read all available repositories from your GitHub Enterprise Server account.

7.  The following screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-integration-ghe-server-repo-sel-c.png)

    *   Repositories that are added or removed from GitHub will be likewise connected or disconnected from Jira Cloud.

    *   Use the search options to filter displayed repositories for the current screen.

    *   Connect all repositories and organizations or select specific repositories to connect for this integration.

8.  Click **Connect repositories** to complete the setup.


GitHub Enterprise Server repositories are now connected to Jira Cloud.

## Single git repository integration

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This section is for users who are using SSH connections or those who wanted to only connect a single specific repository.
    </div>
    </div>
</div>
<br>

This process requires an existing GitHub Enterprise Server git repository. Look for the the repository clone URL on the repository project page.

Use this information to connect the GitHub git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

## Setting up GitHub Enterprise Server permissions

We recommend using a "service user" in GitHub Enterprise Server _(example: "GitIntegrationforJira")_ to be used to integrate with Git Integration for Jira app. This dedicated "service user" will allow the GitHub Enterprise Server administrator to set permissions so the app clones only the desired repositories.

Assign GitHub Enterprise Server permissions for team members or collaborators to allow which resources are accessible for service users. This feature is only available in a GitHub Organization.

### Default repository permission

1.  Login to your GitHub Enterprise Server account.

2.  Go to ![profile icon](/wp-content/uploads/gij-profile-icon.png) **Profile** ➜ **Settings**.

3.  On your sidebar, click **Organizations**.

4.  Click **Settings** for the selected organization.

5.  On your sidebar, click **Member Privileges**. The following screen is displayed.

    ![](/wp-content/uploads/gij-github-org-repo-base-permissions-c.png)

6.  Under the **Base permissions**, click on the dropdown button.

    *   Choose the base permission level for organization members. The base repository permission only applies to organization members and not to outside collaborators. If the base permission is set to _**None**_, organization members will need to be given access to repositories using the _**Teams or Collaborators**_ methods (see below).

7.  **Save** the changes.


For more information, see [**Access Permissions on GitHub »**](https://help.github.com/articles/access-permissions-on-github/).

### Teams and collaborators

To give a member additional access, they must be added to a team or make them collaborators on individual repos.

**Set default repository permission for the current team:**

1.  Open an organization team. (_Your org ➜ Teams ➜ scroll down to the bottom then click the desired team._)

2.  Click the **Repositories** tab.

    ![](/wp-content/uploads/gij-github-org-repo-team-repo-permissions-c.png)

3.  Set **Read**, **Write** or **Admin** repository access as desired.


**Assign members to a team on your GitHub repository:**

1.  Create a team in your GitHub Organization.

2.  Invite a member to add it into the team. An email invitation is sent to that GitHub service user.

    ![](/wp-content/uploads/gij-github-add-members-to-team-c.png)

    *   The service user is then added to the team if the invitation has been accepted.

3.  Click the service user to manage permissions for this member to:

    1.  Set desired Role for this member.

    2.  Convert this member to outside collaborator.

    3.  Give this member access to organization repositories.

    4.  Remove this member from the team.

4.  Click **Manage access** to manage repository access for this member.

    ![](/wp-content/uploads/gij-github-manage-team-repo-permission-c.png)

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Organization Permissions</b?<br>
While users have configured PAT for repository access, users in a GitHub Organization must at least have **Read** permissions. This allows them to view commits and smart commits (if enabled) of connected GitHub Organization repositories inside Jira.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>GitHub Organization</b><br>
For collaborators and commit authors, set these users to have <b>Write</b> permissions. This will allow them to view commits and smart commits, browse repositories and also enables them to create branches and pull requests to specified GitHub git repositories via developer panel of a Jira issue.
    </div>
    </div>
</div>
<br>

For more information on organization teams, see [**GitHub: Organizing Members into Teams »**](https://help.github.com/articles/organizing-members-into-teams/).

For more information on inviting collaborators, see [**Inviting Collaborators to a Personal/Organization Repository »**](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/).

## Setting up GitHub web links

The Git Integration for Jira app automatically configures web linking for GitHub Enterprise Server git repositories.

For single repository connections, web link setup is optional. However, git links will become available in Git Commits tab when configured.

For more information on this feature, see [Documentation: Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud).

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This action will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View Full Commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Working with branches and pull requests with GitHub Enterprise Server

This process requires a GitHub Enterprise Server git repository and a PAT with `repo` scopes.

For GitHub Organization, the user must have the **Write** permissions and the `repo` PAT scopes.

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level.

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

### Creating branches

On your Jira Cloud, open a Jira issue. On the Jira Git integration development panel, click **Open** **Git Integration** then click **Create branch**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-issue-dev-panel-create-branch-dlg.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

2.  Choose a **Base branch**.

    <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the branch to be the default selected branch for the active repository. To configure default branches for more than one repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Enter a **Branch name** or leave it as is (recommended).

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

### Creating pull requests

The pull request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Git Integration**, click **Create pull request**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-issue-dev-panel-create-pull-req-dlg.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

2.  Choose the newly-created branch as the **Source branch**.

    <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp;Designate the branch to be the default selected branch for the active repository. To configure default branches for more than one repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Preview</b> allows you to see the comparison view of the current changes in the selected <b>Source branch</b> vs <b>Target branch</b> (<i>usually master</i>).
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For more detailed information on this feature, see <a href='/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud'>Create pull/merge request</a>.
    </div>
    </div>
</div>
<br>


The pull request is listed on the developer panel of the Jira issue page.

The pull request is also ready for approval by the reviewers in your GitHub web portal.

## More Integration Guides

[GitHub.com (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/github-com-gij-cloud)

[GitLab CE/EE (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud)

[GitHub Enterprise Server (this page)

[GitLab.com (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/gitlab-com-gij-cloud)

[Azure DevOps | Visual Studio Team Services (VSTS) (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud)

[Azure DevOps Server | Team Foundation Services (TFS) (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud)

[AWS CodeCommit (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/aws-codecommmit-gij-cloud)

[Gerrit (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/gerrit-gij-cloud)

[Bitbucket Cloud (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/bitbucket-gij-cloud)

[Introduction to Git integration (Git Integration for Jira Cloud)](/git-integration-for-jira-cloud/integration-guide-gij-cloud)

