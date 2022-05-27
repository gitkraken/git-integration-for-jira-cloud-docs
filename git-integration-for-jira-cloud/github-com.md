---

title: GitHub.com
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
These instructions apply to instances on Free, Team, Cloud Enterprise (including [**EMU**](https://docs.github.com/en/enterprise-cloud@latest/admin/identity-and-access-management/managing-iam-with-enterprise-managed-users/about-enterprise-managed-users)) plans hosted on GitHub.com.

For instructions on self-hosted GitHub Enterprise Server, please see [this page](#).

Using **Jira Server or Data Center**?  [See the corresponding article](https://bigbrassband.atlassian.net/wiki/x/igBNAw).

![GitHub Banner logo](https://bigbrassband.com/confluence/images/github-logo.svg)

# Integrate GitHub.com with Jira Cloud

Quickly learn how to connect GitHub.com git repositories via Git Integration for Jira Cloud app.

**What's on this page:**

* * *

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/8jtnqzp79y) _and open this video in a new window/tab for more viewing options._
_(Updated video coming soon)_

## Creating a personal access token

If two-factor authentication is enabled for your GitHub account, you will need to create a personal access token (PAT) to access your git repositories. Enable two-factor authentication in your GitHub.com account for increased security.

While instructions from GitHub works just fine, please [follow this article](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens#CreatingPersonalAccessTokens-github) for a quick step-by-step guide to get you started.

## Using Git service integration

This process requires an existing GitHub git repository. A GitHub account with enabled two-factor authentication and configured personal access token is encouraged.

We recommend using the **Git service integration** panel to connect multiple repositories from your GitHub.com account.

On November 13, 2020, GitHub.com is going to stop allowing API authentication via username/password. For more information, see [**GitHub.com - Deprecating Password Authentication**](https://developer.github.com/changes/2020-02-14-deprecating-password-auth/).

We strongly recommend to use personal access tokens for GitHub.com account integration.

1.  On your Jira dashboard menu, go to **Apps** ➜ **Git Integration: Manage integrations**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/82477058/gitcloud-jira-apps-manage-integrations-sel(c).png?version=2&modificationDate=1648642830446&cacheVersion=1&api=v2)

2.  On the Manage integrations page, click **Add integration.**

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/82477058/gitcloud-managed-ui-webhook-idx-setup(c).png?version=2&modificationDate=1648642957396&cacheVersion=1&api=v2&width=646&height=378)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/82477058/gitcloud-managed-ui-git-service-sel(c).png?version=1&modificationDate=1649313462074&cacheVersion=1&api=v2)

4.  Select **GitHub.com** from the list then click **Connect …** 

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/82477058/gitcloud-github-integration-sel-service(c).png?version=1&modificationDate=1649150967182&cacheVersion=1&api=v2)
    1.  Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/82477058/gitcloud-integration-advanced-options-wo-sslverify(c).png?version=1&modificationDate=1649313273881&cacheVersion=1&api=v2&width=510&height=266)
        *   **Custom API Path**  –  his is a relative path that starts with "/". The integration will use the relative REST API path to retrieve the list of tracked repositories. The maximum allowed length is 2000 characters or less.
            To learn more examples, see article [Jira Cloud: Working with Custom API Path](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/133201972/Working+with+Custom+API+Path).

        *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is 2000 characters or less.
            Read about JMESPath expressions on their [website](http://jmespath.org/). For help with writing expressions, please contact [support](mailto:support@bigbrassband.com).
            To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/133234759/Working+with+JMESPath+Filters).

    2.  While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

5.  **Login to your GitHub account when prompted.** When connecting to GitHub.com using OAuth for the first time, the user will be presented with a grant authorization screen.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/82477058/github-autoconnect-grant-auth-screen(c).png?version=1&modificationDate=1600060492750&cacheVersion=1&api=v2)
    *   Grant organization access to an org to also have its repositories listed in the Manage repositories page.

    *   Below are the differences between the three authentication options for GitHub:

        ```java
        Authentication Method       When are org repositories connected?
        ----------------------------------------------------------------------------
        OAuth                       User should notice and press the "Grant" button
                                    near the org repositories to connect them.

        PAT                         Org repositories are connected immediately.

        Username/Password           Org repositories are connected immediately.
        ```

    *   Click **Authorize** **BigBrassBand** to continue.

6.  The following page is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/82477058/gitcloud-github-integration-oauth-sel-repos(c).png?version=1&modificationDate=1649152763376&cacheVersion=1&api=v2&width=612&height=358)
    1.  The Git Integration for Jira app will read all available repositories from your GitHub account.
        Repositories of the logged-in GitHub user can be automatically connected to Jira Cloud. Repositories that are added or removed from GitHub will be likewise connected or disconnected from Jira Cloud.

    2.  Use the search options to filter displayed repositories for the current screen.

    3.  Connect all repositories and organizations or select specific repositories to connect for this integration.

7.  Click **Connect repositories** to complete this setup.


The GitHub.com repositories are now connected to Jira Cloud. There will be a slight delay in adding 2FA-enabled repositories compared to others. These will show in the git configuration list eventually.

## Single git repository integration

This section is for users who are using SSH connections or those who wanted to only connect a single specific repository.

This process requires an existing GitHub git repository. Look for the the GitHub repository URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the GitHub git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https/)

