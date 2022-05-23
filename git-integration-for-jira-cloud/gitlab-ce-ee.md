---

title: GitLab CE/EE
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Using **Jira Server or Data Center**? [See the corresponding article](/wiki/spaces/GITSERVER/pages/80805889).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85524528/image-20200815-134810.png?version=1&modificationDate=1597500982662&cacheVersion=1&api=v2&width=374&height=84)

# Integrate GitLab CE/EE with Jira Cloud

This feature tracks added or deleted repositories from a remote GitLab server (EE/CE) and automatically imports those Git repository references into Jira.

GitLab v10+ stopped accepting username/password credentials for API access and will only recognize Personal Access Tokens (PAT) and OAuth authentications. Service users are strongly advised to switch from using username/password for newer versions of GitLab Server (CE/EE) to using PAT.

For GitLab Server service users, they won't see the issue until they upgrade their GitLab Servers to version 10 and higher. Git Integration for Jira app offers pre-v10 GitLab Server service users as a Legacy connection option.

Support for Gitlab API v3 is deprecated. We recommend to use **GitLab API v4** when adding new integrations for increased security.

BigBrassBand recommends a dedicated user for this integration which has access permissions to the GitLab CE/EE git repositories.


Quickly learn how to connect GitLab CE/EE git repositories via Git Integration for Jira Server app.

**What's on this page:**

* * *

_Right click_ [_**here**_](https://bigbrassband.wisita.com/medias/q9q0zg3rug) _and open this video in a new tab/window for more viewing options._
_(Updated video coming soon)_

## Permissions

GitLab can have users with different access level to a group or project. If the user's connected GitLab repositories to Jira are not accessible or commits are not showing for that user -- it's related to permission issues. This can be a per user, repository or a project level restriction.

If you encounter access permission issues, you will need to ask your Git administrator to grant you the required level of access to specific projects. If you are a Git administrator, you will need to setup a GitLab user with the minimum required permissions to view GitLab projects from Jira.

Take the following cases for example:

*   The personal access token (PAT) that the GitLab user provided doesn't have the correct permissions within GitLab to view source code for specific repositories.

*   The GitLab user doesn't have access privileges to a GitLab repository or is not a member of a group that has access to specific repositories.


We recommend creating a specific GitLab user for the integration. This way, the GitLab user can have specific permissions to do the given tasks.

![gitlab user permissions or repository permissions](https://bigbrassband.atlassian.net/wiki/download/attachments/85524528/image-20200815-075633.png?version=1&modificationDate=1597500983821&cacheVersion=1&api=v2)

**For minimum access (read-only) permissions:**

1.  Set the user account profile's PAT scope to **read\_repository**.

2.  The GitLab user is set to only **read** a specific repository. Set to **Reporter** role.


This level of access allows the user to view commits for the specific repository.

**For users who will be tasked with creating branches and merge requests:**

1.  Set the user account profile's PAT scope to **api**.

2.  The GitLab user should be set to **read/write** access for the specific repository. Set to **Developer** role.


This level of access allows the user to create/delete branches and create merge requests.

For more information, see [**GitLab Permissions »**](https://docs.gitlab.com/ee/user/permissions.html).

## Creating a personal access token

If two-factor authentication is enabled for your GitLab Server account, you will need to create a personal access token (PAT) to access your git repositories. Enable two-factor authentication in your GitLab Server account for increased security.

While instructions from GitHub works just fine, [follow this article](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens#CreatingPersonalAccessTokens-gitlab) for a quick step-by-step guide to get you started.

## Using Git service integration

Support for Gitlab API v3 is deprecated. We recommend to use **GitLab API v4** when adding new integrations for increased security.

This process requires an existing GitLab Server EE or GitLab Server CE. If your GitLab Server version is 10.2 or newer, a [personal access token](/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens) must be configured.

We recommend using the Full feature integrations panel to connect multiple repositories from your GitLab CE/EE account.

1.  On the Jira Cloud dashboard menu, go to **Apps** ➜ **Git Integration: Manage integrations**. The git configuration page for connecting repositories is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85524528/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1649329458191&cacheVersion=1&api=v2)

2.  On the Manage integrations page, click **Add integration.**

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85524528/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1649329480531&cacheVersion=1&api=v2)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85524528/gitcloud-managed-ui-git-service-sel(c).png?version=1&modificationDate=1649329480536&cacheVersion=1&api=v2)

4.  The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85524528/gitcloud-gitlab-ceee-git-service-sel(c).png?version=1&modificationDate=1649688381097&cacheVersion=1&api=v2)
    1.  Choose **GitLab**[1](https://bigbrassband.atlassian.net/wiki/pages/resumedraft.action?draftId=85524528#GitLabCE/EE-gitlab-logo-license) **Server CE/EE (APIv4)** from the Git hosting service list.

    2.  Enter the **Host URL** of the GitLab Server

    3.  Enter the **Personal Access Token** for server authentication. 2FA must be enabled in your GitLab Server and [PAT has been configured](/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens).

    4.  Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed. These settings are used with integration to retrieve the list of tracked repositories. Set a filter that will only load some cloned repositories which can be viewed in the Manage repositories page.

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85524528/gitcloud-integration-advanced-options-wo-sslverify(c).png?version=1&modificationDate=1649688737208&cacheVersion=1&api=v2&width=533&height=279)
        1.  **Custom API Path**  –  this is a relative path that starts with "/". The maximum allowed length is 2000 characters or less. The integration will use the relative REST API path to retrieve the list of tracked repositories. For more information on GitLab custom API paths, see [GitLab API](https://docs.gitlab.com/ee/api/projects.html). For more examples, see article [Jira Cloud: Working with Custom API Path](/wiki/spaces/GITCLOUD/pages/133201972/Working+with+Custom+API+Path).

            ```java
            GitLab version API support:
            Gitlab v9.5 and above -- only API v4.
            Gitlab v9.0 to v9.4.x -- API v3 and API v4.
            ```

        2.  **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is 2000 characters or less.
            Read about JMESPath expressions on their [website](http://jmespath.org/). For help with writing expressions, please contact [support](mailto:support@bigbrassband.com).
            To know more examples, see article [Jira Cloud: Working with JMESPath Filters](/wiki/spaces/GITCLOUD/pages/133234759/Working+with+JMESPath+Filters).

    5.  While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

5.  Click **Connect and select repositories**. The Git Integration for Jira app will import detected GitLab CE/EE repositories.

    *   Currently, the Git Integration for Jira app scans only the repositories visible to the user which is used for scanning. The repositories which are publicly visible _(shared for all members or visible to the member with the admin rights)_ will not be scanned. This will be supported in a future release.

6.  On the following screen, the Git Integration for Jira app will read all available repositories from your GitLab account.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/85524528/gitcloud-gitlab-ceee-repo-sel(c).png?version=1&modificationDate=1649690339078&cacheVersion=1&api=v2)

7.  Click **Connect** **repositories** to complete this setup.


GitLab CE/EE repositories are now connected to Jira Cloud. The GitLab server is added to the repositories list as a connected server and is automatically reindexed.

Repositories added or removed from GitLab server will be likewise added or removed from Jira Cloud. There will be a slight delay in adding 2FA-enabled repositories compared to others. These will show in the git configuration list eventually.

The Git Integration for Jira app supports GitLab API v4 (in both Jira Cloud and Jira Server/Data Center).

For newer GitLab authentication - in order to access a Git repository over HTTP, use the username as the username and the PAT for the password.

**Administrators**
If you need to require users PAT for creating branches or merge requests, turn on this setting via the selected integration in Manage integrations page ➜ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Edit integration**.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85524528/gitcloud-edit-integration-feature-cfg-req-user-PAT.png?version=1&modificationDate=1649690453368&cacheVersion=1&api=v2&width=680&height=75)

