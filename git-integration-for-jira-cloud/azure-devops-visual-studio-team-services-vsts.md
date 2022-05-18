---

title: Azure DevOps | Visual Studio Team Services (VSTS)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Using **Jira Server or Data Center**?  [See the corresponding article](/wiki/spaces/GITSERVER/pages/80805899).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/image-20200907-092906.png?version=1&modificationDate=1599482305596&cacheVersion=1&api=v2&width=340&height=74)![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/image-20200907-092920.png?version=1&modificationDate=1599482306094&cacheVersion=1&api=v2&width=340&height=112)

# Integrate VSTS/Azure DevOps with Jira Cloud

Quickly learn how to connect Azure DevOps/VSTS git repositories via Git Integration for Jira app.

The Git Integration for Jira app supports Azure Repos.

**What's on this page:**

* * *

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/n840jfrer4) _and open this video in a new window/tab for more viewing options._

## Creating personal access tokens

If you have not yet generated a personal access token (PAT), you can create one by following the simple steps in [this article](/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens) – use the table of content anchor link to go to the Azure DevOps / VSTS section.

This step is **highly required** for Azure DevOps/ VSTS integrations connected via the Full feature integrations panel.

## Permissions

Set Azure DevOps/VSTS repository permissions according to your organization's rules. Viewing commits from Jira requires the user to have at least **Read** or **View** permissions. For branch/pull request creation, set specific service users with **Write** permissions.

Git Integration for Jira Cloud requires Git admins to allow the third-party app access OAuth security policy in their organization settings:

1.  On your Azure DevOps/VSTS portal, go to the home page.

2.  Click an organization then go to **Organization Settings** (sidebar).

3.  Under _**Security**_, click **Policies**.

4.  Ensure that the **Third-party application access via OAuth** option is set to ON.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/vsts-azure-devops-org-cfg-policy-oauth.png%3Fversion=1&modificationDate=1575389745086&cacheVersion=1&api=v2?version=1&modificationDate=1599482306573&cacheVersion=1&api=v2&width=680&height=177)

For projects connected with Azure Active Directory, set the conditional access policy validation to OFF:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/enable-conditional-access-policy-AD.png%3Fversion=1&modificationDate=1575427942111&cacheVersion=1&api=v2?version=1&modificationDate=1599482307061&cacheVersion=1&api=v2&width=442&height=126)

## Using Git service integration

Connecting Azure DevOps / VSTS accounts with Full feature integration enables usability features that are not available in single repository connections.

**Creating personal access token**

If you have not yet generated a personal access token (PAT), you can create one by following the simple steps in [this article](/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens) – use the table of content anchor link to go to the Azure DevOps / VSTS section.

This step is **highly required** for Azure DevOps/ VSTS integrations connected via the Full feature integrations panel.

### Authenticate with OAuth (recommended)

This process requires an existing Microsoft account with Azure DevOps/VSTS **git** projects.

We recommend using the Git service integration panel to connect multiple repositories from your Azure DevOps/VSTS account.

1.  On the Jira Cloud dashboard menu, go to **Apps ➜ Git Integration: Manage integrations**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1649811215699&cacheVersion=1&api=v2)

2.  On the Manage integrations page, click **Add integration.**

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1649811242005&cacheVersion=1&api=v2)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-managed-ui-git-service-sel(c).png?version=1&modificationDate=1649811242012&cacheVersion=1&api=v2)

4.  The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-integration-azure-vsts-oauth-connect(c).png?version=1&modificationDate=1650530291987&cacheVersion=1&api=v2)
    1.  For Git hosting service, scroll to _Microsoft using OAuth_, select **Visual Studio Team Services (VSTS)**. If you are using **Azure DevOps Repos**, choose that instead.

    2.  Configuring the **Advanced** settings is optional. This setting is used with integration to retrieve the list of tracked repositories. Set a filter that will only load some cloned repositories which can be viewed in the Manage repositories page. However, admins/power users may set how the project listing is displayed on the following:

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/gitcloud-integration-advanced-vsts-azure-options(c).png?version=2&modificationDate=1649815607044&cacheVersion=1&api=v2&width=510&height=163)
    3.  **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is **2000** characters or less.

        1.  If the field is empty, the Git Integration for Jira app will get all available accounts and then scans all available git repositories.

        2.  If the field is not blank, the app will assume it as a single account path and will try to use it. To connect to all available accounts, manually create integrations for each one of them.

        3.  Read about JMESPath expressions on their [website](http://jmespath.org/).

        4.  For help with writing expressions, please contact [support](mailto:support@bigbrassband.com).

        5.  To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](/wiki/spaces/GITCLOUD/pages/133234759/Working+with+JMESPath+Filters).

