---

title: GitHub Enterprise Server
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
These instructions apply to self-hosted GitHub Enterprise Server.

For instructions to instances hosted on GitHub.com (Free, Team, Enterprise (including [**EMU**](https://docs.github.com/en/enterprise-cloud@latest/admin/identity-and-access-management/managing-iam-with-enterprise-managed-users/about-enterprise-managed-users)) plans), please go to [this page](/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com).

Using **Jira Server or Data Center**? [See the corresponding article](https://bigbrassband.atlassian.net/wiki/x/E4FMAw).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622870/github-ent-server-banner-logo.png?version=1&modificationDate=1646820087185&cacheVersion=1&api=v2&width=510&height=59)

# Integrate GitHub Enterprise Server with Jira Cloud

Quickly learn how to connect GitHub Enterprise Server git repositories via Git Integration for Jira Cloud.

**What's on this page:**

* * *

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/vfwwqnn3mm) _and open this video in a new tab/window for more viewing options._
(_Updated video coming soon_)

## Creating a personal access token

If two-factor authentication is enabled for your GitHub Enterprise Server account, you will need to create a personal access token (PAT) to access your git repositories. Enable two-factor authentication in your GitHub Enterprise Server account for increased security.

While instructions from GitHub works just fine, [follow this article](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens#CreatingPersonalAccessTokens-github) for a quick step-by-step guide to get you started.

## Using Git service integration

This process requires an existing GitHub Enterprise Server account. 

We recommend using the **Git service integration** panel to connect multiple repositories from your GitHub Enterprise Server account.

1.  On your Jira Cloud dashboard menu, go to **Apps ➜ Git Integration: Manage integrations**.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622870/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1649154910071&cacheVersion=1&api=v2&width=646&height=378)

2.  On the Manage integrations page, click **Add integration.**

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622870/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1649154918082&cacheVersion=1&api=v2)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622870/gitcloud-managed-ui-git-service-sel(c).png?version=1&modificationDate=1649155243812&cacheVersion=1&api=v2)

4.  The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622870/gitcloud-integration-ghe-server-connect-service(c).png?version=1&modificationDate=1649307736168&cacheVersion=1&api=v2)
    1.  Select **GitHub Enterprise Server (self-managed)** from the Git hosting service drop down list.

    2.  For the **Host URL**, enter the address of the GitHub Enterprise Server.

    3.  For admins/owners, repository managers, collaborators or users that have enabled 2FA, enter username to the **Login** field and enter the PAT on the **Token** field.

5.  Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622870/gitcloud-integration-advanced-options-std(c).png?version=1&modificationDate=1649311626794&cacheVersion=1&api=v2&width=476&height=301)
    1.  **SSL Verify** – The **SSL Verify** option is set to `Enabled` by default. If set to `Disabled`, the Git Integration for Jira Cloud app will ignore verification of SSL certificates when connecting to a git server. _This option is not available for non-fetched repositories._

    2.  **Custom API Path**  –  this is a relative path that starts with "/". The maximum allowed length is 2000 characters or less. The integration will use the relative REST API path to retrieve the list of tracked repositories.
        To learn more examples, see article [Jira Cloud: Working with Custom API Path](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/133201972/Working+with+Custom+API+Path).

    3.  **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is 2000 characters or less.
        Read about JMESPath expressions on their [website](http://jmespath.org/). For help with writing expressions, please contact [support](mailto:support@bigbrassband.com).
        To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/133234759/Working+with+JMESPath+Filters).

    4.  While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

6.  Click **Connect and select repositories**. The Git Integration for Jira app will read all available repositories from your GitHub Enterprise Server account.

7.  The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622870/gitcloud-integration-ghe-server-repo-sel(c).png?version=1&modificationDate=1649314456645&cacheVersion=1&api=v2)
    *   Repositories that are added or removed from GitHub will be likewise connected or disconnected from Jira Cloud.

    *   Use the search options to filter displayed repositories for the current screen.

    *   Connect all repositories and organizations or select specific repositories to connect for this integration.

8.  Click **Connect** **repositories** to complete the setup.


GitHub Enterprise Server repositories are now connected to Jira Cloud.

## Single git repository integration

This section is for users who are using SSH connections or those who wanted to only connect a single specific repository.

This process requires an existing GitHub Enterprise Server git repository. Look for the the repository clone URL on the repository project page.

Use this information to connect the GitHub git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/wiki/spaces/GITCLOUD/pages/923238448)

## Setting up GitHub Enterprise Server permissions

We recommend using a "service user" in GitHub Enterprise Server _(example: "GitIntegrationforJira")_ to be used to integrate with Git Integration for Jira app. This dedicated "service user" will allow the GitHub Enterprise Server administrator to set permissions so the app clones only the desired repositories.

Assign GitHub Enterprise Server permissions for team members or collaborators to allow which resources are accessible for service users. This feature is only available in a GitHub Organization.

### Default repository permission

1.  Login to your GitHub Enterprise Server account.

2.  Go to ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Profile** ➜ **Settings**.

3.  On your sidebar, click **Organizations**.

4.  Click **Settings** for the selected organization.

5.  On your sidebar, click **Member Privileges**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622870/github-org-repo-base-permissions(c).png?version=1&modificationDate=1597322225784&cacheVersion=1&api=v2)
6.  Under the **Base permissions**, click on the dropdown button.

    *   Choose the base permission level for organization members. The base repository permission only applies to organization members and not to outside collaborators. If the base permission is set to _**None**_, organization members will need to be given access to repositories using the _**Teams or Collaborators**_ methods (see below).

7.  **Save** the changes.


