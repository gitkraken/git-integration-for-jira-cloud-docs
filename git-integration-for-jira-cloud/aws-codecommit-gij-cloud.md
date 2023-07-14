---

title: AWS CodeCommit for Git Integration for Jira Cloud
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
        Using <b>Jira Server</b> or <b>Data Center</b>? <a href='/git-integration-for-jira-self-managed/aws-codecommit-gij-self-managed'>See the corresponding article</a>.
    </div>
    </div>
</div>

<img src='/wp-content/uploads/gij-aws-cc-logo-banner.png' width=442 height=92 style='margin:25px 0 30px 0' />

# Integrate AWS CodeCommit with Jira Cloud

AWS CodeCommit is a git host service by Amazon Web Services to store and manage source code, related files and private Git repositories in the cloud.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        You can use the AWS CLI or the AWS CodeCommit console to track and manage your repositories.
    </div>
    </div>
</div>
<br>

Quickly learn how to connect AWS CodeCommit git repositories via Git Integration for Jira Cloud.

&nbsp;

### Required permissions

<b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before performing an AWS CodeCommit integration, make sure to configure the recommended permissions.
    </div>
    </div>
</div>

The permissions detailed in the connect/Full feature integrations wizard are necessary for specific features to work.

We recommend that the following AWS IAM policies are configured beforehand based on what features that will be used.

Configure [**AWSCodeCommitReadOnly »**](http://docs.aws.amazon.com/codecommit/latest/userguide/access-permissions.html) IAM policy for basic features:

<table>
    <thead>
    <tr>
        <th align=left>Feature</th>
        <th align=left>Required Permission</th>
    </tr>
    </thead>
    <tbody>
        <tr>
            <td width=340>show commits, process smart commits, show branches</td>
            <td><code>codecommit:ListRepositories</code><br>
            <code>codecommit:GitPull</code><br>
            <code>codecommit:BatchGetRepositories</code></td>
        </tr>
        <tr>
            <td>show pull requests</td>
            <td><code>codecommit:ListPullRequests</code><br>
            <code>codecommit:GetPullRequest</code></td>
        </tr>
    </tbody>
</table>
<br>

<div id='all-features' style='display:hidden;margin:15px 0'></div>

Configure [**AWSCodeCommitPowerUser »**](https://docs.aws.amazon.com/codecommit/latest/userguide/auth-and-access-control-permissions-reference.html) IAM policy for all features:

<table>
    <thead>
        <tr>
            <th align=left>Feature</th>
            <th align=left>Required Permission</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td width=340>create pull request</td>
            <td><code>codecommit:CreatePullRequest</code></td>
        </tr>
        <tr>
            <td>create branch</td>
            <td><code>codecommit:CreateBranch</code></td>
        </tr>
        <tr>
            <td>delete branch</td>
            <td><code>codecommit:DeleteBranch</code></td>
        </tr>
        <tr>
            <td>configure webhooks automatically</td>
            <td><code>codecommit:GetRepositoryTriggers</code><br>
            <code>codecommit:PutRepositoryTriggers</code><br>
            <code>sns:CreateTopic</code><br>
            <code>sns:DeleteTopic</code><br>
            <code>sns:Subscribe</code></td>
        </tr>
    </tbody>
</table>

See [this article](/git-integration-for-jira-cloud/creating-personal-access-tokens/) for related information.

&nbsp;

### Webhooks and Triggers

<b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b>

CodeCommit doesn't have webhooks but it has SNS triggers requiring a <a href='https://docs.aws.amazon.com/sns/latest/dg/SendMessageToHttp.html' target='_blank'><b>subscription confirmation »</b></a>.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For webhooks to work automatically, the IAM user used to setup the connection must have the <b><i>configure webhooks automatically</i></b> permissions (<i>see Required permissions above – under IAM policy for</i> all features). If permissions has not been set, the repositories are connected but no webhooks are created.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        While the new UI is not fully functional in AWS CodeCommits, users are required to create triggers via the old UI or with the API.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Shorthand:</b><br>
        With an existing AWS CC repository, enable triggers then create an SNS topic and subscribe to that topic.
    </div>
    </div>
</div>

For more information on Amazon SNS, see <a href='https://docs.aws.amazon.com/sns/latest/dg/sns-getting-started.html' target='_blank'><b>Amazon SNS: Getting Started »</b></a>.

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/5w5p0lbz77?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/5w5p0lbz77'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<div align='center'>
    <i>Updated video coming soon.</i>
</div>
<br>

### Using Git service integration

This process requires an AWS account with existing CodeCommit repositories.

We recommend using the Full feature integrations panel (formerly Auto-connect integration panel) to connect multiple repositories from your AWS CodeCommit git host.

To connect your repository to Jira thru the Git Integration for Jira app, open the Add new integration wizard:

1.  On the Jira Cloud dashboard menu, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  For the following screen, click **AWS CodeCommit** to start integration with this git service.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-aws-cc-sel.png)

4.  On the following screen, proceed to enter information on the provided field boxes.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-add-integration-aws-cc.png)

    *   Enter the **Access key ID** and the **Secret access key** in their respective fields.

    *   Select the **Region** where the CodeCommit repositories reside. See below for the supported regions:

        *   AWS GovCloud (US)
        *   AWS GovCloud (US-East)
        *   US East (N. Virginia)
        *   US East (Ohio)
        *   US West (N. California)
        *   US West (Oregon)
        *   EU (Ireland)
        *   EU (London)
        *   EU (Paris)
        *   EU (Frankfurt)
        *   EU (Stockholm)
        *   EU (Milan)
        *   Asia Pacific (Hong Kong)
        *   Asia Pacific (Mumbai)
        *   Asia Pacific (Singapore)
        *   Asia Pacific (Sydney)
        *   Asia Pacific (Jakarta)
        *   Asia Pacific (Tokyo)
        *   Asia Pacific (Seoul)
        *   Asia Pacific (Osaka)
        *   South America (Sao Paulo)
        *   China (Beijing)
        *   China (Ningxia)
        *   Canada (Central)
        *   Middle East (Bahrain)
        *   Africa (Cape Town)
        *   US ISO East
        *   US ISOB East (Ohio)
        *   US ISO West

