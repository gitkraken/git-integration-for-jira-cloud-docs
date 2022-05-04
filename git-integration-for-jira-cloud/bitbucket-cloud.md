---

title: Bitbucket Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Bitbucket Cloud

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/86343820/Bitbucket+Cloud>

* * *

  

Using **Jira Server or Data Center**? [See the corresponding article](https://bigbrassband.atlassian.net/wiki/x/JoDSB).

![](https://bigbrassband.com/confluence/images/bitbucket-banner-logo.png)

**Integrate Bitbucket Cloud with Jira Cloud**

  

Quickly learn how to connect Bitbucket Cloud git repositories via Git Integration for Jira Cloud app.

**What's on this page:**

  

* * *

  

  

  

## **Using Full feature integration**

We recommend using the Full feature integrations panel to connect multiple repositories from your Bitbucket Cloud account.

1.  On your Jira dashboard menu, go to **Apps** ➜ **Git Integration: Manage Git repositories**.
2.  Click **Bitbucket** on the **_Full feature integrations_** panel..
3.  Login to your Bitbucket Cloud account if prompted.
4.  Grant **OAuth access** for Git Integration for Jira Cloud app when prompted.
5.  On the following screen, click **Next** to import repositories.
6.  On the following screen, set **Project permissions** according to your organization's rules.
7.  Click **Connect** to complete this setup.

Bitbucket Cloud repositories are now connected to Jira Cloud.

  

## **Single repository connection**

Obtain the repository URL from the Bitbucket Cloud repository project page. Choose between SSH or HTTPS.

1.  On your Jira dashboard menu, go to **Apps** ➜ **Git Integration: Manage Git repositories**.
2.  Click **Connect to Git Repository** to open the Connect Wizard.
3.  Paste the URL from Bitbucket Cloud in the provided box.
4.  Continue to the next step by following the screen instructions.
5.  Click **Finish** to complete this process. 

The repository is now connected to Jira Cloud.

  

## **Permissions**

Set Bitbucket Cloud permissions according to your organization's rules. Viewing commits from Jira requires at least **Read** or **View** repository permissions. For branch/merge request creation, set specific service users with **Write** permissions.

  

## **Viewing git commits in Jira Cloud**

1.  Perform a git commit by adding the Jira issue key in the commit message.  This will associate the commit to the mentioned Jira issue.
2.  Open the Jira issue.
3.  Scroll down to the **_Activity_** panel then click the **Git Commits** tab.
4.  Click **View Full Commit** to view the code diff.

For more information about this feature, see [Documentation: Linking git commits to Jira issues](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923025229 "/wiki/spaces/GITCLOUD/pages/1923025229").

  

## **Creating branches and pull/merge requests**

The Git Integration for Jira Cloud app adds two features on the Jira issue developer panel – **Create Branch**, and **Create Pull/Merge Request**. For more information about the developer panel, see the **[Jira Git development panel documentation](/wiki/spaces/GITCLOUD/pages/1923025809/Jira+Git+integration+development+panel)**.

### **Default Branch**

Most git integrations allow changing of the default branch of the repository/project other than "master". This change is reflected in the  Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this function where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level. 

  

Main branch for repositories within an integration can only be changed on the git server.

### **Creating branches**

On your Jira Cloud, open a Jira issue. On the Jira Git integration development panel, click **Open** **Git Integration** then click **Create branch**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/86343820/gitcloud-bitbucket-create-branch-dlg.png?version=1&modificationDate=1601463635612&cacheVersion=1&api=v2)

**Pointers:**

1.  Select a **Repository** from the list.
    
    1.  The selected repository will display the git service logo to identify which git host it is located from.
    2.  If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.
        
    3.  Use the search box to look for the specific repository that will be used.
        
    4.  Optional – designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the **User settings** page.
        
2.  Choose a **Base branch**.
    
3.  The Git Integration app will populate the **Branch name** field according to the _Branch Name Template_ declared in the **[Git integration options »](/wiki/spaces/GITCLOUD/pages/1207829137/Git+integration+options)** via **General Settings**. Enter a descriptive name or leave it as is (recommended).

  

For more detailed information on this feature, see [**Create branch**](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/733282366/Create+branch).

The newly-created branch is now listed in the developer panel under **Branches**. Perform a commit to the newly-created branch to be ready for merge.

### **Creating pull/merge requests**

The pull request feature works the same as merge request. On your Jira Cloud, open the Jira issue where your previously created a branch. On the developer panel under **Git Integration**, click **Create pull request**. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/86343820/gitcloud-bitbucket-create-pull-req-dlg.png?version=1&modificationDate=1601464089328&cacheVersion=1&api=v2)

**Pointers:**

1.  Select a **Repository** from the list.
    
    1.  The selected repository will display the git service logo to identify which git host it is located from.
        
    2.  If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, BigBrassBand/second-webhook-test-repo.
        
    3.  Use the search box to look for the specific repository that will be used.
        
    4.  Optional – designate the repository to be the default selected repository for current Jira project. To configure default repositories for more than one Jira project - use the **User settings** page.
        
2.  Choose the newly-created branch as the **Source branch**.
    
3.  Set _**master**_ as the **Target branch**.
    
4.  Enter a descriptive **Title** or leave it as is _(recommended)_.
    

  

**Preview** allows you to see the comparison view of the current changes in the selected **Source branch** vs **Target branch** (_usually_ _master_).

  

  

For more detailed information on this feature, see [**Create pull/merge request**](/wiki/spaces/GITCLOUD/pages/733315235/Create+pull+or+merge+request).

Index trigger

Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.

The pull request is listed on the developer panel of the Jira issue page.

The pull request is also ready for approval by the reviewers in your GitHub web portal.

Access the **Create branch** and **Create pull/merge request** features in the Jira issue developer panel.  For more information, see **[Jira Git integration development panel](/wiki/spaces/GITCLOUD/pages/1923025809/Jira+Git+integration+development+panel)**.

  

  

* * *

## More Integration Guides

page icon as list [Integrate GitHub.com with Jira Cloud](/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com)

page icon as list [Integrate GitHub Enterprise with Jira Cloud](/wiki/spaces/GITCLOUD/pages/85622870/GitHub+Enterprise+Server)

page icon as list [Integrate GitLab.com with Jira Cloud](/wiki/spaces/GITCLOUD/pages/85622895/GitLab.com)

page icon as list [Integrate GitLab CE/EE with Jira Cloud](/wiki/spaces/GITCLOUD/pages/85524528)

page icon as list [Integrate Azure DevOps/VSTS with Jira Cloud](/wiki/spaces/GITCLOUD/pages/86278279)

page icon as list [Integrate Azure DevOps Server/TFS with Jira Cloud](/wiki/spaces/GITCLOUD/pages/86409345)

page icon as list [Integrate AWS CodeCommit with Jira Cloud](/wiki/spaces/GITCLOUD/pages/86180077/AWS+CodeCommit)

page icon as list [Integrate Gerrit with Jira Cloud](/wiki/spaces/GITCLOUD/pages/86474926/Gerrit)