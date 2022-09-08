---

title: Azure DevOps Server | Team Foundation Services (TFS)
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
        Using <b>Jira Server or Data Center</b>? <a href='/git-integration-for-jira-self-managed/azure-devops-server-team-foundation-services-tfs-gij-self-managed'>See the corresponding article</a>.
    </div>
    </div>
</div>
<br>

<img src='/wp-content/uploads/gij-azure-devops-banner.png' width=481 height=77 style='margin:25px 0;max-width:100%;margin-bottom:0' />

<img src='/wp-content/uploads/gij-tfs-logo.png' width=359 height=138 style='margin:25px 0;max-width:100%;margin-bottom:40px' />

# Integrate Azure DevOps Server/TFS with Jira Cloud

Quickly learn how to connect Azure DevOps Server/TFS git repositories via Git Integration for Jira app.

The Git Integration for Jira app supports Azure Repos.

**What’s on this page:**
- [Integrate Azure DevOps Server/TFS with Jira Cloud](#integrate-azure-devops-servertfswith-jira-cloud)
  - [Creating personal access tokens](#creating-personal-access-tokens)
  - [Permissions](#permissions)
  - [Using Git service integration and OAuth](#using-git-service-integration-and-oauth)
  - [Single git repository integration](#single-git-repository-integration)
  - [Troubleshooting integration](#troubleshooting-integration)
  - [Webhooks and web linking](#webhooks-and-web-linking)
  - [Linking Azure DevOps Server/TFS git commits to Jira Cloud](#linking-azure-devops-servertfs-git-commits-to-jira-cloud)
  - [Viewing git commits in Jira Cloud](#viewing-git-commits-in-jira-cloud)
  - [Working with branches and pull requests with Azure DevOps Server/TFS](#working-with-branches-and-pull-requests-with-azure-devops-servertfs)
    - [Default branch](#default-branch)
    - [Creating branches](#creating-branches)
    - [Creating pull requests](#creating-pull-requests)
    - [Merging _branch_ to _master_](#merging-branch-to-master)
  - [More Integration Guides](#more-integration-guides)

<hr>

## Creating personal access tokens

If you have not yet generated a personal access token (PAT), you can create one by following the simple steps in [this article](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) – use the table of content anchor link to go to the Azure DevOps Server/TFS section.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This step is <b>highly required</b> for Azure DevOps Server/TFS integrations connected via the Full feature integrations panel.
    </div>
    </div>
</div>
<br>

## Permissions

Set Azure DevOps Server/TFS repository permissions according to your organization's rules. Viewing commits from Jira requires the user to have at least **Read** or **View** permissions. For branch/pull request creation, set specific service users with **Write** permissions.

## Using Git service integration and OAuth

This process requires an existing Microsoft account with Azure DevOps Server/TFS **git** projects.

We recommend using the Git service integrations panel to connect multiple repositories from your Azure DevOps Server/TFS account.

1.  On the Jira Cloud dashboard menu, go to **Apps ➜ Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-service-sel-c.png)

4.  The following screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-integration-azure-server-2019-connect-c.png)

    *   For Git hosting service, choose **Azure DevOps Server**. If you are using **Team Foundation Server (TFS)**, choose that instead.

    *   Enter the **Host URL** for your Azure/TFS git server.

    *   <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> For TFS 2017 and newer, use **PAT** for authentication. Otherwise, use **Username/Password** for authentication (for example: TFS 2013/2015). PATs were introduced with TFS 2017 and newer. TFS 2013 and TFS 2015 do not support PATs.

        ```java
        IMPORTANT!
        ==========
        Do NOT include the <DOMAIN> in the Username field when Azure DevOps
        Server/TFS is connected to Active Directory.

        Example: "BigBrassBand\johnsmith" ==> "johnsmith"
        ```

5.  Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed by configuring the following options:

    <img src='/wp-content/uploads/gij-gitcloud-integration-azure-tfs-advanced-c.png' width=530 height=315 style='margin:25px 0;max-width:100%' />

    These settings are used with integration to control which tracked repositories are displayed and listed. Set a filter that will only load some cloned repositories which can be viewed via the **Manage repositories** page.

    *   **Suffix**  –  This is a relative path that defaults to `"/tfs"`.

        *   For TFS integrations, the suffix will have a **/tfs** as default path. Thus, there is no need to add the `/tfs` to the **Host URL** path. If this field is blank, the Git Integration for Jira app automatically appends the default `"/tfs"` suffix and scans for all the collections inside it.

        *   If this field is not empty, the app assumes it as a single collection path and will try to use it.

        *   <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>AZURE DEVOPS SERVER</b> For Azure DevOps Server integrations, leave this field empty.

    *   **Collection**  –  Enter a specific collection to use. If you know your specific collection, type it in the provided box. The Git Integration app defaults to read and import all collection in the connected Azure DevOps Server/TFS server.

    *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is 2000 characters or less.

        *   If the field is empty, the Git Integration for Jira app will get all available accounts and then scans all available git repositories.

        *   If the field is not blank, the app will assume it as a single account path and will try to use it. To connect to all available accounts, manually create integrations for each one of them.

        Read about JMESPath expressions on their website. For help with writing expressions, please [contact support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).
        To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters).

6.  After filling up required fields, click **Connect and select repositories** to continue. The Git Integration for Jira app will read all available repositories from Azure DevOps Server/TFS.

    ![](/wp-content/uploads/gij-gitcloud-integration-azure-server-repo-sel-c.png)

    *   Currently, all available accounts are scanned and corresponding URLs are created internally. Repositories of the logged-in Microsoft user can be automatically connected to Jira Cloud. Repositories that are added or removed from Azure DevOps Server/TFS will be likewise connected or disconnected from Jira Cloud.

7.  Click **Connect repositories** to complete this setup.


For now, only **git** projects are supported from Azure DevOps Server/TFS.

Azure DevOps Server/TFS git repositories are now connected to Jira Cloud.

## Single git repository integration

<img src='/wp-content/uploads/gij-gitcloud-azure-tfs-git-clone-url.png' width=680 height=248 style='margin:25px auto;display:block;max-width:100%' />

This process requires an existing Azure DevOps Server/TFS git repository. Look for the repository git clone URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the Azure DevOps Server/TFS git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

[Single git repository integration (SSH)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-ssh-gij-cloud)

The repository is now connected to Jira Cloud.

## Troubleshooting integration

Some repositories are not showing for the integration user. If this is the case, make adjustments to the configuration on the following settings:

1.  Permissions  –  verify correct permissions have been granted to the integration user.

2.  Grant access to the Git Integration for Jira app.

3.  Convert the current repository format to git.


For detailed information, see [Troubleshooting: Repositories missing from Azure/VSTS/TFS integrations](/git-integration-for-jira-cloud/repositories-missing-from-azure-devops-or-vsts-integration-gij-cloud).

## Webhooks and web linking

The Git Integration for Jira app automatically configures web linking for Azure DevOps Server/TFS git repositories.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Webhooks are supported on Azure DevOps Server and TFS.</b><br>
        First - configure webhooks in the Git Integration app in Jira via the <b>Apps</b> menu ➜ <b>Git Integration: Manage integrations</b> then click <b>Indexing triggers</b> (sidebar). Enable the feature and save the settings. Then <a href='https://docs.microsoft.com/en-us/azure/devops/service-hooks/services/webhooks?view=vsts' target='_blank'>follow these instructions</a> to setup the webhook trigger. Azure DevOps Server/TFS webhooks will trigger an immediate index of all repositories within the integration.
    </div>
    </div>
</div>
<br>

For detailed step-by-step guide showcasing webhooks setup, [see this article](/git-integration-for-jira-cloud/adding-webhooks-for-azure-devops-server-tfs-gij-cloud).

## Linking Azure DevOps Server/TFS git commits to Jira Cloud

For the following steps, a Azure DevOps Server/TFS and a Visual Studio environment that supports git is required.

1.  Open Visual Studio IDE. Sign in to your Microsoft account, if prompted.

2.  Connect to your Azure DevOps Server/Team Foundation Server.

    ![Dialog showing VS IDE - TFS integration.](/wp-content/uploads/gij-vs2013-connect-tfs-server-dlg-c.png)

    *   Select a server in the dropdown list to connect to.

    *   If this is a new connection, add a new server by clicking **Servers...** :

        *   Type your Azure DevOps Server/TFS server **Host URL**

        *   Enter **Username** and **Password**, if prompted.

    *   Click **OK** to continue.

3.  Select a **Team Project** to work on then click **Connect**.

    *   For first time connection to the Azure DevOps Server/TFS team project, the default work branch is _**master**_.

4.  On the Team Explorer, click **Unsynced Commits** or **Sync**.

5.  Click the **Pull** to clone the git repositories to your local machine.

6.  Make changes to the code of a file/project.

7.  On the Team Explorer, click **Changes**.

8.  Type a message for this commit.

    ```powershell
    To associate this commit to the Jira issue page, mention the Jira issue key
    along with the commit message.

    For example:
    PRJ-123 Fix null code
    Where PRJ-123 is the Jira issue key and Fix null code is the commit comment.
    ```

    <img src='/wp-content/uploads/gij-vs-ide-team-explorer-make-commit-c.png' width=348 height=275 style='margin:25px 0' />

9.  Click **Commit and Push**.


The commit is published to the Azure DevOps Server/TFS.  To view the commit in Jira, go to the Jira issue mentioned in the commit message. Click the **Git Commits** tab in the _**Activity**_ row.

![TFS commit example in Jira Cloud](/wp-content/uploads/gij-jira-cloud-tfs-commit-example.png)

<br>

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Working with branches and pull requests with Azure DevOps Server/TFS

This process requires a Azure DevOps Server/TFS git repository and a PAT with at least `Code (read and write)` scope.

This feature allows users to create branches and pull requests while inside Jira.

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

On your Jira Cloud, open a Jira issue. On the Jira Git integration development panel, click **Open Git Integration** then click **Create branch**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-jira-issue-create-branch-azure-tfs.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed Azure DevOps Server/TFS repositories will have their names attached with a Azure DevOps Server/TFS organization name. For example, `johnsmith/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

    *   For integration that uses PAT, the user is required to provide a personal access token for the repository to proceed creating the branch. Otherwise, no branch is created.

2.  Choose a **Source branch**. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  Click **Create branch** to complete this process.


The branch is created and can be viewed under the **Branches** tab in your Azure DevOps Server/TFS.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        PATs were introduced with TFS 2017 and newer. TFS 2013 and TFS 2015 do not support PATs – for this case, if the repository setting <i>Require User PAT</i> property is set to <code>ON</code>, the users will not be able to create/delete branches and pull requests.
    </div>
    </div>
</div>
<br>

<img src='/tfs-server-2017-new-branch-example-c.png' width=723 height=451 style='margin:25px auto;display:block;max-width:100%;' />

To update the branch list to your Visual Studio's Team Explorer:

1.  Perform a **Pull** action on the connected team project. The branches list in your VS IDE should be updated now.

2.  On the VS IDE Team Explorer, click **Branches**.

3.  Click **New Branch** then select the newly-created branch from the dropdown list.

4.  Click **Create Branch**. The selected branch is now listed under the **Published Branches** in the Team Explorer.

5.  Make changes to a file or project then perform a commit to the selected branch.

    <img src='/wp-content/uploads/gij-vs-ide-team-explorer-branch-commit(c).png' width=349 height=427 style='margin:25px 0;' />

    1.  On the Team Explorer, click Changes.

    2.  Make sure that **Branch:** displays the name of the newly-created branch. If not, select it again from the list.

    3.  This will associate the commit to the mentioned Jira issue key.

6.  Click the dropdown on the **Commit** button then select **Commit and Push**.


The commit is pushed to the new branch and is now ready for merge.

### Creating pull requests

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before you can create a pull request, you need to create a branch first.
    </div>
    </div>
</div>
<br>

The pull request feature works the same as merge request.

On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Git integration**, click **Create pull request**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-create-pull-req-dlg-azure-tfs.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The selected repository will display the git service logo to identify which git host it is located from.

    *   If there are several repositories with the same name, the listed Azure DevOps Server/TFSrepositories will have their names attached with a owner/team name. For example, `johnsmith/second-webhook-test-repo`.

    *   Use the search box to look for the specific repository that will be used.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

    *   For integration that uses PAT, the user is required to provide a personal access token for the repository to proceed creating the branch. Otherwise, no branch is created.

2.  Choose the newly-created branch as the **Source branch**. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

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
<br>

The branch and the pull request status are displayed on the developer panel.

<img src='/wp-content/uploads/gij-jira-cloud-tfs-branch-and-pull-request-dev-panel.png' width=298 height=288 style='margin:25px auto;display:block;' />

The pull request is also listed in the Azure DevOps Server/TFS.

![TFS portal showing pull requests items](/wp-content/uploads/gij-jira-cloud-tfs-pull-request-merge-details.png)

### Merging _branch_ to _master_

Continuing from the above steps, the current branch is ready for merge.

![TFS portal showing pull request ready for merge](/wp-content/uploads/gij-jira-cloud-tfs-pull-request-ready-to-merge.png)

1.  On your VS IDE Team Explorer, go to **Branches**.

2.  Click the **Merge** tab.

    <img src='/wp-content/uploads/gij-vs-ide-team-explorer-branch-merge-to-master-c.png' width=348 height=287 style='margin:25px 0;' />

    *   Set the source to the branch you pushed the commits to.

    *   Set the target branch to _**master**_.

3.  Click the **Merge** button to continue.


The reviewer's approval is required to completely merge the pull request. This usually takes place in the Azure DevOps Server/TFS web UI where your updated code is being reviewed.

![TFS portal showing pull request approved and ready for merge](/wp-content/uploads/gij-tfs-web-ui-pull-request-approved-merge.png)

Once approved, the team leader or reviewer can then complete the merge. The commit can be viewed in the associated Jira issue page.

![Jira Cloud Issue page showing Git Commits tab with merged commit information](/wp-content/uploads/gij-gitcloud-azure-tfs-merge-req-commit-example.png)

## More Integration Guides

[GitHub.com](/git-integration-for-jira-cloud/github-com-gij-cloud)

[GitHub Enterprise Server](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud)

[GitLab.com](/git-integration-for-jira-cloud/gitlab-com-gij-cloud)

[GitLab CE/EE](/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud)

[Azure DevOps \| Visual Studio Team Services (VSTS)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud)

Azure DevOps Server \| Team Foundation Services (this page)

[AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommit-gij-cloud)

[Gerrit](/git-integration-for-jira-cloud/gerrit-gij-cloud)

[Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-cloud-gij-cloud)

[Introduction to Git integration](/git-integration-for-jira-cloud/integration-guide-gij-cloud)

