---

title: GitHub.com
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
        These instructions apply to instances on Free, Team, Cloud Enterprise (including <a href='https://docs.github.com/en/enterprise-cloud@latest/admin/identity-and-access-management/managing-iam-with-enterprise-managed-users/about-enterprise-managed-users'><b>EMU</b></a>) plans hosted on GitHub.com.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For instructions on self-hosted GitHub Enterprise Server, please see <a href='/git-integration-for-jira-data-center/github-enterprise-server-gij-self-managed'>this page</a>.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Using Jira Server or Data Center? See the <a href='/git-integration-for-jira-data-center/github-gij-self-managed'>corresponding article</a>.
    </div>
    </div>
</div>
<br>

&nbsp;

<img src='/wp-content/uploads/gij-github-mobile-logo-dark.png' height=100 width=355 style='max-width:100%' />

<br>

# Integrate GitHub.com with Jira Cloud

Quickly learn how to connect GitHub.com git repositories via Git Integration for Jira Cloud app.

**What's on this page:**
- [Integrate GitHub.com with Jira Cloud](#integrate-githubcom-with-jira-cloud)
  - [Creating a personal access token](#creating-a-personal-access-token)
  - [Using Git service integration](#using-git-service-integration)
  - [Single git repository integration](#single-git-repository-integration)
  - [Setting up GitHub permissions](#setting-up-github-permissions)
    - [Default repository permission](#default-repository-permission)
    - [Teams and collaborators](#teams-and-collaborators)
  - [Setting up GitHub web links](#setting-up-github-web-links)
  - [Viewing git commits in Jira Cloud](#viewing-git-commits-in-jira-cloud)
  - [Working with branches and pull requests with GitHub](#working-with-branches-and-pull-requests-with-github)
    - [Default Branch](#default-branch)
    - [Creating branches](#creating-branches)
    - [Creating pull requests](#creating-pull-requests)
  - [More Integration Guides](#more-integration-guides)

&nbsp;
<hr>
&nbsp;

## Creating a personal access token

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If two-factor authentication is enabled for your GitHub account, you will need to create a personal access token (PAT) to access your git repositories. Enable two-factor authentication in your GitHub.com account for increased security.
    </div>
    </div>
</div>
<br>

While instructions from GitHub works just fine, please [follow this article](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) for a quick step-by-step guide to get you started.

## Using Git service integration

This process requires an existing GitHub git repository. A GitHub account with enabled two-factor authentication and configured personal access token is encouraged.

We recommend using the **Git service integration** panel to connect multiple repositories from your GitHub.com account.

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        On November 13, 2020, GitHub.com is going to stop allowing API authentication via username/password. For more information, see <a href='https://developer.github.com/changes/2020-02-14-deprecating-password-auth/' target='_blank'><b>GitHub.com - Deprecating Password Authentication</b></a>.<br>
        <p style='margin-bottom:-10px !important'>We strongly recommend to use personal access tokens for GitHub.com account integration.</p>
    </div>
    </div>
</div>
<br>

1.  On your Jira side bar, go to Apps ➜ **Git Integration for Jira**, then **Settings** ➜ **Manage Integrations**

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c-2025.png)

2.  On the Manage integrations page, click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-2025.png)

3.  For the following screen, click **GitHub.com** to start integration with this git service.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-type-github-2025.png)

4.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-github-integration-oauth-01-2025.png)

5.  For this guide, click on the **OAuth integration** to select it.

    *   We recommend the OAuth integration which is outlined like a setup wizard -- making it more easier for users to connect GitHub integrations.

    *   For PAT integration, however, uses personal access tokens to setup GitHub integrations. Users will have to configure their own PAT from GitHub to use for this setup.

    *   For GitHub webhook indexing integration, see [this article](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud) instead.

    *   Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed.

        ![](/wp-content/uploads/gij-gitcloud-integration-advanced-options-wo-sslverify-c.png)

        *   **Custom API Path**  –  this is a relative path that starts with "/". The integration will use the relative REST API path to retrieve the list of tracked repositories. The maximum allowed length is **2000** characters or less.

            To learn more examples, see article [Jira Cloud: Working with Custom API Path](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

        *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is **2000** characters or less.
            
            Read about JMESPath expressions on their [website](http://jmespath.org/). For help with writing expressions, please contact [support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

            To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

    *   While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

6.  Click **Connect to GitHub.com** to proceed to the next step.

7.  **Login to your GitHub account when prompted.** When connecting to your GitHub.com account using OAuth for the first time, the user will be presented with a grant authorization screen.

    ![](/wp-content/uploads/gij-github-autoconnect-grant-auth-screen-c.png)

    *   Grant organization access to an org to also have its repositories listed in the Manage repositories page.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> If access is not granted, the repositories within those organizations (and even the orgs themselves) will not show up in the Git Integration for Jira app repositories list. The only way to see these repos/orgs is to return to the GitHub web portal using admin interface and specifically grant such permissions (Profile settings ➜ Developer settings ➜ **OAuth Apps**).

    *   Below are the differences between the three authentication options for GitHub:

        ```java
        Authentication Method       When are org repositories connected?
        ----------------------------------------------------------------------------
        OAuth                       User should notice and press the "Grant" button
                                    near the org repositories to connect them.
        ----------------------------------------------------------------------------
        PAT                         Org repositories are connected immediately.
        ----------------------------------------------------------------------------
        Username/Password           Org repositories are connected immediately.
        ```

    *   Click **Authorize BigBrassBand** to continue.

8.  The following page is displayed.

    ![](/wp-content/uploads/gij-gitcloud-github-integration-oauth-sel-repos-c.png)

    *   The Git Integration for Jira app will read all available repositories from your GitHub account. Repositories of the logged-in GitHub user can be automatically connected to Jira Cloud. Repositories that are added or removed from GitHub will be likewise connected or disconnected from Jira Cloud.

    *   Use the search options to filter displayed repositories for the current screen.

    *   Connect all repositories and organizations or select specific repositories to connect for this integration.

9.  Click **Connect repositories** to complete this setup.


The GitHub.com repositories are now connected to Jira Cloud. There will be a slight delay in adding 2FA-enabled repositories compared to others. These will show in the git configuration list eventually.

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

This process requires an existing GitHub git repository. Look for the the GitHub repository URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the GitHub git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

[Single git repository integration (SSH)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-ssh-gij-cloud)

## Setting up GitHub permissions

We recommend using a "service user" in GitHub _(example: "Git-Integration-for-Jira")_ to be used to integrate GitHub with the Git Integration for Jira app. This dedicated "service user" will allow the GitHub administrator to set permissions so the app clones only the desired repositories.

Assign GitHub permissions for team members or collaborators to allow which resources are accessible for service users. This feature is only available in a GitHub Organization.

### Default repository permission

1.  Login to your GitHub.com account.

2.  Go to <img src='/wp-content/uploads/gij-profile-icon.png' /> Profile ➜ **Settings**.

3.  On your sidebar, click **Organizations**.

4.  Click **Settings** for the selected organization.

5.  On your sidebar, click **Member Privileges**. The following screen is displayed.

    ![](/wp-content/uploads/gij-github-org-repo-base-permissions-c.png)

6.  Under the **Base permissions**, click on the dropdown button.

    *   Choose the base permission level for organization members. The base repository permission only applies to organization members and not to outside collaborators. If the base permission is set to _**None**_, organization members will need to be given access to repositories using the _**Teams or Collaborators**_ methods (see below).

7.  **Save** the changes.

<div style='margin:25px 0 20px 0'>
    For more information, see <a href='https://help.github.com/articles/access-permissions-on-github/'><b>Access Permissions on GitHub »</b></a>.
</div>

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

    The service user is then added to the team if the invitation has been accepted.

3.  Click the service user to manage permissions for this member to:

    *   Set desired Role for this member.

    *   Convert this member to outside collaborator.

    *   Give this member access to organization repositories.

    *   Remove this member from the team.

4.  Click **Manage access** to manage repository access for this member.

    ![](/wp-content/uploads/gij-github-manage-team-repo-permission-c.png)

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Organization Permissions</b><br>
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
        For collaborators and commit authors, set these users to have **Write** permissions. This will allow them to view commits and smart commits, browse repositories and also enables them to create branches and pull requests to specified GitHub git repositories via developer panel of a Jira issue.
    </div>
    </div>
</div>
<br>

For more information on organization teams, see [**GitHub: Organizing Members into Teams »**](https://help.github.com/articles/organizing-members-into-teams/).

For more information on inviting collaborators, see [**Inviting Collaborators to a Personal/Organization Repository »**](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/).

## Setting up GitHub web links

The Git Integration for Jira app automatically configures web linking for GitHub git repositories.

For single repository connections, web link setup is optional. However, git links will become available in Git Commits tab when configured.

For more information on this feature, see [Documentation: Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud).

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This action will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue in your Jira instance.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Working with branches and pull requests with GitHub

The Git Integration for Jira Cloud app adds two features on the Jira issue developer panel – Create Branch, and Create Pull/Merge Request. For more information about the developer panel, see the [Jira Git integration development panel](/git-integration-for-jira-cloud/jira-issue-page-gij-cloud#jira-git-integration-development-panel) documentation.

This process requires a GitHub git repository and a PAT with `repo` scopes.

For GitHub Organization, the user must have the **Write** permissions and the `repo` PAT scopes.

### Default Branch

Most git integrations allow changing of the default branch of the repository/project other than "master". This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Git service integrations support this function where the default branch is acquired from almost all integrations and apply this setting at repository level. 

### Creating branches

On your Jira Cloud, open a Jira issue. On the [Jira Git integration development panel](/git-integration-for-jira-cloud/jira-issue-page-gij-cloud#jira-git-integration-development-panel), click **Open Git Integration** then click **Create branch**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-issue-dev-panel-create-branch-dlg.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the User settings page.

2.  Choose a **Source branch**.

    <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

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

The newly-created branch is now listed in the Jira developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

### Creating pull requests

The pull request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Open Git Integration**, click **Create pull request**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-issue-dev-panel-create-pull-req-dlg.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    4.  <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

2.  Choose the newly-created branch as the **Source branch**.
   
   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>&nbsp; Designate the branch to be the default selected branch for the currently selected repository. To configure default pull requests for more than one repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.

5.  Click **Create pull request** to complete this process. Follow the link to the PR to setup for review and approval.

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
<br>

The pull request is listed on the developer panel of the Jira issue page.

The pull request is also ready for approval by the reviewers in your GitHub web portal.

&nbsp;

## More Integration Guides

**GitHub.com** (this page)

[GitLab CE/EE](/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud) (Git Integration for Jira Cloud)

[GitHub Enterprise Server](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud) (Git Integration for Jira Cloud)

[GitLab.com](/git-integration-for-jira-cloud/gitlab-com-gij-cloud) (Git Integration for Jira Cloud)

[Azure DevOps \| Visual Studio Team Services (VSTS)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud) (Git Integration for Jira Cloud)

[Azure DevOps Server \| Team Foundation Services (TFS)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud) (Git Integration for Jira Cloud)

[AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommmit-gij-cloud) (Git Integration for Jira Cloud)

[Gerrit](/git-integration-for-jira-cloud/gerrit-gij-cloud) (Git Integration for Jira Cloud)

[Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-cloud-gij-cloud) (Git Integration for Jira Cloud)

[Introduction to Git integration](/git-integration-for-jira-cloud/integration-guide-gij-cloud) (Git Integration for Jira Cloud)

