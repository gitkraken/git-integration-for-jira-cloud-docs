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


The **Git service integration** (formerly auto-connect/full feature integration) allows administrators to setup multiple repositories for integration with Jira. This is the recommended way and offers features not found in other integration types. _If you are behind a firewall, you need to_ [_whitelist the app_](/wiki/spaces/GITCLOUD/pages/121241614/Allow+list+%28whitelist%29+BigBrassBand+Cloud) _to get it to work._

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

*   [GitHub.com and GitHub Enterprise (Cloud)](/wiki/spaces/GITCLOUD/pages/82477058/GitHub.com)

*   [GitHub Enterprise Server](/wiki/spaces/GITCLOUD/pages/85622870/GitHub+Enterprise+Server)

*   [GitLab.com](/wiki/spaces/GITCLOUD/pages/85622895/GitLab.com)

*   [GitLab CE/EE](/wiki/spaces/GITCLOUD/pages/85524528)

*   [Azure DevOps | Visual Studio Team Services (VSTS)](/wiki/spaces/GITCLOUD/pages/86278279)

*   [Azure DevOps Server | Team Foundation Services (TFS)](/wiki/spaces/GITCLOUD/pages/86409345)

*   [AWS CodeCommit](/git-integration-for-jira-cloud/AWS-CodeCommit)

*   [Bitbucket Cloud](/git-integration-for-jira-cloud/Bitbucket-Cloud)

*   [Gerrit](/git-integration-for-jira-cloud/Gerrit)


### Webhook indexing integration

*   [GitHub](/wiki/spaces/GITCLOUD/pages/1494646787/GitHub+webhook+indexing+integration)

*   [GitLab](/wiki/spaces/GITCLOUD/pages/1503494176/GitLab+webhook+indexing+integration)

*   [Microsoft](/wiki/spaces/GITCLOUD/pages/1509032469/Microsoft+webhook+indexing+integration)

*   [Gerrit](/wiki/spaces/GITCLOUD/pages/1647116289/Gerrit+webhook+indexing+integration) (_guide coming soon_)


### Single repository integration

*   [HTTP/HTTPS integration](/wiki/spaces/GITCLOUD/pages/923238448)

*   [SSH integration](/wiki/spaces/GITCLOUD/pages/923238489)


###
Setup next features to improve Git user experience

*   Page:

    [Setting up web links](/wiki/spaces/GITCLOUD/pages/923566197/Setting+up+web+links) (Git Integration for Jira Cloud)

*   Page:

    [Link git commits to Jira issue](/wiki/spaces/GITCLOUD/pages/923238543/Link+git+commits+to+Jira+issue) (Git Integration for Jira Cloud)

*   Page:

    [Using Smart Commits](/wiki/spaces/GITCLOUD/pages/923664519/Using+Smart+Commits) (Git Integration for Jira Cloud)

*   Page:

    [Using the Repository Browser](/wiki/spaces/GITCLOUD/pages/923664546/Using+the+Repository+Browser) (Git Integration for Jira Cloud)

*   Page:

    [Creating branches and pull | merge requests](/wiki/spaces/GITCLOUD/pages/923566251/Creating+branches+and+pull+%7C+merge+requests) (Git Integration for Jira Cloud)