[Single git repository integration (SSH)](/wiki/spaces/GITCLOUD/pages/923238489)

## Setting up GitHub permissions

We recommend using a "service user" in GitHub _(example: "Git-Integration-for-Jira")_ to be used to integrate GitHub with the Git Integration for Jira app. This dedicated "service user" will allow the GitHub administrator to set permissions so the app clones only the desired repositories.

Assign GitHub permissions for team members or collaborators to allow which resources are accessible for service users. This feature is only available in a GitHub Organization.

### Default repository permission

1.  Login to your GitHub.com account.

2.  Go to ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Profile** ➜ **Settings**.

3.  On your sidebar, click **Organizations**.

4.  Click **Settings** for the selected organization.

5.  On your sidebar, click **Member Privileges**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/82477058/github-org-repo-base-permissions(c).png?version=1&modificationDate=1597238662574&cacheVersion=1&api=v2)
6.  Under the **Base permissions**, click on the dropdown button.

    *   Choose the base permission level for organization members. The base repository permission only applies to organization members and not to outside collaborators. If the base permission is set to _**None**_, organization members will need to be given access to repositories using the _**Teams or Collaborators**_ methods (see below).

7.  **Save** the changes.


For more information, see [**Access Permissions on GitHub »**](https://help.github.com/articles/access-permissions-on-github/).

### Teams and collaborators

To give a member additional access, they must be added to a team or make them collaborators on individual repos.

**Set default repository permission for the current team:**

1.  Open an organization team. (_Your org ➜ Teams ➜ scroll down to the bottom then click the desired team._)

2.  Click the **Repositories** tab.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/82477058/github-org-repo-team-repo-permissions(c).png?version=1&modificationDate=1597238663935&cacheVersion=1&api=v2)
3.  Set **Read**, **Write** or **Admin** repository access as desired.



**Assign members to a team on your GitHub repository:**

1.  Create a team in your GitHub Organization.

2.  Invite a member to add it into the team. An email invitation is sent to that GitHub service user.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/82477058/github-add-members-to-team(c).png?version=1&modificationDate=1597238664762&cacheVersion=1&api=v2)

    The service user is then added to the team if the invitation has been accepted.

3.  Click the service user to manage permissions for this member to:

    *   Set desired Role for this member.

    *   Convert this member to outside collaborator.

    *   Give this member access to organization repositories.

    *   Remove this member from the team.

4.  Click **Manage access** to manage repository access for this member.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/82477058/github-manage-team-repo-permission(c).png?version=1&modificationDate=1597238665239&cacheVersion=1&api=v2)

**Organization Permissions**
While users have configured PAT for repository access, users in a GitHub Organization must at least have **Read** permissions. This allows them to view commits and smart commits (if enabled) of connected GitHub Organization repositories inside Jira.

**GitHub Organization**
For collaborators and commit authors, set these users to have **Write** permissions. This will allow them to view commits and smart commits, browse repositories and also enables them to create branches and pull requests to specified GitHub git repositories via developer panel of a Jira issue.

For more information on organization teams, see [**GitHub: Organizing Members into Teams »**](https://help.github.com/articles/organizing-members-into-teams/).

For more information on inviting collaborators, see [**Inviting Collaborators to a Personal/Organization Repository »**](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/).

## Setting up GitHub web links

The Git Integration for Jira app automatically configures web linking for GitHub git repositories.

For single repository connections, web link setup is optional. However, git links will become available in Git Commits tab when configured.

For more information on this feature, see [Documentation: Web linking](/git-integration-for-jira-cloud/Web-linking).

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This action will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue in your Jira instance.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](/wiki/spaces/GITCLOUD/pages/1923025229/Linking+git+commits+to+Jira+issues).

## Working with branches and pull requests with GitHub

This process requires a GitHub git repository and a PAT with `repo` scopes.

For GitHub Organization, the user must have the **Write** permissions and the `repo` PAT scopes.

### Creating branches

On your Jira Cloud, open a Jira issue. On the Jira Git integration development panel, click **Open Git Integration** then click **Create branch**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/82477058/gitcloud-issue-dev-panel-create-branch-dlg.png?version=2&modificationDate=1649154037835&cacheVersion=1&api=v2&width=680&height=243)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the User settings page.

2.  Choose a **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](#) page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  Click **Create branch** to complete this process.


For more detailed information on this feature, see [Create branch](/git-integration-for-jira-cloud/Create-branch).


The newly-created branch is now listed in the Jira developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

### Creating pull requests

The pull request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Open** **Git Integration**, click **Create pull request**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/82477058/gitcloud-issue-dev-panel-create-pull-req-dlg.png?version=1&modificationDate=1649154519995&cacheVersion=1&api=v2&width=680&height=262)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](#) page.

2.  Choose the newly-created branch as the **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](#) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.

5.  Click **Create pull request** to complete this process. Follow the link to the PR to setup for review and approval.


Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.

**Preview** allows you to see the comparison view of the current changes in the selected **Source branch** vs **Target branch** (_usually_ _master_).

For more detailed information on this feature, see [Create pull/merge request](/wiki/spaces/GITCLOUD/pages/733315235/Create+pull+or+merge+request).


The pull request is listed on the developer panel of the Jira issue page.

The pull request is also ready for approval by the reviewers in your GitHub web portal.

