---

title: AWS CodeCommit
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Using **Jira Server or Data Center**? [See the corresponding article](https://bigbrassband.atlassian.net/wiki/x/JQDRB).

![AWS codecommit banner logo](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86180077/image-20200909-134637.png?version=1&modificationDate=1599745472495&cacheVersion=1&api=v2&width=442&height=92)

# Integrate AWS CodeCommit with Jira Cloud

AWS CodeCommit is a git host service by Amazon Web Services to store and manage source code, related files and private Git repositories in the cloud.

You can use the AWS CLI or the AWS CodeCommit console to track and manage your repositories.


Quickly learn how to connect AWS CodeCommit git repositories via Git Integration for Jira Cloud.

**What's on this page:**

* * *

## Required permissions

IMPORTANT

Before performing an AWS CodeCommit integration, make sure to configure the recommended permissions.


The permissions detailed in the connect/Full feature integrations wizard are necessary for specific features to work.

We recommend that the following AWS IAM policies are configured beforehand based on what features that will be used.

Configure [**AWSCodeCommitReadOnly »**](http://docs.aws.amazon.com/codecommit/latest/userguide/access-permissions.html) IAM policy for basic features:

|     |     |
| --- | --- |
| **Feature** | **Required Permission** |
| show commits, process smart commits, show branches | `codecommit:ListRepositories`  <br>`codecommit:GitPull`  <br>`codecommit:BatchGetRepositories` |
| show pull requests | `codecommit:ListPullRequests`  <br>`codecommit:GetPullRequest` |

#### all features

Configure [**AWSCodeCommitPowerUser »**](https://docs.aws.amazon.com/codecommit/latest/userguide/auth-and-access-control-permissions-reference.html) IAM policy for all features:

|     |     |
| --- | --- |
| **Feature** | **Required Permission** |
| create pull request | `codecommit:CreatePullRequest` |
| create branch | `codecommit:CreateBranch` |
| delete branch | `codecommit:DeleteBranch` |
| configure webhooks automatically | `codecommit:GetRepositoryTriggers`  <br>`codecommit:PutRepositoryTriggers`  <br>`sns:CreateTopic`  <br>`sns:DeleteTopic`  <br>`sns:Subscribe` |

See [this article](/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens#CreatingPersonalAccessTokens-aws_codecommit) for related information.

## Webhooks | Triggers

RECOMMENDED

CodeCommit doesn't have webhooks but it has SNS triggers requiring a [**subscription confirmation »**](https://docs.aws.amazon.com/sns/latest/dg/SendMessageToHttp.html).

For webhooks to work automatically, the IAM user used to setup the connection must have the _**configure webhooks automatically**_ permissions (_see Required permissions above – under IAM policy for_ all features). If permissions has not been set, the repositories are connected but no webhooks are created.

While the new UI is not fully functional in AWS CodeCommits, users are required to create triggers via the old UI or with the API.

**Shorthand:**
With an existing AWS CC repository, enable triggers then create an SNS topic and subscribe to that topic.

For more information on Amazon SNS, see [**Amazon SNS: Getting Started »**](https://docs.aws.amazon.com/sns/latest/dg/sns-getting-started.html).



_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/5w5p0lbz77) _to open this video in a new browser tab for more viewing options._

## Using Full feature integration

This process requires an AWS account with existing CodeCommit repositories.

We recommend using the Full feature integrations panel (formerly Auto-connect integration panel) to connect multiple repositories from your AWS CodeCommit git host.

To connect your repository to Jira thru the Git Integration for Jira app, open the **Connect to Git Repository** wizard:

1.  On the Jira Cloud dashboard menu, go to **Apps** ➜ **Git Integration: Manage Git repositories**. The git configuration page for connecting repositories is displayed.

2.  On the Full feature integrations panel, click **AWS CodeCommit**. The Full feature integration wizard is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86180077/gitcloud-aws-cc-auto-connect-dlg(c).png?version=1&modificationDate=1599745472981&cacheVersion=1&api=v2)
    1.  Select the **Region** where the CodeCommit repositories reside then enter credentials for the **Access key ID** and **Secret access key**.

    2.  See below on the supported regions:

        *   AWS GovCloud (US)

        *   AWS GovCloud (US-East)

        *   US East (N. Virginia)

        *   US East (Ohio)

        *   US West (N. California)

        *   US West (Oregon)

        *   Canada (Central)

        *   EU (Ireland)

        *   EU (Frankfurt)

        *   EU (London)

        *   EU (Paris)

        *   EU (Stockholm)

        *   EU (Milan)

        *   Asia Pacific (Mumbai)

        *   Asia Pacific (Singapore)

        *   Asia Pacific (Sydney)

        *   Asia Pacific (Seoul)

        *   Asia Pacific (Tokyo)

        *   Asia Pacific (Hong Kong)

        *   Middle East (Bahrain)

        *   South America (Sao Paulo)

        *   China (Beijing)

        *   China (Ningxia)

        *   Africa (Capetown)

3.  Click **Connect** to continue. On the following screen, Git Integration for Jira app will read all available repositories from your AWS CodeCommit account. Click **Import repositories**.
    Repositories of the logged-in AWS CodeCommit user can be automatically connected to Jira Cloud. Repositories that are added or removed from AWS CodeCommit will be likewise connected or disconnected from Jira Cloud.

4.  After the import process, the **Settings** dialog is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86180077/gitcloud-autoconnect-projacl-pat-wizard(c).png?version=1&modificationDate=1599745473683&cacheVersion=1&api=v2)
    *   On the Integration Settings, setting the [Require User PAT option](/wiki/spaces/GITSERVER/pages/131170306) to `ON`, will require users to provide valid AWS Access Key ID and Secret Access Key for branch and pull requests creation/deletion _(via the_ [_developer panel_](/wiki/spaces/GITCLOUD/pages/1923025809/Jira+Git+integration+development+panel) _on the Jira issue page)_. The required permission must be configured for the service user to do specific tasks as described in the [Required permissions](#Required-permissions) section.

    *   Set Project Permissions according to your organization's project association rules.

5.  Click **Finish** to complete this setup.


The AWS CodeCommit repositories are now connected to Jira Cloud.

The Git Integration for Jira app supports tracked folders for AWS CodeCommit git repositories. The connected git host is scanned for existing repository folders. The found repositories can then be added to the Git Repositories configuration.

There are two ways to configure the git repository connection using tracked repositories with Git Integration for Jira Cloud:

*   connect via Full feature integrations panel ➜ **AWS CodeCommit**, or

*   connect via Connect to Git Repository dropdown ➜ **AWS CodeCommit**.


If the connected git host has newly added repositories, the Git Integration for Jira app will automatically add them to the git repositories configuration on the next reindex. For the deleted git repositories, these will be removed from the Git repositories configuration on the next reindex.

## Single repository (Manually connect via HTTP/HTTPS)

Connect a single AWS CodeCommit repository manually to Jira via HTTP/HTTPS connection.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/86180077/aws-cc-repo-home-portal-git-clone-url.png?version=1&modificationDate=1599745474156&cacheVersion=1&api=v2)

Use the host HTTP/HTTPS git clone URL from your AWS CodeCommit repository home portal. Click on the HTTPS (Clone URL column - column 1) and paste it on the Connect to Git Repository screen.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/86180077/gitcloud-app-gitmgr-connect2git-highlight.png?version=1&modificationDate=1599745474623&cacheVersion=1&api=v2)

1.  On your Jira Cloud dashboard menu, go to **Apps** ➜ **Git Integration: Manage Git repositories**,

2.  On the following screen, click **Connect to Git Repository**. The next screen is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86180077/gitcloud-connect-wizard-dlg(c).png?version=1&modificationDate=1599745475120&cacheVersion=1&api=v2)
3.  Click **Next** to proceed.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86180077/gitcloud-aws-cc-auto-connect-permisions(c).png?version=1&modificationDate=1599745475599&cacheVersion=1&api=v2)
4.  On the **Permissions** screen, set **Project Association** permissions, if required. Otherwise, leave it as is. Click **Connect** to continue to the next step.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/86180077/gitcloud-aws-cc-auto-connect-credentials(c).png?version=1&modificationDate=1599745476275&cacheVersion=1&api=v2)
    *   On the Authentication screen, enter _**Access key ID**_ and _**Secret access key**_.

