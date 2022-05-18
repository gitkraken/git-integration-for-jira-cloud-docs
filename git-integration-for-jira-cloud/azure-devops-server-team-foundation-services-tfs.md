---

title: Azure DevOps Server | Team Foundation Services (TFS)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Using **Jira Server or Data Center**? [See the corresponding article](/wiki/spaces/GITSERVER/pages/80904193).

![Azure DevOps Server banner logo](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86409345/image-20200817-113521.png?version=1&modificationDate=1598528954986&cacheVersion=1&api=v2&width=481&height=77)![Team Foundation Server banner logo](https://bigbrassband.com/confluence/images/tfs-logo.png)

# Integrate Azure DevOps Server/TFS with Jira Cloud

Quickly learn how to connect Azure DevOps Server/TFS git repositories via Git Integration for Jira app.

The Git Integration for Jira app supports Azure Repos.

**What’s on this page:**

* * *

## Creating personal access tokens

If you have not yet generated a personal access token (PAT), you can create one by following the simple steps in [this article](/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens) – use the table of content anchor link to go to the Azure DevOps Server/TFS section.

This step is **highly required** for Azure DevOps Server/TFS integrations connected via the Full feature integrations panel.

## Permissions

Set Azure DevOps Server/TFS repository permissions according to your organization's rules. Viewing commits from Jira requires the user to have at least **Read** or **View** permissions. For branch/pull request creation, set specific service users with **Write** permissions.

## Using Git service integration and OAuth

This process requires an existing Microsoft account with Azure DevOps Server/TFS **git** projects.

We recommend using the Git service integrations panel to connect multiple repositories from your Azure DevOps Server/TFS account.

1.  On the Jira Cloud dashboard menu, go to **Apps ➜ Git Integration: Manage integrations**.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/gitcloud-jira-apps-manage-integrations-sel(c).png?version=1&modificationDate=1649856891937&cacheVersion=1&api=v2)

2.  On the Manage integrations page, click **Add integration.**

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/gitcloud-managed-ui-webhook-idx-setup(c).png?version=1&modificationDate=1649856891946&cacheVersion=1&api=v2)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/gitcloud-managed-ui-git-service-sel(c).png?version=1&modificationDate=1649856891950&cacheVersion=1&api=v2)

4.  The following screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/gitcloud-integration-azure-server-2019-connect(c).png?version=1&modificationDate=1650535366559&cacheVersion=1&api=v2)
    1.  For Git hosting service, choose **Azure DevOps Server**. If you are using **Team Foundation Server (TFS)**, choose that instead.

    2.  Enter the **Host URL** for your Azure/TFS git server.

    3.  IMPORTANT For TFS 2017 and newer, use **PAT** for authentication. Otherwise, use **Username/Password** for authentication (for example: TFS 2013/2015). PATs were introduced with TFS 2017 and newer. TFS 2013 and TFS 2015 do not support PATs.

        ```java
        IMPORTANT!
        ==========
        Do NOT include the <DOMAIN> in the Username field when Azure DevOps
        Server/TFS is connected to Active Directory.

        Example: "BigBrassBand\johnsmith" ==> "johnsmith"
        ```

5.  Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed by configuring the following options:

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86409345/gitcloud-integration-azure-tfs-advanced(c).png?version=1&modificationDate=1650537080862&cacheVersion=1&api=v2&width=530&height=315)

    These settings are used with integration to control which tracked repositories are displayed and listed. Set a filter that will only load some cloned repositories which can be viewed via the **Manage repositories** page.

    1.  **Suffix**  –  This is a relative path that defaults to `"/tfs"`.

        *   For TFS integrations, the suffix will have a **/tfs** as default path. Thus, there is no need to add the `/tfs` to the **Host URL** path. If this field is blank, the Git Integration for Jira app automatically appends the default `"/tfs"` suffix and scans for all the collections inside it.

        *   If this field is not empty, the app assumes it as a single collection path and will try to use it.

        *   AZURE DEVOPS SERVER For Azure DevOps Server integrations, leave this field empty.

    2.  **Collection**  –  Enter a specific collection to use. If you know your specific collection, type it in the provided box. The Git Integration app defaults to read and import all collection in the connected Azure DevOps Server/TFS server.

    3.  **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is 2000 characters or less.

        *   If the field is empty, the Git Integration for Jira app will get all available accounts and then scans all available git repositories.

        *   If the field is not blank, the app will assume it as a single account path and will try to use it. To connect to all available accounts, manually create integrations for each one of them.


        Read about JMESPath expressions on their website. For help with writing expressions, please contact support.
        To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](/wiki/spaces/GITCLOUD/pages/133234759/Working+with+JMESPath+Filters).

