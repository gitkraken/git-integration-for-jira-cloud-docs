---

title: GitLab.com
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Using **Jira Server or Data Center**? [See the corresponding article](https://bigbrassband.atlassian.net/wiki/x/iABMAw).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622895/gitlab_wm_no_bg.png?version=1&modificationDate=1597499071261&cacheVersion=1&api=v2&width=224&height=84)

# Integrate GitLab.com with Jira Cloud

GitLab introduced personal access tokens (PAT) since version 8.8 and now (v10+) prefers this type of authentication for accessing the git repositories.  Service users are strongly advised to switch from using username/password to using Personal Access Tokens (PAT) for GitLab.com.

Support for Gitlab API v3 is deprecated. We recommend to use **GitLab API v4** when adding new integrations for increased security.


Quickly learn how to connect GitLab.com git repositories via Git Integration for Jira Cloud app.

**What's on this page:**

* * *

_Right click_ [_**here**_](https://bigbrassband.wisita.com/medias/hi45vum4yp) _and open this video in a new tab/window for more viewing options._
_(Updated video coming soon)_

## Permissions

GitLab can have users with different access level to a group or project. If the user's connected GitLab repositories to Jira are not accessible or commits are not showing for that user -- it's related to permission issues. This can be a per user, repository or a project level restriction.

If you encounter access permission issues, you will need to ask your Git administrator to grant you the required level of access to specific projects. If you are a Git administrator, you will need to setup a GitLab user with the minimum required permissions to view GitLab projects from Jira.

Take the following cases for example:

*   The personal access token (PAT) that the GitLab user provided doesn't have the correct permissions within GitLab to view source code for specific repositories.

*   The GitLab user doesn't have access privileges to a GitLab repository or is not a member of a group that has access to specific repositories.


We recommend creating a specific GitLab user for the integration. This way, the GitLab user can have specific permissions to do the given tasks.

![gitlab user permissions or repository permissions](https://bigbrassband.atlassian.net/wiki/download/attachments/85622895/image-20200815-075633.png?version=1&modificationDate=1597499071968&cacheVersion=1&api=v2)

**For minimum access (read-only) permissions:**

1.  Set the user account profile's PAT scope to `read_repository`.

2.  The GitLab user is set to only **read** a specific repository. Set to **Reporter** role.


This level of access allows the user to view commits for the specific repository.

**For users who will be tasked with creating branches and merge requests:**

1.  Set the user account profile's PAT scope to `api`.

2.  The GitLab user should be set to **read/write** access for the specific repository. Set to **Developer** role.


This level of access allows the user to create/delete branches and create merge requests.

For more information, see [**GitLab Permissions »**](https://docs.gitlab.com/ee/user/permissions.html).

## Creating a personal access token

If two-factor authentication is enabled for your GitLab account, you will need to create a personal access token (PAT) to access your git repositories. Enable two-factor authentication in your GitLab.com account for increased security.

While instructions from GitHub works just fine, [follow this article](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens#CreatingPersonalAccessTokens-gitlab) for a quick step-by-step guide to get you started.

## Using Git service integration

This process requires an existing GitLab.com account. Multiple git repositories in a GitLab.com account will be connected via Git Integration for Jira Cloud app.

While instructions from GitLab works just fine, here are some specific instructions to get you up and running.

We recommend using the Git service integration panel[1](#logo) to connect multiple repositories from your GitLab.com account.

1.  On your Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622895/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1649322898452&cacheVersion=1&api=v2)

2.  On the Manage integrations page, click **Add integration.**

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622895/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1649322743497&cacheVersion=1&api=v2)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622895/gitcloud-managed-ui-git-service-sel(c).png?version=2&modificationDate=1649322811881&cacheVersion=1&api=v2&width=652&height=382)

4.  The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622895/gitcloud-integration-gitlab-service-sel(c).png?version=1&modificationDate=1649326068539&cacheVersion=1&api=v2)
    1.  Select **GitLab.com** from the Git hosting service dropdown list.

    2.  Enter the PAT on the provided field.

    3.  Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed. These settings are used with integration to retrieve the list of tracked repositories. Set a filter that will only load some cloned repositories which can be viewed in the Manage repositories page.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622895/gitcloud-integration-advanced-options-wo-sslverify(c).png?version=1&modificationDate=1649327432387&cacheVersion=1&api=v2&width=533&height=279)
        *   **Custom API Path**  –  this is a relative path that starts with "/". The maximum allowed length is 2000 characters or less. The integration will use the relative REST API path to retrieve the list of tracked repositories.
            For more information on GitLab custom API paths, see [GitLab API](https://docs.gitlab.com/ee/api/projects.html).
            For more examples, see article [Jira Cloud: Working with Custom API Path](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/133201972/Working+with+Custom+API+Path).

            ```java
            GitLab version API support:

            Gitlab v8.16 and earlier -- API v3.
            Gitlab v8.17 to v8.xx -- API v3. 
            Gitlab v9.0 to v9.4.x -- API v3 and API v4.
            Gitlab v9.5 and above -- only API v4.
            ```

            *   ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Remember:**
                The GitLab.com API can see all the public projects. For GitLab.com, we recommend using JMESPath over the Custom API path when possible.

        *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is 2000 characters or less.
            Read about JMESPath expressions on their [website](http://jmespath.org/). For help with writing expressions, please contact [support](mailto:support@bigbrassband.com).
            To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/133234759/Working+with+JMESPath+Filters).

    4.  While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

5.  Click **Connect and select repositories** to proceed.

6.  On the following screen, the Git Integration for Jira app will read all available repositories from your GitLab account.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85622895/gitcloud-integration-gitlab-repo-sel(c).png?version=1&modificationDate=1649327825946&cacheVersion=1&api=v2)
    1.  Repositories of the logged-in GitLab user can be automatically connected to Jira Cloud. Repositories that are added or removed from GitLab will be likewise connected or disconnected from Jira Cloud.

    2.  Use the search options to filter displayed repositories for the current screen.

    3.  Connect all repositories and organizations or select specific repositories to connect for this integration.

7.  Click **Connect repositories** to complete this setup.


The GitLab.com git repositories are now connected to Jira Cloud.

There will be a slight delay in adding 2FA-enabled repositories compared to others. These will show in the git configuration list eventually.

**Administrators**
If you need to require users PAT for creating branches or merge requests, turn on this setting via the selected integration in Manage integrations page ➜ ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Edit integration** ➜ Feature settings.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622895/gitcloud-edit-integration-feature-cfg-req-user-PAT.png?version=1&modificationDate=1649328090252&cacheVersion=1&api=v2&width=680&height=75)