5.  Click **Connect Azure Repos/VSTS** to continue.

6.  Login to your Microsoft account, if prompted. We recommend creating a new Microsoft user and setting specific permissions for use with Jira Cloud. The following authentication screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/gitcloud-ms-azure-vsts-grant-permissions(c).png?version=3&modificationDate=1649821597479&cacheVersion=1&api=v2&width=646&height=401)

7.  The Git Integration for Jira Cloud app will read all available repositories from your Azure DevOps/VSTS git service account. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-integration-azure-vsts-repo-sel(c).png?version=1&modificationDate=1649819236305&cacheVersion=1&api=v2)
    1.  Currently, all available accounts are scanned and corresponding URLs are created internally. Repositories of the logged-in Microsoft user can be automatically connected to Jira Cloud. Repositories that are added or removed from Azure DevOps/VSTS will be likewise connected or disconnected from Jira Cloud.

    2.  Use the search options to filter displayed repositories for the current screen.

    3.  Connect all repositories and organizations or select specific repositories to connect for this integration.

8.  Click **Connect repositories**. For now, only git projects are supported from Azure DevOps or VSTS.


Azure DevOps/VSTS git repositories are now connected to Jira Cloud.

### Authenticate with personal access token

This process requires an existing Microsoft account with Azure DevOps/VSTS **git** projects and PAT is configured.

We recommend using the Full feature integrations panel to connect multiple repositories from your Azure DevOps/VSTS account.

1.  On the Jira Cloud dashboard menu, go to **Apps ➜ Git Integration: Manage integrations**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1649811215699&cacheVersion=1&api=v2)

2.  On the Manage integrations page, click **Add integration.**

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1649811242005&cacheVersion=1&api=v2)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-managed-ui-git-service-sel(c).png?version=1&modificationDate=1649811242012&cacheVersion=1&api=v2)

4.  The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-integration-azure-vsts-pat-connect-sel(c).png?version=1&modificationDate=1649825538741&cacheVersion=1&api=v2)
    1.  For Git hosting service, scroll to _Microsoft using PAT_, select **Visual Studio Team Services (VSTS)**. If you are using **Azure DevOps Repos**, choose that instead.

    2.  Enter the personal access token on the provided box.

    3.  Configuring the **Advanced** settings is optional. This setting is used with integration to retrieve the list of tracked repositories. Set a filter that will only load some cloned repositories which can be viewed in the Manage repositories page. However, admins/power users may set how the project listing is displayed on the following:

        ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/gitcloud-integration-advanced-vsts-azure-options(c).png?version=2&modificationDate=1649815607044&cacheVersion=1&api=v2&width=510&height=163)
    4.  **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is **2000** characters or less.

        1.  If the field is empty, the Git Integration for Jira app will get all available accounts and then scans all available git repositories.

        2.  If the field is not blank, the app will assume it as a single account path and will try to use it. To connect to all available accounts, manually create integrations for each one of them.

        3.  Read about JMESPath expressions on their [website](http://jmespath.org/).

        4.  For help with writing expressions, please contact [support](mailto:support@bigbrassband.com).

        5.  To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](#).

5.  Click **Connect and select repositories** to continue.

6.  Login to your Microsoft account, if prompted. We recommend creating a new Microsoft user and setting specific permissions for use with Jira Cloud. The following authentication screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/gitcloud-ms-azure-vsts-grant-permissions(c).png?version=3&modificationDate=1649821597479&cacheVersion=1&api=v2&width=646&height=401)