5.  Click **Connect** to complete this setup.


The repository is now connected to Jira Cloud.

## Single repository (Manually connect via SSH)

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/xq1xzic0tm) _to open this video in a new browser tab for more viewing options._


Connect a single AWS CodeCommit repository manually to Jira via SSH connection.

SSH connections are handled automatically if the PUBLIC KEY was added in the AWS IAM console and the associated PRIVATE KEY was added/uploaded on the Jira side (_Manage Git repositories page_ ➜ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) _Actions_ ➜ _**Edit repository settings** with an SSH repository on the list_).

If authentication issues are encountered during connecting an AWS repository to Jira, modify the original URL by inserting the **SSH Key ID** as the username. The **SSH Key ID** is an alphanumeric sequence provided by AWS IAM when importing a PUBLIC KEY for a particular user account in IAM.

For example, the original URL is:

```java
ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/test-repo
```

If the SSH Key ID **1a2b3c4d5e** is applied to the original SSH URL, the resulting URL would be:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/86180077/aws-cc-ssh-codeline-example.png?version=1&modificationDate=1599745476751&cacheVersion=1&api=v2&width=633&height=52)

The modified URL can now be used as a valid repository URL via **Manage Git repositories** page ➜ **Connect to Git Repository**.

## Setting up AWS CodeCommit web links

