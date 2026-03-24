---
title: "Introduction to Git integration"
description: "Learn how to integrate Git repositories with Jira Cloud"
product: "Git Integration for Jira Cloud"
feature: "Introduction to Git integration"
content_type: "concept"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "concept", "admin"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Learn basic integration for most git hosts by connecting git repositories to Jira Cloud. This page contains information about the different integration types and how to get started.

<img src='/wp-content/uploads/gij-instant-integration-process.png' style='display:block;margin:25px auto;max-width:100%' width=500px /> 

The Git Integration for Jira Cloud app offers three integration types:

| Integration type | Best for | Repository scope | Key limitation or note |
| :--- | :--- | :--- | :--- |
| Git service integration | Connecting multiple repositories from supported cloud-hosted or self-hosted git services | Multiple repositories | Recommended path; may require allowlisting when the git host is behind a firewall |
| Webhook indexing integration | Git servers behind a firewall that can send outbound webhook requests | Multiple repositories | Does not support creating branches or pull/merge requests inside Jira |
| Single repository integration (Plain Git) | Connecting one specific repository over SSH or HTTP(S) | Single repository | Best for one-off or protocol-specific connections rather than full multi-repository setup |

**Git service integration (recommended)**

The **Git service integration** (formerly auto-connect/full feature integration) allows administrators to set up multiple repositories for integration with Jira. This is the recommended method and offers features not found in other integration types. _If you are behind a firewall, you need to_ [_whitelist the app_](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud/) _to get it to work._

**Webhook indexing integration (special cases)**

The **Webhook indexing integration** allows administrators to integrate multiple repositories behind a firewall. However, this integration type does not support creating branches or pull/merge requests inside Jira.

**Single repository integration (plain git)**

The **Single repository integration** setup is ideal for users who use SSH connections or only connect a single specific repository.

&nbsp;

### Getting Started

**Integration basics checklist:**

*   Connect multiple or single git repositories to Jira
*   Learn how to associate git commits to Jira issues
*   Learn about smart commits
*   Learn how to create branches and pull/merge requests inside Jira via the developer panel
*   <b style='background-color:#006745; padding:1px 5px; color:#E2FCEF; border-radius:3px; margin: 0 5px; font-size: small;'>NEW!</b> Post integration: Perform administrator toolbox tasks to discover helpful features and improve your Jira + Git experience

&nbsp;

### How to choose the integration setup path

Connect your git repositories via **Add integration** (_Apps_ ➜ _Git integration: Manage integrations_ ➜ _Add integration_). Start by following the steps for your preferred git host service:

&nbsp;

#### Git Service Integration

*   [GitHub.com and GitHub Enterprise (Cloud)](/git-integration-for-jira-cloud/github-com-gij-cloud)

*   [GitHub Enterprise Server](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud)

*   [GitLab.com](/git-integration-for-jira-cloud/gitlab-com-gij-cloud)

*   [GitLab CE/EE](/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud)

*   [Azure DevOps | Visual Studio Team Services (VSTS)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud)

*   [Azure DevOps Server | Team Foundation Services (TFS)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud)

*   [AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommit-gij-cloud)

*   [Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-cloud-gij-cloud)

*   [Gerrit](/git-integration-for-jira-cloud/Gerrit-gij-cloud)

&nbsp;

#### Webhook Indexing Integration

*   [GitHub](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud)

*   [GitLab](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud)

*   [Microsoft](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud)

*   Gerrit <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>GUIDE UNDER CONSTRUCTION</b>

<!-- [Gerrit](/git-integration-for-jira-cloud/gerrit-webhook-indexing-integration-gij-cloud/) -->

&nbsp;

#### Single Repository Integration

*   [HTTP/HTTPS integration](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

*   [SSH integration](/git-integration-for-jira-cloud/connecting-ssh-git-repositories-jira-cloud-gij-cloud)

&nbsp;

### Improve Your Git User Experience

*   [Setting up web links](/git-integration-for-jira-cloud/setting-up-web-links-gij-cloud)

*   [Link git commits to Jira issue](/git-integration-for-jira-cloud/link-git-commits-to-jira-issue-gij-cloud)

*   [Using Smart Commits](/git-integration-for-jira-cloud/using-smart-commits-gij-cloud)

*   [Using the Repository Browser](/git-integration-for-jira-cloud/using-the-repository-browser-gij-cloud)

*   [Creating branches and pull | merge requests](/git-integration-for-jira-cloud/creating-branches-and-pull-merge-requests-gij-cloud)

&nbsp;
* * *
&nbsp;

[**Back to:** Integration guides index](/git-integration-for-jira-cloud/integration-guide-gij-cloud/)

[**Next:** Connecting to a Single Git Repository (HTTP/HTTPS)](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https-gij-cloud)

<p>&nbsp;</p>