7.  The Git Integration for Jira Cloud app will read all available repositories from your Azure DevOps/VSTS git service account. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-integration-azure-vsts-repo-sel(c).png?version=1&modificationDate=1649819236305&cacheVersion=1&api=v2)
    1.  Currently, all available accounts are scanned and corresponding URLs are created internally. Repositories of the logged-in Microsoft user can be automatically connected to Jira Cloud. Repositories that are added or removed from Azure DevOps/VSTS will be likewise connected or disconnected from Jira Cloud.

    2.  Use the search options to filter displayed repositories for the current screen.

    3.  Connect all repositories and organizations or select specific repositories to connect for this integration.

8.  Click **Connect repositories**. For now, only git projects are supported from Azure DevOps or VSTS.


Azure DevOps/VSTS git repositories are now connected to Jira Cloud.

## Single git repository integration

This process requires an existing Azure/VSTS git repository. Look for the the Azure/VSTS repository URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the Azure/VSTS git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/wiki/spaces/GITCLOUD/pages/923238448)

[Single git repository integration (SSH)](/wiki/spaces/GITCLOUD/pages/923238489)

The repository is now connected to Jira Cloud.

**Webhooks fail with DefaultCollection in URL Path**
To fix webhooks for old VSTS/Azure repository connections with `DefaultCollection` in the URL path, update the _**Repository origin**_ field in the Manage git repositories page ➜ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Edit repository settings** with the repository URL currently being returned by Azure.

## Troubleshooting integration

Some repositories are not showing for the integration user. If this is the case, make adjustments to the configuration on the following settings:

1.  Permissions  –  verify correct permissions have been granted to the integration user.

2.  Grant access to the Git Integration for Jira app.

3.  Convert the current repository format to git.


For detailed information, see [Troubleshooting: Repositories missing from Azure/VSTS/TFS integrations](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/421462017/Repositories+missing+from+Azure+DevOps+or+VSTS+integration).

## Webhooks and web linking

The Git Integration for Jira app automatically configures web linking for Azure DevOps/VSTS git repositories.

**Webhooks are supported on Azure DevOps and VSTS.**
First - configure webhooks in the Git Integration app in Jira via the **Apps** menu ➜ **Git Integration:** **Manage Git Repositories** then click **Indexing triggers** (sidebar). Enable the feature and save the settings. Then [follow these instructions](https://docs.microsoft.com/en-us/azure/devops/service-hooks/services/webhooks?view=vsts) to setup the webhook trigger. Azure DevOps/VSTS webhooks will trigger an immediate index of all repositories within the integration.

For detailed step-by-step guide showcasing webhooks setup, [see this article](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/172294150/Adding+Webhooks+for+Azure+DevOps+%7C+VSTS).

## Linking Azure DevOps/VSTS git commits to Jira Cloud

This process requires a VSTS/Azure DevOps git repository.

1.  On your web browser, login to your Azure DevOps/VSTS account then go to your working repository.

2.  Clone this repository into your Visual Studio IDE.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/vsts-webui-get-clone-url(c).png?version=1&modificationDate=1599482313298&cacheVersion=1&api=v2)

    ... or update your local repository files by performing a **Pull** action via VS IDE ➜ **Team Explorer**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/vside-teamexp-sync-changes-pull(c).png?version=1&modificationDate=1599482313986&cacheVersion=1&api=v2)
3.  Create or modify a file from your local repository.

4.  Perform a commit of the changes via **Team Explorer** ➜ **Changes**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/vs-ide-team-explorer-changes-commit-push(c).png?version=1&modificationDate=1599482314671&cacheVersion=1&api=v2)
    *   Enter the commit message by mentioning the Jira issue key to associate this commit to. _(Underlined in red)_.

    *   Click the dropdown on the Commit All button then select **Commit All and Push**.

5.  The commit is now displayed in the specified Jira issue.


![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/jira-server-vsts-repo-view-commit.png?version=1&modificationDate=1599482315314&cacheVersion=1&api=v2)

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025229).

## Working with branches and pull requests with Azure DevOps/VSTS

This process requires a VSTS/Azure DevOps git repository and a PAT with at least `Code (read and write)` scope.

This feature allows users to create branches and pull requests while inside Jira.

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level. 

Main branch for repositories within an integration can only be changed on the git server.

### Creating branches

