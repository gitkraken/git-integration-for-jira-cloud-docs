---

title: Introduction to Git integration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
**Covers release** 25 Mar 2022


Learn basic integration for most git hosts by connecting git repositories to Jira Cloud. This page contains simple

## Introduction

The Git Integration for Jira Cloud app offers three (3) types of integration, namely:

*   Git service integration (recommended)

*   Webhook indexing integration (special cases)

*   Single repository integration (plain git)


The **Git service integration** (formerly auto-connect/full feature integration) allows administrators to setup multiple repositories for integration with Jira. This is the recommended way and offers features not found in other integration types. _If you are behind a firewall, you need to_ [_whitelist the app_](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud/) _to get it to work._

The **Webhook indexing integration** allows administrators to integrate multiple repositories behind a firewall. However, this type of integration does not support creating branches or pull/merge request inside Jira.

The **Single repository integration** setup is ideal for users who are using SSH connections or only connect a single specific repository.

## Getting started

**Integration basics checklist:**

*   Connect multiple or single git repositories to Jira;
*   Find out how to associate git commits to a Jira issue(s);
*   Know more about smart commits;
*   Learn how to create branch/pull/merge request inside Jira via the developer panel; and
*   COMING SOON Post integration: Perform administrator toolbox tasks to discover helpful features and improve your Jira + Git experience.

## Integration setup

Connect your git repositories via **Add integration** (_Apps_ ➜ _Git integration: Manage integrations_ ➜ _Add integration_). Start by following the steps for your favorite git host service:

### Git service integration

*   [GitHub.com and GitHub Enterprise (Cloud)](/git-integration-for-jira-cloud/github-com/)

*   [GitHub Enterprise Server](/git-integration-for-jira-cloud/github-enterprise-server/)

*   [GitLab.com](/git-integration-for-jira-cloud/gitlab-com/)

*   [GitLab CE/EE](/git-integration-for-jira-cloud/gitlab-ce-ee/)

*   [Azure DevOps | Visual Studio Team Services (VSTS)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts/)

*   [Azure DevOps Server | Team Foundation Services (TFS)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs/)

*   [AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommit-gij-cloud/)

*   [Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-cloud/)

*   [Gerrit](/git-integration-for-jira-cloud/Gerrit)


### Webhook indexing integration

*   [GitHub](/git-integration-for-jira-cloud/github-webhook-indexing-integration/)

*   [GitLab](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration/)

*   [Microsoft](/git-integration-for-jira-cloud/github-webhook-indexing-integration/)

*   [Gerrit](/git-integration-for-jira-cloud/gerrit-webhook-indexing-integration/) (_guide coming soon_)


### Single repository integration

*   [HTTP/HTTPS integration](/git-integration-for-jira-cloud/connecting-to-a-single-git-repository-http-https/)

*   [SSH integration](/connecting-to-a-single-git-repository-ssh/)


###
Setup next features to improve Git user experience

*   [Setting up web links](/git-integration-for-jira-cloud/setting-up-web-links-gij-cloud/) (Git Integration for Jira Cloud)

*   [Link git commits to Jira issue](/git-integration-for-jira-cloud/link-git-commits-to-jira-issue/) (Git Integration for Jira Cloud)

*   [Using Smart Commits](/git-integration-for-jira-cloud/using-smart-commits/) (Git Integration for Jira Cloud)

*   [Using the Repository Browser](/git-integration-for-jira-cloud/using-the-repository-browser/) (Git Integration for Jira Cloud)

*   [Creating branches and pull | merge requests](/git-integration-for-jira-cloud/creating-branches-and-pull-merge-requests/) (Git Integration for Jira Cloud)