The Git Integration for Jira app automatically configures web linking for AWS CodeCommit repositories connected via Full feature integration in Jira Cloud.

For single repository connections, configuring web linking is optional. For more information, see [Web linking documentation](/wiki/spaces/GITCLOUD/pages/1923025184/Web+linking).

## Viewing git commits in Jira Cloud

1.  Perform a git commit by adding the Jira issue key in the commit message. This will associate the commit to the mentioned Jira issue.

2.  Open the Jira issue.

3.  Scroll down to the _**Activity**_ panel then click the **Git Commits** tab.

4.  Click **View Full Commit** to view the code diff.


For detailed information on this process, see [Linking git commits to Jira issues](/wiki/spaces/GITCLOUD/pages/1923025229/Linking+git+commits+to+Jira+issues).

## Working with branches and pull requests

This section requires the necessary permissions for [all features](#all-features).

The Git Integration for Jira app supports creation of branches and pull requests from Jira via the developer panel.

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the  Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level. 

Main branch for repositories within an integration can only be changed on the git server.

### Creating branches

On your Jira Cloud, open a Jira issue. On the Jira Git development panel, click **Open Git Integration** then click **Create branch**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/86180077/gitcloud-aws-cc-create-branch-dlg.png?version=1&modificationDate=1599745477235&cacheVersion=1&api=v2)

**Pointers:**

1.  Select a **Repository** from the list.

    1.  The selected repository will display the git service logo to identify which git host it is located from.

    2.  If there are several repositories with the same name, the listed CodeCommit repositories will have their names attached with a region name. For example, `us-west-2/test-repo`.

    3.  Use the search box to look for the specific repository that will be used.

    4.  Optional – designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the [User settings](/wiki/spaces/GITCLOUD/pages/781975665/User+Settings) page.

2.  Choose the newly-created branch as the **Source branch**.

3.  Set _**master**_ as the **Target branch**.

4.  Enter a descriptive **Title** or leave it as is _(recommended)_.

5.  Click **Create Branch**.


The branch is created and can be viewed under the **Branches** tab in your AWS CodeCommit web portal.

### Creating pull requests

The pull request feature works the same as merge request.

On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Git integration**, click **Create Pull Request**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/86180077/gitcloud-aws-cc-create-pullreq-dlg.png?version=1&modificationDate=1599745477698&cacheVersion=1&api=v2)

**Pointers:**

1.  Select your working **Repository**.

    1.  The selected repository will display the git service logo to identify which git host it is located from.

    2.  If there are several repositories with the same name, the listed CodeCommit repositories will have their names attached with a region name. For example, `us-west-2/test-repo`.

    3.  Use the search box to look for the specific repository that will be used.

    4.  Optional – designate the repository to be the default selected repository for current Jira project.  To configure default repositories for more than one Jira project - use the [User settings](/wiki/spaces/GITCLOUD/pages/781975665/User+Settings) page.

2.  Set the **Source branch** to the newly-created branch.

3.  Set the **Target branch** to _**master**_.

4.  Give the pull request **Title** a descriptive name or leave it as is.

5.  Click **Create pull request** to create the pull request.


Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.


The pull request is listed on the developer panel of the Jira issue page.

The pull request is also ready for approval by the reviewers in your AWS CodeCommit web portal.

The branch and the pull request status are also displayed on the developer panel.

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