On your Jira Cloud, open a Jira issue. On the Jira Git integration development panel, click **Open** **Git Integration** then click **Create branch**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/gitcloud-azure-vsts-creat-branch-dlg.png?version=2&modificationDate=1649833750537&cacheVersion=1&api=v2&width=680&height=221)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed Azure DevOps/VSTS repositories will have their names attached with a Azure DevOps/VSTS organization name. For example, `johnsmith/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com#) page.

    5.  For integration that uses PAT, the user is required to provide a personal access token for the repository to proceed creating the branch. Otherwise, no branch is created.

2.  Choose a **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com#) page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  Click **Create branch** to complete this process.


For more detailed information on this feature, see [Create branch](/wiki/spaces/GITCLOUD/pages/733282366/Create+branch).

The newly-created branch is now listed in the developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

### Creating pull requests

Before you can create a pull request, you need to create a branch first.

The pull request feature works the same as merge request.

On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Git Integration,** click **Create pull request**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86278279/gitcloud-dev-panel-create-pull-req-vsts-azure.png?version=1&modificationDate=1649856590192&cacheVersion=1&api=v2&width=680&height=240)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The selected repository will display the git service logo to identify which git host it is located from.

    2.  If there are several repositories with the same name, the listed Azure DevOps/VSTS repositories will have their names attached with a owner/team name. For example, `johnsmith/second-webhook-test-repo`.

    3.  Use the search box to look for the specific repository that will be used.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/wiki/spaces/GITCLOUD/pages/781975665/User+Settings) page.

    5.  For integration that uses PAT, the user is required to provide a personal access token for the repository to proceed creating the branch. Otherwise, no branch is created.

2.  Choose the newly-created branch as the **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com#) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.


Pull requests are still indexed based on branch name even if the PR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.

**Preview** allows you to see the comparison view of the current changes in the selected **Source branch** vs **Target branch** (_usually_ _master_).

For more detailed information on this feature, see [Create pull/merge request](/wiki/spaces/GITCLOUD/pages/733315235/Create+pull+or+merge+request).


The pull request is listed on the developer panel of the Jira issue page.

The pull request is also ready for approval by the reviewers in your Azure DevOps/VSTS web portal.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/vsts-webui-branch-ready-for-merge.png?version=1&modificationDate=1599482317585&cacheVersion=1&api=v2)

### Merging _branch_ to _master_

Continuing from the above steps, the current branch is ready for merge.

1.  On the Team Explorer, update your local repository by performing a **Pull** action.

2.  Go to **Pull Requests**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/vs-ide-teamexp-pull-request-approved(c).png?version=1&modificationDate=1599482318258&cacheVersion=1&api=v2)

    The pending pull request items are displayed here. Pull requests requires the approval of the reviewers before it can be merged from the VS IDE.

3.  Go to **Branches**. Click **Merge**. The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/vs-ide-team-explorer-branch-merge-2017(c).png?version=1&modificationDate=1599482318742&cacheVersion=1&api=v2)
    *   Set the source to the branch to which you pushed the commits.

    *   Set the target branch to _**master**_.

4.  Click **Merge** (button) to continue.


The reviewer's approval is required to completely merge the pull request. This usually takes place in the Azure DevOps/VSTS portal where your updated code is being reviewed.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/vsts-webui-pull-request-review-approve.png?version=1&modificationDate=1599482319180&cacheVersion=1&api=v2)

Once approved, the team leader or reviewer can then complete the merge. The commit can be viewed in the associated Jira issue page.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/86278279/gitcloud-merge-pull-request-example.png?version=2&modificationDate=1599482320395&cacheVersion=1&api=v2)

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

    [AWS CodeCommit](/wiki/spaces/GITCLOUD/pages/86180077/AWS+CodeCommit) (Git Integration for Jira Cloud)

*   Page:

    [Gerrit](/wiki/spaces/GITCLOUD/pages/86474926/Gerrit) (Git Integration for Jira Cloud)

*   Page:

    [Bitbucket Cloud](/wiki/spaces/GITCLOUD/pages/86343820/Bitbucket+Cloud) (Git Integration for Jira Cloud)

*   Page:

    [Introduction to Git integration](/wiki/spaces/GITCLOUD/pages/86966273/Introduction+to+Git+integration) (Git Integration for Jira Cloud)