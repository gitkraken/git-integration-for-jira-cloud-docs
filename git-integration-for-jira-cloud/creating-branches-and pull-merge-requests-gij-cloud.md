---

title: Creating branches and pull/merge requests introduction
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<!-- INTRODUCTION TO GIT INTEGRATION -->

The Git Integration for Jira app adds two features on the Jira issue developer panel –  **Create branch**, and **Create pull/merge request**. For more information on where to access them, see the [Jira Git development panel documentation](/git-integration-for-jira-cloud/jira-git-integration-development-panel-gij-cloud).

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
       Pull/merge requests are still indexed based on branch name even if the PR/MR title does not have the Jira issue key – as long as the branch name contains the Jira issue key.
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

### Default branch

Most git integrations allow changing of the default branch of the repository/project other than "master".  This change is reflected in the Repository Settings of the Git Integration for Jira app on the next reindex. Full feature integrations support this feature where Git Integration for Jira app gets the default branch from almost all integrations and apply this setting at repository level. For the case with Gerrit, the default main branch is always “master”.

Main branch for repositories within an integration can only be changed on the git server.

### Creating branches

Open a Jira issue then on the developer panel, click **Create Branch** label to create a branch for the selected repository.

For detailed information on this feature, see [Creating branches from Jira](/git-integration-for-jira-cloud/create-branch-gij-cloud).

### Creating pull/merge requests

Open a Jira issue then on the developer panel, click **Create pull/merge request** label to create a pull/merge request for the selected repository.

For detailed information on this feature, see [Creating pull/merge requests from Jira](/git-integration-for-jira-cloud/creating-branches-and%20pull-merge-requests-gij-cloud)

&nbsp;
* * *

[Prev: Using Repository Browser](/git-integration-for-jira-cloud/using-the-repository-browser-gij-cloud/)


### More git service specific integration guides

[GitHub.com](/git-integration-for-jira-cloud/github-com-gij-cloud/) (Git Integration for Jira Cloud)

[GitHub Enterprise](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud/) (Git Integration for Jira Cloud)

[GitLab.com](/git-integration-for-jira-cloud/gitlab-com-gij-cloud/) (Git Integration for Jira Cloud)

[GitLab CE/EE](/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud/) (Git Integration for Jira Cloud)

[Azure DevOps/VSTS](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud/) (Git Integration for Jira Cloud)

[Azure DevOps Server/TFS](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud/) (Git Integration for Jira Cloud)

[AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommit-gij-cloud/) (Git Integration for Jira Cloud)

[Gerrit](/git-integration-for-jira-cloud/gerrit-gij-cloud/) (Git Integration for Jira Cloud)

[Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-cloud-gij-cloud/) (Git Integration for Jira Cloud)

[Webhook indexing integration](/git-integration-for-jira-cloud/webhook-indexing-integration-gij-cloud/) (Git Integration for Jira Cloud)