6.  After filling up required fields, click **Connect and select repositories** to continue. The Git Integration for Jira app will read all available repositories from Azure DevOps Server/TFS.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/gitcloud-integration-azure-server-repo-sel(c).png?version=1&modificationDate=1650537944560&cacheVersion=1&api=v2)
    *   Currently, all available accounts are scanned and corresponding URLs are created internally. Repositories of the logged-in Microsoft user can be automatically connected to Jira Cloud. Repositories that are added or removed from Azure DevOps Server/TFS will be likewise connected or disconnected from Jira Cloud.

7.  Click **Connect repositories** to complete this setup.


For now, only **git** projects are supported from Azure DevOps Server/TFS.

Azure DevOps Server/TFS git repositories are now connected to Jira Cloud.

## Single git repository integration

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86409345/gitcloud-azure-tfs-git-clone-url.png?version=1&modificationDate=1650538648025&cacheVersion=1&api=v2&width=680&height=248)

This process requires an existing Azure DevOps Server/TFS git repository. Look for the repository git clone URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the Azure DevOps Server/TFS git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/wiki/spaces/GITCLOUD/pages/923238448)

[Single git repository integration (SSH)](/wiki/spaces/GITCLOUD/pages/923238489)

The repository is now connected to Jira Cloud.

## Troubleshooting integration

Some repositories are not showing for the integration user. If this is the case, make adjustments to the configuration on the following settings:

1.  Permissions  –  verify correct permissions have been granted to the integration user.

2.  Grant access to the Git Integration for Jira app.

3.  Convert the current repository format to git.


For detailed information, see [Troubleshooting: Repositories missing from Azure/VSTS/TFS integrations](http://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/421462017/Repositories+missing+from+Azure+DevOps+or+VSTS+integration).

## Webhooks and web linking

The Git Integration for Jira app automatically configures web linking for Azure DevOps Server/TFS git repositories.

**Webhooks are supported on Azure DevOps Server and TFS.**
First - configure webhooks in the Git Integration app in Jira via the **Apps** menu ➜ **Git Integration: Manage integrations** then click **Indexing triggers** (sidebar). Enable the feature and save the settings. Then [follow these instructions](https://docs.microsoft.com/en-us/azure/devops/service-hooks/services/webhooks?view=vsts) to setup the webhook trigger. Azure DevOps Server/TFS webhooks will trigger an immediate index of all repositories within the integration.

For detailed step-by-step guide showcasing webhooks setup, [see this article](/wiki/spaces/GITCLOUD/pages/234782736/Adding+webhooks+for+Azure+DevOps+Server+%7C+TFS).

## Linking Azure DevOps Server/TFS git commits to Jira Cloud

For the following steps, a Azure DevOps Server/TFS and a Visual Studio environment that supports git is required.

1.  Open Visual Studio IDE. Sign in to your Microsoft account, if prompted.

2.  Connect to your Azure DevOps Server/Team Foundation Server.

    ![Dialog showing VS IDE - TFS integration.](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/vs2013-connect-tfs-server-dlg(c).png?version=1&modificationDate=1598528959927&cacheVersion=1&api=v2)
    1.  Select a server in the dropdown list to connect to.

    2.  If this is a new connection, add a new server by clicking **Servers...** :

        1.  Type your Azure DevOps Server/TFS server **Host URL**

        2.  Enter **Username** and **Password**, if prompted.

    3.  Click **OK** to continue.

3.  Select a **Team Project** to work on then click **Connect**.

    *   For first time connection to the Azure DevOps Server/TFS team project, the default work branch is _**master**_.

4.  On the Team Explorer, click **Unsynced Commits** or **Sync**.

5.  Click the **Pull** to clone the git repositories to your local machine.

6.  Make changes to the code of a file/project.

7.  On the Team Explorer, click **Changes**.

8.  Type a message for this commit.

    ```java
    To associate this commit to the Jira issue page, mention the Jira issue key
    along with the commit message.

    For example:
    PRJ-123 Fix null code
    Where PRJ-123 is the Jira issue key and Fix null code is the commit comment.
    ```

    ![VS IDE team explorer dialog showing Changes tab and commit push options](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/vs-ide-team-explorer-make-commit(c).png?version=1&modificationDate=1598528960399&cacheVersion=1&api=v2)
9.  Click **Commit and Push**.


The commit is published to the Azure DevOps Server/TFS.  To view the commit in Jira, go to the Jira issue mentioned in the commit message. Click the **Git Commits** tab in the _**Activity**_ row.

![TFS commit example in Jira Cloud](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/jira-cloud-tfs-commit-example.png?version=1&modificationDate=1598528961042&cacheVersion=1&api=v2)

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025229).

## Working with branches and pull requests with Azure DevOps Server/TFS

This process requires a Azure DevOps Server/TFS git repository and a PAT with at least `Code (read and write)` scope.

This feature allows users to create branches and pull requests while inside Jira.

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level. 

Main branch for repositories within an integration can only be changed on the git server.

### Creating branches

On your Jira Cloud, open a Jira issue. On the Jira Git integration development panel, click **Open Git Integration** then click **Create branch**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86409345/gitcloud-jira-issue-create-branch-azure-tfs.png?version=1&modificationDate=1650539580030&cacheVersion=1&api=v2&width=680&height=242)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    2.  If there are several repositories with the same name, the listed Azure DevOps Server/TFS repositories will have their names attached with a Azure DevOps Server/TFS organization name. For example, `johnsmith/second-webhook-test-repo`.

    3.  Use the search box in the dropdown list to filter displayed repositories.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com#) page.

    5.  For integration that uses PAT, the user is required to provide a personal access token for the repository to proceed creating the branch. Otherwise, no branch is created.