## Single git repository integration

This process requires an existing GitLab CE/EE git repository. Look for the the GitLab CE/EE repository clone URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the GitLab CE/EE git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/wiki/spaces/GITCLOUD/pages/923238448)

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

4.  Click **View Full Commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025229).

## Working with branches and merge requests with GitLab CE/EE

For GitLab CE/EE (Legacy or newer), the user must have the **Write** permissions and the `api` PAT scope.

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex.  Auto-connected integrations support this feature where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level.

Main branch for repositories within an integration can only be changed on the git server.

### Creating Branches

On your Jira Cloud, open a Jira issue. On the [Jira Git integration development panel](/wiki/spaces/GITCLOUD/pages/1923025809/Jira+Git+integration+development+panel), click **Open Git Integration** then click **Create branch**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85524528/gitcloud-gitlab-ceee-create-branch-dlg.png?version=1&modificationDate=1649691446984&cacheVersion=1&api=v2&width=680&height=221)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab owner name. For example, `johnsmith/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/781975665) page.

2.  Choose a **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one connected repository - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/85622895/GitLab.com#) page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  Click **Create branch** to complete this process.


For more detailed information on this feature, see [Create Branch](/git-integration-for-jira-cloud/Create-branch).


The newly-created branch is now listed in the developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

### Creating merge requests

The merge request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the Jira Git integration development panel, click **Open Git integration** then click **Create merge request**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/85524528/gitcloud-dev-panel-create-merge-req-dlg.png?version=1&modificationDate=1649690775185&cacheVersion=1&api=v2&width=680&height=240)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab group name. For example, `BigBrassBand/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/85622895/GitLab.com#) page.

2.  Choose the newly-created branch as the **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one connected repository - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/85622895/GitLab.com#) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.

5.  Click **Create merge request** to complete this process. Follow the link to the PR to setup for review and approval.


Merge requests are still indexed based on branch name even if the MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.

**Preview** allows you to see the comparison view of the current changes in the selected **Source branch** vs **Target branch** (_usually_ _master_).

For more detailed information on this feature, see [Creating merge requests](/wiki/spaces/GITCLOUD/pages/733315235/Create+pull+or+merge+request).


The merge request is listed on the developer panel of the Jira issue page.

The merge request is also ready for approval by the reviewers in your GitLab web portal.



1 _Logo owned by_ [_GitLab Inc_](https://gitlab.com/) _used under_ [_license_](https://creativecommons.org/licenses/by-nc-sa/4.0/)