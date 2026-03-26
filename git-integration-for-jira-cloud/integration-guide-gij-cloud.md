---
title: "Integration Guide"
description: "Guide to connecting Git repositories with Jira Cloud using Git Integration for Jira"
product: "Git Integration for Jira Cloud"
feature: "Integration Guide"
content_type: "integration"
audience: "developer"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "User"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "integration", "developer"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

The Integration Guide helps Jira administrators choose the right setup document for each supported git host in Git Integration for Jira Cloud. Use this page when you need the correct host-specific guide for GitHub, GitLab, Azure DevOps, Bitbucket, AWS CodeCommit, or a Plain Git repository.

| Git host or setup path | Best for | Typical integration method | Start here when you need |
| :--- | :--- | :--- | :--- |
| GitHub and GitLab | Cloud-hosted or self-hosted git services with multi-repository support | Git service integration | OAuth or PAT-based setup guidance |
| Azure DevOps or TFS | Microsoft-hosted or self-hosted repositories | Git service integration or webhook indexing | Microsoft-specific setup and repository selection steps |
| AWS CodeCommit and Bitbucket Cloud | Service-specific connection requirements | Git service integration or HTTP/SSH | Provider-specific authentication and repository setup steps |
| Plain Git repository | One SSH or HTTP(S) repository | Single repository integration | Direct repository connection outside the multi-repository flows |

For a comparison of integration types before choosing a git-host guide, see **[Introduction to Git integration](/git-integration-for-jira-cloud/introduction-to-git-integration-gij-cloud)**.

## How to choose the right Git Integration for Jira Cloud guide

Select the git host that matches the repository platform you want to connect. If you need to connect only one repository over SSH or HTTP(S), use the Plain Git repository guide instead of the multi-repository host guides.

<br>

* * *

<img src='/wp-content/uploads/gij-gitlab-mobile.png' width=40 height=40 style='display:inline-block;margin:15px 10px 0 0;' /> [**GitLab.com**](/git-integration-for-jira-cloud/gitlab-com-gij-cloud)<sup>1</sup>

Connect your GitLab.com remote repositories via the Connect to Git Repository wizard or Connect to GitLab wizard.

* * *

<img src='/wp-content/uploads/gij-gitlab-icon-ee32.png' width=40 height=40 style='display:inline-block;margin:15px 10px 0 0;' /> [**GitLab CE/EE Server**](/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud)<sup>1</sup>

Connect and manage multiple GitLab server repositories at once via the **Connect to GitLab wizard** and the **Show connected repositories** dialog.

* * *

<img src='/wp-content/uploads/github-mobile-dark.png' width=40 height=40  style='display:inline-block;margin:15px 10px 0 0;' /> [**GitHub.com**](/git-integration-for-jira-cloud/github-com-gij-cloud)

Connect your GitHub remote repositories via the Connect to Git Repository Wizard.

* * *

<img src='/wp-content/uploads/gij-github-ent-64.png' width=40 height=40  style='display:inline-block;margin:15px 10px 0 0;' /> [**GitHub Enterprise Server**](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud)

Connect your GitHub Enterprise remote repositories via the Connect to Git Repository Wizard.

* * *

<img src='/wp-content/uploads/gij-vsts-azure-devops-logo2.png' width=40 height=40  style='display:inline-block;margin:15px 10px 0 0;' /> [**VSTS / Azure DevOps**](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud)

Connect to Visual Studio Team Services (VSTS) / Azure DevOps via the Auto-Connect integration panel in Manage Git Repositories.

* * *

<img src='/wp-content/uploads/gij-tfs-icon.png' width=40 height=40  style='display:inline-block;margin:15px 10px 0 0;' /> [TFS / Azure DevOps Server](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud)

Connect to Team Foundation Server (TFS) / Azure DevOps Server via the Auto-Connect integration panel in Manage Git Repositories.

* * *

<img src='/wp-content/uploads/gij-aws-codecommit-icon.png' width=40 height=40  style='display:inline-block;margin:15px 10px 0 0;' /> [AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommit-gij-cloud)

Connect your AWS CodeCommit repositories via the Git Integration for Jira app in Jira Cloud.

* * *

<img src='/wp-content/uploads/gij-bitbucket-mobile.png' width=44 height=40  style='display:inline-block;margin:15px 10px 0 0;' /> [Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-cloud-gij-cloud)

Integrate Bitbucket Cloud git repositories via the Git Integration for Jira app using HTTP/SSH connection.

* * *

<img src='/wp-content/uploads/gij-bonobo-icon.png' width=40 height=40  style='display:inline-block;margin:15px 10px 0 0;' /> [Plain Git repository](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

Connect plain git repositories via the Git Integration for Jira app in Jira Cloud.

&nbsp;

<br>
<br>
<div style='border-top: 1px solid #456; width: 40%; padding-bottom: 12px'></div>
<div style='font-size: 12px;'>
    <sup>1</sup> <i>Logo owned by <a href='https://gitlab.com/'>GitLab Inc</a> used under <a href='https://creativecommons.org/licenses/by-nc-sa/4.0/'>license</a>.
    <p>&nbsp;&nbsp;All product names, logos, and brands are property of their respective owners.<p><i>
</div>

<p>&nbsp;</p>
