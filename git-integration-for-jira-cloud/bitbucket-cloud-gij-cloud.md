---

title: Bitbucket Cloud
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
        Using <b>Jira Server</b> or <b>Data Center</b>? <a href=''>See the corresponding article</a>.
    </div>
    </div>
</div>

&nbsp;

![](/wp-content/uploads/bitbucket-mobile2.png)

&nbsp;

# Integrate Bitbucket Cloud with Jira Cloud

Quickly learn how to connect Bitbucket Cloud git repositories via Git Integration for Jira Cloud app.

**What's on this page:**
- [Integrate Bitbucket Cloud with Jira Cloud](#integratebitbucket-cloud-with-jira-cloud)
  - [Permissions](#permissions)
  - [Using Git service integration](#using-git-service-integration)
  - [Single repository connection](#single-repository-connection)
  - [Viewing git commits in Jira Cloud](#viewing-git-commits-in-jira-cloud)
  - [Working with branches and pull requests with Bitbucket](#working-with-branches-and-pull-requests-with-bitbucket)
    - [Default Branch](#default-branch)
    - [Creating branches](#creating-branches)
    - [Creating pull/merge requests](#creating-pullmerge-requests)
  - [More Integration Guides](#more-integration-guides)

<br>
<br>
<hr>
<br>
<br>

## Permissions

Set Bitbucket Cloud permissions according to your organization's rules. Viewing commits from Jira requires at least **Read** or **View** repository permissions. For branch/merge request creation, set specific service users with **Write** permissions.

## Using Git service integration

We recommend using the Git service integration setup to connect multiple repositories from your Bitbucket Cloud account.

1.  On your Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration.**

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  For the following screen, click **Bitbucket.org** to start integration with this git service.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-bitbucket.png)

4.  The following screen is displayed.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-bitbucket-connect.png)    

    *   Configuring the **Advanced** settings is optional. However, admins/power users may set how the project listing is displayed.

        ![](/wp-content/uploads/gij-gitcloud-integration-advanced-options-wo-sslverify-c.png)

        *   **Custom API Path**  –  this is a relative path that starts with "/". The integration will use the relative REST API path to retrieve the list of tracked repositories. The maximum allowed length is **2000** characters or less.

            To learn more examples, see article [Jira Cloud: Working with Custom API Path](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

        *   **JMESPath filter**  –  JMESPath is a query language for JSON used to filter API results and to limit which repositories are integrated. The maximum allowed length is **2000** characters or less.
            
            Read about JMESPath expressions on their [website](http://jmespath.org/). For help with writing expressions, please contact [support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

            To learn more examples, see article [Jira Cloud: Working with JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

    *   While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

5.  Click **Connect** to proceed.

6.  Login to your Bitbucket Cloud account if prompted. If 2FA is enabled for your account, enter the code and continue.

    ![](/wp-content/uploads/gij-gitcloud-bitbucket-grant-oauth-access.png)

7.  Grant OAuth access for Git Integration for Jira Cloud app when prompted.

8.  On the repository selection screen, feel free to choose repositories to use for this integration. You may use the **Connect all...** option to mark all repositories in the list.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-bitbucket-repo-sel.png)

9.  Click **Connect repositories** to complete this setup.


The Bitbucket Cloud repositories are now connected to Jira Cloud.


## Single repository connection

![](/wp-content/uploads/gij-gitcloud-bitbucket-home-repo-clone-url.png)

Obtain the repository URL from the Bitbucket Cloud repository project page. Choose between SSH or HTTPS.

1.  On your Jira dashboard menu, go to Apps ➜ **Git Integration: Manage integrations**.

2.  Click **Add integration**.

3.  At the bottom section on the following screen, enter the git clone URL in the provided box.

    ![](/wp-content/uploads/ij-gitcloud-managed-ui-git-integration-single-https-bitbucket.png)

4.  Click **Connect** to proceed.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-bitbucket-integration-repo-settings.png)

5.  Enter **Username** and **Password**. If 2FA is enabled, enter PAT on the password field.

6.  Click **Add integration** to complete this process.

The repository is now connected to Jira Cloud.

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message.  This will associate the commit to the mentioned Jira issue.
2.  Open the Jira issue.
3.  Scroll down to the **_Activity_** panel then click the **Git Commits** tab.
4.  Click **View Full Commit** to view the code diff.

For more information about this feature, see [Documentation: Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Working with branches and pull requests with Bitbucket

The Git Integration for Jira Cloud app adds two features on the Jira issue developer panel – **Create Branch**, and **Create Pull/Merge Request**. For more information about the developer panel, see the Jira Git development panel documentation.

This process requires a Bitbucket Cloud git repository. An **app password** is optional for access, but not required.

For Workspace users, the user must have the **Write** permissions.

<img src='/wp-content/uploads/gij-gitcloud-bitbucket-cloud-user-permissions.png' style='display:block;margin:25px auto 30px auto;max-width:100%' />

### Default Branch

Most git integrations allow changing of the default branch of the repository/project other than "master". This change is reflected in the  Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level.

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
<br><br>

### Creating branches

On your Jira Cloud, open a Jira issue. On the Jira Git integration development panel, click **Open Git Integration** then click **Create branch**. The following dialog is displayed.

<img src='/wp-content/uploads/gij-gitcloud-jira-issue-create-branch-dlg-bitbucket.png' style='display:block;margin:25px auto 25px auto;max-width:100%' />

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.
    
    *   If there are several repositories with the same name, the listed Bitbucket repositories will have their names attached with a Bitbucket workspace name. For example, `workspace01/revision-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the repository to be the default selected repository for current Jira project. To configure <u>default repositories</u> for more than one Jira project - use the <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a> page.

2.  Choose a **Source branch**. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the branch to be the default selected branch for the currently selected repository. To configure <u>default branches</u> for more than one repository - use the <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a> page.

3.  Enter a **Branch name** or leave it as is (recommended).

4.  lick **Create branch** to complete this process.

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

### Creating pull/merge requests

The pull request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Open Git Integration**, click **Create pull request**. The following dialog is displayed.

<img src='/wp-content/uploads/gij-gitcloud-jira-issue-create-pull-req-dlg-bitbucket.png' style='display:block;margin:25px auto 25px auto;max-width:100%' />

**Pointers:**

1.  Select a **Repository** from the list.

    *   The git host service logo is displayed for all the repositories in the dropdown list to easily identify which git service they belong.

    *   If there are several repositories with the same name, the listed Bitbucket repositories will have their names attached with a Bitbucket workspace name. For example, `workspace01/revision-test-repo`.

    *   Use the search box in the dropdown list to filter displayed repositories.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the repository to be the default selected repository for current Jira project. To configure <u>default repositories</u> for more than one Jira project - use the <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a> page.

2.  Choose the newly-created branch as the <b>Source branch</b>. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>
 Designate the branch to be the default selected branch for the currently selected repository. To configure <u>default branches</u> for more than one repository - use the <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a> page.

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

Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.

The pull request is listed on the developer panel of the Jira issue page.

The pull request is also ready for approval by the reviewers in your GitHub web portal.

Access the **Create branch** and **Create pull/merge request** features in the Jira issue developer panel. For more information, see [Jira Git integration development panel](/git-integration-for-jira-cloud/jira-issue-page-gij-cloud#jira-git-integration-development-panel).

&nbsp;

## More Integration Guides

[GitHub.com](/git-integration-for-jira-cloud/github-com-gij-cloud) (Git Integration for Jira Cloud)

[GitHub Enterprise Server](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud) (Git Integration for Jira Cloud)

[GitLab.com](/git-integration-for-jira-cloud/gitlab-com-gij-cloud) (Git Integration for Jira Cloud)

[GitLab CE/EE](/git-integration-for-jira-cloud/github-ce-ee-com-gij-cloud) (Git Integration for Jira Cloud)

[Azure DevOps \| Visual Studio Team Services (VSTS)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud) (Git Integration for Jira Cloud)

[Azure DevOps Server \| Team Foundation Services (TFS)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud) (Git Integration for Jira Cloud)

[AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommmit-gij-cloud) (Git Integration for Jira Cloud)

[Gerrit](/git-integration-for-jira-cloud/gerrit-gij-cloud) (Git Integration for Jira Cloud)

**Bitbucket Cloud** (this page)

[Introduction to Git integration](/git-integration-for-jira-cloud/integration-guide-gij-cloud) (Git Integration for Jira Cloud)