For more information, see [**Access Permissions on GitHub »**](https://help.github.com/articles/access-permissions-on-github/).

### Teams and collaborators

To give a member additional access, they must be added to a team or make them collaborators on individual repos.

**Set default repository permission for the current team:**

1.  Open an organization team. (_Your org ➜ Teams ➜ scroll down to the bottom then click the desired team._)

2.  Click the **Repositories** tab.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622870/github-ent-org-repo-team-repo-permissions(c).png?version=1&modificationDate=1597322226657&cacheVersion=1&api=v2)
3.  Set **Read**, **Write** or **Admin** repository access as desired.


**Assign members to a team on your GitHub repository:**

1.  Create a team in your GitHub Organization.

2.  Invite a member to add it into the team. An email invitation is sent to that GitHub service user.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622870/github-add-members-to-team(c).png?version=1&modificationDate=1597322227306&cacheVersion=1&api=v2)
    *   The service user is then added to the team if the invitation has been accepted.

3.  Click the service user to manage permissions for this member to:

    1.  Set desired Role for this member.

    2.  Convert this member to outside collaborator.

    3.  Give this member access to organization repositories.

    4.  Remove this member from the team.

4.  Click **Manage access** to manage repository access for this member.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622870/github-manage-team-repo-permission(c).png?version=1&modificationDate=1597322228490&cacheVersion=1&api=v2)

**Organization Permissions**
While users have configured PAT for repository access, users in a GitHub Organization must at least have **Read** permissions. This allows them to view commits and smart commits (if enabled) of connected GitHub Organization repositories inside Jira.

**GitHub Organization**
For collaborators and commit authors, set these users to have **Write** permissions. This will allow them to view commits and smart commits, browse repositories and also enables them to create branches and pull requests to specified GitHub git repositories via developer panel of a Jira issue.

For more information on organization teams, see [**GitHub: Organizing Members into Teams »**](https://help.github.com/articles/organizing-members-into-teams/).

For more information on inviting collaborators, see [**Inviting Collaborators to a Personal/Organization Repository »**](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/).

## Setting up GitHub web links

The Git Integration for Jira app automatically configures web linking for GitHub Enterprise Server git repositories.

For single repository connections, web link setup is optional. However, git links will become available in Git Commits tab when configured.

For more information on this feature, see [Documentation: Web linking](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025184).

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This action will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View Full Commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025229).

## Working with branches and pull requests with GitHub Enterprise Server

This process requires a GitHub Enterprise Server git repository and a PAT with `repo` scopes.

For GitHub Organization, the user must have the **Write** permissions and the `repo` PAT scopes.

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level.

Main branch for repositories within an integration can only be changed on the git server.

### Creating branches

On your Jira Cloud, open a Jira issue. On the Jira Git integration development panel, click **Open** **Git Integration** then click **Create branch**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622870/gitcloud-issue-dev-panel-create-branch-dlg.png?version=1&modificationDate=1649316489253&cacheVersion=1&api=v2&width=680&height=243)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/User-Settings) page.

2.  Choose a **Base branch**. OPTIONAL Designate the branch to be the default selected branch for the active repository. To configure default branches for more than one repository - use the [User settings](#) page.

3.  Enter a **Branch name** or leave it as is (recommended).


For more detailed information on this feature, see [Create branch](/git-integration-for-jira-cloud/Create-branch).

The newly-created branch is now listed in the developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

### Creating pull requests

The pull request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Git Integration**, click **Create pull request**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622870/gitcloud-issue-dev-panel-create-pull-req-dlg.png?version=1&modificationDate=1649320516984&cacheVersion=1&api=v2&width=680&height=262)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](#) page.

2.  Choose the newly-created branch as the **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the active repository. To configure default branches for more than one repository - use the [User settings](#) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.


Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.

**Preview** allows you to see the comparison view of the current changes in the selected **Source branch** vs **Target branch** (_usually_ _master_).

For more detailed information on this feature, see [Create pull/merge request](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/733315235).


The pull request is listed on the developer panel of the Jira issue page.

The pull request is also ready for approval by the reviewers in your GitHub web portal.

## More Integration Guides

*   Page:

    [GitHub.com](/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com) (Git Integration for Jira Cloud)

*   Page:

    [GitLab CE/EE](/wiki/spaces/GITCLOUD/pages/85524528) (Git Integration for Jira Cloud)

*   Page:

    [GitHub Enterprise Server](/wiki/spaces/GITCLOUD/pages/85622870/GitHub+Enterprise+Server) (Git Integration for Jira Cloud)

*   Page:

    [GitLab.com](/wiki/spaces/GITCLOUD/pages/85622895/GitLab.com) (Git Integration for Jira Cloud)

*   Page:

    [Azure DevOps | Visual Studio Team Services (VSTS)](/wiki/spaces/GITCLOUD/pages/86278279) (Git Integration for Jira Cloud)

*   Page:

    [Azure DevOps Server | Team Foundation Services (TFS)](/wiki/spaces/GITCLOUD/pages/86409345) (Git Integration for Jira Cloud)

*   Page:

    [AWS CodeCommit](/git-integration-for-jira-cloud/AWS-CodeCommit) (Git Integration for Jira Cloud)

*   Page:

    [Gerrit](/git-integration-for-jira-cloud/Gerrit) (Git Integration for Jira Cloud)

*   Page:

    [Bitbucket Cloud](/git-integration-for-jira-cloud/Bitbucket-Cloud) (Git Integration for Jira Cloud)

*   Page:

    [Introduction to Git integration](/wiki/spaces/GITCLOUD/pages/86966273/Introduction+to+Git+integration) (Git Integration for Jira Cloud)