2.  Choose a **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com#) page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  Click **Create branch** to complete this process.


The branch is created and can be viewed under the **Branches** tab in your Azure DevOps Server/TFS.

PATs were introduced with TFS 2017 and newer. TFS 2013 and TFS 2015 do not support PATs – for this case, if the repository setting _Require User PAT_ property is set to `ON`, the users will not be able to create/delete branches and pull requests.

![TFS portal showing newly created branch](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/tfs-server-2017-new-branch-example(c).png?version=1&modificationDate=1598528965435&cacheVersion=1&api=v2)

To update the branch list to your Visual Studio's Team Explorer:

1.  Perform a **Pull** action on the connected team project. The branches list in your VS IDE should be updated now.

2.  On the VS IDE Team Explorer, click **Branches**.

3.  Click **New Branch** then select the newly-created branch from the dropdown list.

4.  Click **Create Branch**. The selected branch is now listed under the **Published Branches** in the Team Explorer.

5.  Make changes to a file or project then perform a commit to the selected branch.

    ![VS IDE Team explorer docker showing Changes tab and committing to the new branch.](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/vs-ide-team-explorer-branch-commit(c).png?version=1&modificationDate=1598528966801&cacheVersion=1&api=v2)
    1.  On the Team Explorer, click Changes.

    2.  Make sure that **Branch:** displays the name of the newly-created branch. If not, select it again from the list.

    3.  This will associate the commit to the mentioned Jira issue key.

6.  Click the dropdown on the **Commit** button then select **Commit and Push**.


The commit is pushed to the new branch and is now ready for merge.

### Creating pull requests

Before you can create a pull request, you need to create a branch first.

The pull request feature works the same as merge request.

On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Git integration**, click **Create pull request**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86409345/gitcloud-create-pull-req-dlg-azure-tfs.png?version=1&modificationDate=1650540197278&cacheVersion=1&api=v2&width=680&height=240)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The selected repository will display the git service logo to identify which git host it is located from.

    2.  If there are several repositories with the same name, the listed Azure DevOps Server/TFSrepositories will have their names attached with a owner/team name. For example, `johnsmith/second-webhook-test-repo`.

    3.  Use the search box to look for the specific repository that will be used.

    4.  OPTIONAL Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/781975665) page.

    5.  For integration that uses PAT, the user is required to provide a personal access token for the repository to proceed creating the branch. Otherwise, no branch is created.

2.  Choose the newly-created branch as the **Source branch**. OPTIONAL Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com#) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.


Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.


The branch and the pull request status are displayed on the developer panel.

![Git development panel showing created branch and pull request](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/jira-cloud-tfs-branch-and-pull-request-dev-panel.png?version=1&modificationDate=1598528968392&cacheVersion=1&api=v2)

The pull request is also listed in the Azure DevOps Server/TFS.

![TFS portal showing pull requests items](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86409345/jira-cloud-tfs-pull-request-merge-details.png?version=1&modificationDate=1598528969572&cacheVersion=1&api=v2&width=680&height=292)

### Merging _branch_ to _master_

Continuing from the above steps, the current branch is ready for merge.

![TFS portal showing pull request ready for merge](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/jira-cloud-tfs-pull-request-ready-to-merge.png?version=1&modificationDate=1598528970432&cacheVersion=1&api=v2)

1.  On your VS IDE Team Explorer, go to **Branches**.

2.  Click the **Merge** tab.

    ![VS IDE Team explorer docker showing merge options](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/vs-ide-team-explorer-branch-merge-to-master(c).png?version=1&modificationDate=1598528971100&cacheVersion=1&api=v2)
    1.  Set the source to the branch you pushed the commits to.

    2.  Set the target branch to _**master**_.

3.  Click the **Merge** button to continue.


The reviewer's approval is required to completely merge the pull request. This usually takes place in the Azure DevOps Server/TFS web UI where your updated code is being reviewed.

![TFS portal showing pull request approved and ready for merge](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/tfs-web-ui-pull-request-approved-merge.png?version=1&modificationDate=1598528971826&cacheVersion=1&api=v2)

Once approved, the team leader or reviewer can then complete the merge. The commit can be viewed in the associated Jira issue page.

![Jira Cloud Issue page showing Git Commits tab with merged commit information](https://bigbrassband.atlassian.net/wiki/download/attachments/86409345/gitcloud-azure-tfs-merge-req-commit-example.png?version=1&modificationDate=1598528972663&cacheVersion=1&api=v2)

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