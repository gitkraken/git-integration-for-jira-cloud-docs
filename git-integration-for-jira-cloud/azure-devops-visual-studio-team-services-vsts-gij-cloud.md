---

title: Azure DevOps | Visual Studio Team Services (VSTS)
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
        Using <b>Jira Server or Data Center</b>?  <a href='/git-integration-for-jira-self-managed/azure-devops-visual-studio-team-services-vsts-gij-self-managed'>See the corresponding article</a>.
    </div>
    </div>
</div>
<br>

<img src='/wp-content/uploads/gij-azure-devops2-banner.png' width=340 height=74 style='margin:25px 0' />

<img src='/wp-content/uploads/gij-vsts-logo.png' width=340 height=112 style='margin-bottom: 40px' />

# Integrate VSTS/Azure DevOps with Jira Cloud

Quickly learn how to connect Azure DevOps/VSTS git repositories via Git Integration for Jira app.

The Git Integration for Jira app supports Azure Repos.

**What's on this page:**
- [Integrate VSTS/Azure DevOps with Jira Cloud](#integratevstsazure-devops-with-jira-cloud)
  - [Creating personal access tokens](#creating-personal-access-tokens)
  - [Permissions](#permissions)
  - [Using Git service integration](#using-git-service-integration)
    - [Authenticate with OAuth (recommended)](#authenticate-with-oauth-recommended)
    - [Authenticate with personal access token](#authenticate-with-personal-access-token)
  - [Single git repository integration](#single-git-repository-integration)
  - [Troubleshooting integration](#troubleshooting-integration)
  - [Webhooks and web linking](#webhooks-and-web-linking)
  - [Linking Azure DevOps/VSTS git commits to Jira Cloud](#linking-azure-devopsvsts-git-commits-to-jira-cloud)
  - [Viewing git commits in Jira Cloud](#viewing-git-commits-in-jira-cloud)
  - [Working with branches and pull requests with Azure DevOps/VSTS](#working-with-branches-and-pull-requests-with-azure-devopsvsts)
    - [Default branch](#default-branch)
    - [Creating branches](#creating-branches)
    - [Creating pull requests](#creating-pull-requests)
    - [Merging _branch_ to _master_](#merging-branch-tomaster)

<br>
<br>
<hr>
<br>
<br>

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/n840jfrer4?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px; margin-bottom:30px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/n840jfrer4'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

## Creating personal access tokens

If you have not yet generated a personal access token (PAT), you can create one by following the simple steps in [this article](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) – use the table of content anchor link to go to the Azure DevOps / VSTS section.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This step is <b>highly required</b> for Azure DevOps/VSTS integrations connected via the Git service integrations setup.
    </div>
    </div>
</div>
<br>

## Permissions

Set Azure DevOps/VSTS repository permissions according to your organization's rules. Viewing commits from Jira requires the user to have at least **Read** or **View** permissions. For branch/pull request creation, set specific service users with **Write** permissions.

Git Integration for Jira Cloud requires Git admins to allow the third-party app access OAuth security policy in their organization settings:

1.  On your Azure DevOps/VSTS portal, go to the home page.

2.  Click an organization then go to **Organization Settings** (sidebar).

3.  Under _**Security**_, click **Policies**.

4.  Ensure that the **Third-party application access via OAuth** option is set to ON.

![](/wp-content/uploads/gij-vsts-azure-devops-org-cfg-policy-oauth.png)

For projects connected with Azure Active Directory, set the conditional access policy validation to OFF:

<img src='/wp-content/uploads/gij-enable-conditional-access-policy-AD.png' width=442 height=126 style='margin:25px auto 35px auto;display:block;max-width:100%' />

## Using Git service integration

Connecting Azure DevOps / VSTS accounts via Git service integration enables usability features that are not available in single repository connections or webhook indexing integrations.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        
    </div>
    </div>
</div>

This step is <b>highly required</b> for Azure DevOps/ VSTS integrations connected via the Git service integrations setup.

### Authenticate with OAuth (recommended)

This process requires an existing Microsoft account with Azure DevOps/VSTS **git** projects.

We recommend using the Git service integration panel to connect multiple repositories from your Azure DevOps/VSTS account.

1.  On the Jira Cloud dashboard menu, go to **Apps ➜ Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  For the following screen, click **Visual Studio Team Services (VSTS)** to start integration with this git service. If you're using Azure Repos, choose that instead.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-azure-vsts.png)

4.  The following screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-gitlab-integration-oauth-vsts-sel.png)

    *   We recommend the PAT integration for this git service. This uses personal access tokens to setup Azure/VSTS integrations. Users will have to configure their own PAT from Azure/VSTS to use for this setup.

    *   Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed. These settings are used with integration to retrieve the list of tracked repositories. Set a filter that will only load some cloned repositories which can be viewed in the Manage repositories page.

        <img src='/wp-content/uploads/gij-gitcloud-integration-advanced-vsts-azure-options-c.png' width=510 height=163 style='max-width:100%' />

    *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is **2000** characters or less.

        *   If the field is empty, the Git Integration for Jira app will get all available accounts and then scans all available git repositories.

        *   If the field is not blank, the app will assume it as a single account path and will try to use it. To connect to all available accounts, manually create integrations for each one of them.

        *   Read about JMESPath expressions on their [website](http://jmespath.org/).

        *   For help with writing expressions, please contact [support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

        *   To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

5.  Click **Connect VSTS** to continue. (For Azure Repos integration, click **Connect Azure Repos**.)

6.  Login to your Microsoft account, if prompted. We recommend creating a new Microsoft user and setting specific permissions for use with Jira Cloud. The following authentication screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-ms-azure-vsts-grant-permissions-c.png)

7.  The Git Integration for Jira Cloud app will read all available repositories from your Azure DevOps/VSTS git service account. The following screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-integration-repo-sel-vsts.png)

    *   Currently, all available accounts are scanned and corresponding URLs are created internally. Repositories of the logged-in Microsoft user can be automatically connected to Jira Cloud. Repositories that are added or removed from Azure DevOps/VSTS will be likewise connected or disconnected from Jira Cloud.

    *   Use the search options to filter displayed repositories for the current screen.

    *   Connect all repositories and organizations or select specific repositories to connect for this integration.

8.  Click **Connect repositories**. For now, only git projects are supported from Azure DevOps or VSTS.


Azure DevOps/VSTS git repositories are now connected to Jira Cloud.

### Authenticate with personal access token

This process requires an existing Microsoft account with Azure DevOps/VSTS **git** projects and PAT is configured.

We recommend using the Full feature integrations panel to connect multiple repositories from your Azure DevOps/VSTS account.

1.  On the Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  For the following screen, click **Visual Studio Team Services (VSTS)** to start integration with this git service. If you're using Azure Repos, choose that instead.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-azure-vsts.png)

4.  For the following screen, click on the **PAT** integration type.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-gitlab-integration-pat-vsts-sel.png)

    *   Enter the personal access token on the provided box.

    *   Configuring the **Advanced** settings is optional. This setting is used with integration to retrieve the list of tracked repositories. Set a filter that will only load some cloned repositories which can be viewed in the Manage repositories page. However, admins/power users may set how the project listing is displayed on the following:

        <img src='/wp-content/uploads/gij-gitcloud-integration-advanced-vsts-azure-options-c.png' width=510 height=163 style='margin:25px 0;max-width:100%' />

    *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is **2000** characters or less.

        *   If the field is empty, the Git Integration for Jira app will get all available accounts and then scans all available git repositories.

        *   If the field is not blank, the app will assume it as a single account path and will try to use it. To connect to all available accounts, manually create integrations for each one of them.

        *   Read about JMESPath expressions on their [website](http://jmespath.org/).

        *   For help with writing expressions, please contact [support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

        *   To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

5.  Click **Connect and select repositories** to continue.

6.  Login to your Microsoft account, if prompted. We recommend creating a new Microsoft user and setting specific permissions for use with Jira Cloud. The following authentication screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-ms-azure-vsts-grant-permissions-c.png)

7.  The Git Integration for Jira Cloud app will read all available repositories from your Azure DevOps/VSTS git service account. The following screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-integration-azure-vsts-repo-pat-sel.png)

    *   Currently, all available accounts are scanned and corresponding URLs are created internally. Repositories of the logged-in Microsoft user can be automatically connected to Jira Cloud. Repositories that are added or removed from Azure DevOps/VSTS will be likewise connected or disconnected from Jira Cloud.

    *   Use the search options to filter displayed repositories for the current screen.

    *   Connect all repositories and organizations or select specific repositories to connect for this integration.

8.  Click **Connect repositories**. For now, only git projects are supported from Azure DevOps or VSTS.


Azure DevOps/VSTS git repositories are now connected to Jira Cloud.

## Single git repository integration

This process requires an existing Azure/VSTS git repository. Look for the the Azure/VSTS repository URL on the repository project page. Choose between SSH or HTTPS.

Use this information to connect the Azure/VSTS git repository to your Jira Cloud via Git Integration for Jira app:

[Single git repository integration (HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

[Single git repository integration (SSH)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-ssh-gij-cloud)

The repository is now connected to Jira Cloud.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Webhooks fail with DefaultCollection in URL Path</b><br>
        To fix webhooks for old VSTS/Azure repository connections with <code>DefaultCollection</code> in the URL path, update the <b><i>Repository origin</i></b> field in the Manage git repositories page ➜ Actions ➜ <b>Edit repository settings</b> with the repository URL currently being returned by Azure.
    </div>
    </div>
</div>
<br>

## Troubleshooting integration

Some repositories are not showing for the integration user. If this is the case, make adjustments to the configuration on the following settings:

1.  Permissions  –  verify correct permissions have been granted to the integration user.

2.  Grant access to the Git Integration for Jira app.

3.  Convert the current repository format to git.


For detailed information, see [Troubleshooting: Repositories missing from Azure/VSTS/TFS integrations](/git-integration-for-jira-cloud/repositories-missing-from-azure-devops-or-vsts-integration-gij-cloud).

## Webhooks and web linking

The Git Integration for Jira app automatically configures web linking for Azure DevOps/VSTS git repositories.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Webhooks are supported on Azure DevOps and VSTS.</b><br>
        First - configure webhooks in the Git Integration app in Jira via the <b>Apps</b> menu ➜ <b>Git Integration: Manage Git Repositories</b> then click <b>Indexing triggers</b> (sidebar). Enable the feature and save the settings. Then <a href='https://docs.microsoft.com/en-us/azure/devops/service-hooks/services/webhooks?view=vsts'>follow these instructions</a> to setup the webhook trigger. Azure DevOps/VSTS webhooks will trigger an immediate index of all repositories within the integration.
    </div>
    </div>
</div>
<br>

For detailed step-by-step guide showcasing webhooks setup, [see this article](/git-integration-for-jira-cloud/adding-webhooks-for-azure-devops-repos-vsts-gij-cloud).

## Linking Azure DevOps/VSTS git commits to Jira Cloud

This process requires a VSTS/Azure DevOps git repository.

1.  On your web browser, login to your Azure DevOps/VSTS account then go to your working repository.

2.  Clone this repository into your Visual Studio IDE.

    ![](/wp-content/uploads/gij-vsts-webui-get-clone-url-c.png)

    ... or update your local repository files by performing a **Pull** action via VS IDE ➜ **Team Explorer**.

    ![](/wp-content/uploads/gij-vside-teamexp-sync-changes-pull-c.png)
3.  Create or modify a file from your local repository.

4.  Perform a commit of the changes via **Team Explorer** ➜ **Changes**.

    ![](/wp-content/uploads/gij-vs-ide-team-explorer-changes-commit-push-c.png)

    *   Enter the commit message by mentioning the Jira issue key to associate this commit to. _(Underlined in red)_.

    *   Click the dropdown on the Commit All button then select **Commit All and Push**.

5.  The commit is now displayed in the specified Jira issue.


<img src='/wp-content/uploads/gij-jira-server-vsts-repo-view-commit.png' width=613 height=202 style='margin:25px auto;display:block;max-width:!00%' />

<br>

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View full commit** to view the code diff.


For more information about this feature, see [Documentation: Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Working with branches and pull requests with Azure DevOps/VSTS

This process requires a VSTS/Azure DevOps git repository and a PAT with at least `Code (read and write)` scope.

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

On your Jira Cloud, open a Jira issue. On the Jira Git integration development panel, click **Open** **Git Integration** then click **Create branch**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-azure-vsts-creat-branch-dlg.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed Azure DevOps/VSTS repositories will have their names attached with a Azure DevOps/VSTS organization name. For example, `johnsmith/second-webhook-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

    *   For integration that uses PAT, the user is required to provide a personal access token for the repository to proceed creating the branch. Otherwise, no branch is created.

2.  Choose a **Source branch**.

    <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  Click **Create branch** to complete this process.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For more detailed information on this feature, see <a href='/git-integration-for-jira-cloud/create-branch-gij-cloud'>Create branch</a>.
    </div>
    </div>
</div>


The newly-created branch is now listed in the developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

### Creating pull requests

<div class="bbb-callout bbb--tip">
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

On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Git Integration,** click **Create pull request**. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-dev-panel-create-pull-req-vsts-azure.png)

**Pointers:**

1.  Select a **Repository** from the list.

    *   The selected repository will display the git service logo to identify which git host it is located from.

    *   If there are several repositories with the same name, the listed Azure DevOps/VSTS repositories will have their names attached with a owner/team name. For example, `johnsmith/second-webhook-test-repo`.

    *   Use the search box to look for the specific repository that will be used.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/git-integration-for-jira-cloud/User-Settings) page.

    *   For integration that uses PAT, the user is required to provide a personal access token for the repository to proceed creating the branch. Otherwise, no branch is created.

2.  Choose the newly-created branch as the **Source branch**.

    <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Pull requests are still indexed based on branch name even if the PR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.
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

The pull request is also ready for approval by the reviewers in your Azure DevOps/VSTS web portal.

![](/wp-content/uploads/gij-vsts-webui-branch-ready-for-merge.png)

<br>

### Merging _branch_ to _master_

Continuing from the above steps, the current branch is ready for merge.

1.  On the Team Explorer, update your local repository by performing a **Pull** action.

2.  Go to **Pull Requests**.

    ![](/wp-content/uploads/gij-vs-ide-teamexp-pull-request-approved-c.png)

    The pending pull request items are displayed here. Pull requests requires the approval of the reviewers before it can be merged from the VS IDE.

3.  Go to **Branches**. Click **Merge**. The following screen is displayed.

    ![](/wp-content/uploads/gij-vs-ide-team-explorer-branch-merge-2017-c.png)

    *   Set the source to the branch to which you pushed the commits.

    *   Set the target branch to _**master**_.

4.  Click **Merge** (button) to continue.


The reviewer's approval is required to completely merge the pull request. This usually takes place in the Azure DevOps/VSTS portal where your updated code is being reviewed.

![](/wp-content/uploads/gij-vsts-webui-pull-request-review-approve.png)

Once approved, the team leader or reviewer can then complete the merge. The commit can be viewed in the associated Jira issue page.

![](/wp-content/uploads/gij-gitcloud-merge-pull-request-example.png)