<br>

5.  Click **Connect and select repositories** to continue. On the following screen, the Git Integration for Jira Cloud app will read all available repositories from your AWS CodeCommit account.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-integration-aws-cc-repo-sel.png)

    *   Select one or more repositories to connect to your Jira Cloud instance.
    *   Repositories of the logged-in AWS CodeCommit user can be automatically connected to Jira Cloud. Repositories that are added or removed from AWS CodeCommit will be likewise connected or disconnected from Jira Cloud.

6.  Click **Connect repositories** to complete this setup.

The AWS CodeCommit repositories are now connected to Jira Cloud.

If the connected git host has newly added repositories, the Git Integration for Jira app will automatically add them to the git repositories configuration on the next reindex.

### Single repository (Manually connect via HTTP/HTTPS)

Connect a single AWS CodeCommit repository manually to Jira via HTTP/HTTPS connection.

<img src='/wp-content/uploads/gij-aws-cc-repo-home-portal-git-clone-url.png' style='max-width:100%;margin:25px auto;display:block;' />

Use the HTTP/HTTPS git clone URL from your AWS CodeCommit repository project page. Click on the HTTPS (Clone URL column - column 1) and use this for single git repository integrations with Git Integration for Jira cloud app.

[Single git repository integration (HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

The repository is now connected to Jira Cloud.

&nbsp;

### Single repository (Manually connect via SSH)

Connect a single AWS CodeCommit repository manually to Jira via SSH connection.

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/xq1xzic0tm?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/xq1xzic0tm'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

<img src='/wp-content/uploads/gij-aws-cc-repo-home-portal-git-clone-url.png' style='max-width:100%;margin:25px auto;display:block;' />

Use the SSH git clone URL from your AWS CodeCommit repository project page. Click on the SSH (Clone URL column - column 2) and use this for single git repository integrations with Git Integration for Jira cloud app.

[Single git repository integration (SSH)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-ssh-gij-cloud)

The repository is now connected to Jira Cloud.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>SSH setup</b><br>
        SSH connections are handled automatically if the PUBLIC KEY was added in the AWS IAM console and the associated PRIVATE KEY was added/uploaded on the Jira side (<i>Manage repositories page ➜ <img src='/wp-content/uploads/actions-icon.png' style='margin:0 3px' /> Actions ➜ <b>Edit repository</b> with an SSH repository on the list</i>).
    </div>
    </div>
</div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>SSH authentication issues</b><br>
        If authentication issues are encountered during connecting an AWS repository to Jira, modify the original URL by inserting the <b>SSH Key ID</b> as the username. The SSH Key ID is an alphanumeric sequence provided by AWS IAM when importing a PUBLIC KEY for a particular user account in IAM.
    </div>
    </div>
</div>

For example, the original URL is:

```powershell
ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/test-repo
```

If the SSH Key ID **1a2b3c4d5e** is applied to the original SSH URL, the resulting URL would be:

<img src='/wp-content/uploads/gij-aws-cc-ssh-codeline-example.png' width=633 height=52 style='max-width:100%;display:block;margin:25px auto' />

The modified URL can now be used as a valid repository URL via Manage repositories page ➜ Add integration ➜ **Single git repository integration** panel.

### Troubleshooting integration

Some repositories are not showing for the integration user. If this is the case, make adjustments to the configuration on the following settings:

*   **Permissions**  –  verify correct permissions have been granted to the integration user.

For detailed information, see [Required permissions](#required-permissions).

### Setting up AWS CodeCommit web links

The Git Integration for Jira app automatically configures web linking for AWS CodeCommit repositories connected via Git service integration in Jira Cloud.

For single repository connections, configuring web linking is optional. For more information, see [Web linking documentation](/git-integration-for-jira-cloud/web-linking-gij-cloud).

### Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View Full Commit** to view the code diff.


For detailed information on this process, see [Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

## Working with branches and pull requests

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This section requires the necessary permissions for <a href='#all-features'>all features</a>.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The user must have the required permissions in IAM to proceed creating the branch or pull request. Otherwise, no branch or pull request is created. For more information, see <a href='#required-permissions'>Required permissions</a> at the start of this guide.
    </div>
    </div>
</div>
<br>

The Git Integration for Jira app supports creation of branches and pull requests from Jira via the developer panel.

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the  Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level. 

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

On your Jira Cloud, open a Jira issue. On the Jira Git development panel, click **Open Git Integration** then click **Create branch**. The following dialog is displayed.

<img src='/wp-content/uploads/gij-gitcloud-create-branch-dlg-aws.png' style='margin:25px auto;display:block;max-width:100%' />

**Pointers:**

1.  Select a **Repository** from the list.

    *   The selected repository will display the git service logo to identify which git host it is located from.

    *   If there are several repositories with the same name, the listed CodeCommit repositories will have their names attached with a region name. For example, `us-west-2/test-repo`.

    *   Use the search box to look for the specific repository that will be used.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a> page.

2.  Choose a **Source branch**. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a> page.

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

The newly-created branch is now listed in the [Jira git development panel](/git-integration-for-jira-cloud/jira-git-integration-development-panel-gij-cloud) under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

The branch is also created and can be viewed under the **Branches** tab in your AWS CodeCommit web portal.

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

On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Git integration**, click **Create Pull Request**. The following dialog is displayed.

<img src='/wp-content/uploads/gij-gitcloud-create-pull-req-dlg-aws.png' style='max-width:100%;display:block;margin:25px auto;' />

**Pointers:**

1.  Select a **Repository** from the list.

    *   The selected repository will display the git service logo to identify which git host it is located from.

    *   If there are several repositories with the same name, the listed CodeCommit repositories will have their names attached with a region name. For example, `us-west-2/test-repo`.

    *   Use the search box to look for the specific repository that will be used.

    *   <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a> page.

2.  Choose the newly-created branch as the **Source branch**. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b> Designate the branch to be the default selected branch for the currently selected repository. To configure default branches for more than one repository - use the <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a> page.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is (recommended).

5.  Click **Create pull request** to complete this setup.

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
        **Preview** allows you to see the comparison view of the current changes in the selected **Source branch** vs **Target branch** (usually master).
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

The pull request is listed on the developer panel of the Jira issue page.

The pull request is also ready for approval by the reviewers in your AWS CodeCommit web portal.

The branch and the pull request status are also displayed on the developer panel.

### More Integration Guides

[GitHub.com](/git-integration-for-jira-cloud/github-com-gij-cloud) (Git Integration for Jira Cloud)

[GitHub Enterprise Server](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud) (Git Integration for Jira Cloud)

[GitLab.com](/git-integration-for-jira-cloud/gitlab-com-gij-cloud) (Git Integration for Jira Cloud)

[GitLab CE/EE](/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud) (Git Integration for Jira Cloud)

[Azure DevOps | Visual Studio Team Services (VSTS)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud) (Git Integration for Jira Cloud)

[Azure DevOps Server | Team Foundation Services (TFS)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud) (Git Integration for Jira Cloud)

[AWS CodeCommit](/git-integration-for-jira-cloud) (Git Integration for Jira Cloud)

[Gerrit](/git-integration-for-jira-cloud/gerrit-gij-cloud) (Git Integration for Jira Cloud)

[Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-cloud-gij-cloud) (Git Integration for Jira Cloud)

[Introduction to Git integration](/git-integration-for-jira-cloud/integration-guide-gij-cloud) (Git Integration for Jira Cloud)