## Single git repository integration

This process requires an existing GitLab git repository. Look for the the GitLab repository clone URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the GitLab git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https/)

[Single git repository integration (SSH)](/wiki/spaces/GITCLOUD/pages/923238489)

There will be a slight delay in adding 2FA-enabled repositories compared to others. These will show in the git configuration list eventually.

In order to access a Git repository over HTTP, use the username as the username and the PAT for the password.

## Setting up GitLab web links

The Git Integration for Jira app automatically configures web linking for GitLab git repositories.

For single repository connections, web link setup is optional. However, git links will become available in Git Commits tab when configured.

For more information on this feature, see [Documentation: Web linking](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025184).

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This action will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue on your Jira instance.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025229).

## Working with branches and merge requests with GitLab

This process requires a GitLab git repository and a PAT with `api` scope.

For GitLab Group, the user must have the **Write** permissions and the `api` PAT scope.

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level.

Main branch for repositories within an integration can only be changed on the git server.

### Creating branches

On your Jira Cloud instance, open a Jira issue. On the Jira Git integration development panel, click **Open Git integration** then click **Create branch**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622895/gitcloud-gitlab-com-dev-panel-create-branch-dlg.png?version=1&modificationDate=1649691715930&cacheVersion=1&api=v2&width=680&height=221)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab owner name. For example, `johnsmith/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/User-Settings) page.

2.  Choose a **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one connected repository - use the [User settings](#) page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  Click **Create branch** to complete this process.


For more detailed information on this feature, see [Create branch](/git-integration-for-jira-cloud/Create-branch).


The newly-created branch is now listed in the developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

### Creating merge requests

The merge request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the Jira Git integration development panel, click **Open Git integration** then click **Create merge request**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85622895/gitcloud-gitlab-com-dev-panel-create-mergereq-dlg.png?version=1&modificationDate=1649691857389&cacheVersion=1&api=v2&width=680&height=240)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab group name. For example, `BigBrassBand/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](#) page.

2.  Choose the newly-created branch as the **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one connected repository - use the [User settings](#) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.

5.  Click **Create pull request** to complete this process. Follow the link to the PR to setup for review and approval.


Merge requests are still indexed based on branch name even if the MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.

**Preview** allows you to see the comparison view of the current changes in the selected **Source branch** vs **Target branch** (_usually_ _master_).

For more detailed information on this feature, see [Create pull/merge request](/wiki/spaces/GITCLOUD/pages/733315235/Create+pull+or+merge+request).


The merge request is listed on the developer panel of the Jira issue page.

The merge request is also ready for approval by the reviewers in your GitLab web portal.



_1 Logo owned by_ [_GitLab Inc_](https://gitlab.com/) _used under_ [_license_](https://creativecommons.org/licenses/by-nc-sa/4.0/)