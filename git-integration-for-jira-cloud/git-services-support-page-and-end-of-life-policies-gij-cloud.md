---
title: Git Services Support Page and End-of-Life Policies
description: End-of-life policies and support information for git services supported by Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

Git Integration for Jira app supports all cloud-hosted versions and officially supported versions of self-hosted git services.

**On this page:**
- [GitHub Enterprise](#github-enterprise)
- [GitLab CE/EE](#gitlab-ceee)
- [Bitbucket Server/Cloud](#bitbucket-servercloud)
- [Azure DevOps Server / TFS](#azure-devops-server--tfs)
- [Gerrit](#gerrit)

Most services have End-of-Life (EOL) policies ranging from one year or more following the release date.

&nbsp;
* * *
&nbsp;

## GitHub Enterprise

GitHub Enterprise Server EOL is generally one year following its release date.

**Examples:**
- GitHub Enterprise Server 2.16.0 released January 22, 2019 → EOL January 22, 2020
- GitHub Enterprise Server 2.17.0 released May 23, 2019 → EOL May 23, 2020

**Resources:**
- [GitHub Releases page](https://enterprise.github.com/releases) for release dates and notes
- [Documentation pages](https://docs.github.com/en/enterprise/2.17) for EOL notices
- [Release notes](https://enterprise.github.com/releases/2.17.25/notes) for patch announcements

&nbsp;
* * *
&nbsp;

## GitLab CE/EE

GitLab supports one stable release at any given time on a best-effort basis.

**Security fix backporting:**
- Medium-level issues: May be backported to the previous two monthly releases
- Critical issues: May be backported to additional releases (case-by-case basis)

Patch releases include only bug fixes for the current stable version.

**Reasons for limited backporting:**
1. Community and Enterprise distributions double testing/release work
2. Backporting to multiple releases creates high development, QA, and support costs
3. Supporting parallel versions discourages incremental upgrades
4. High volume of changes increases backporting complexity
5. Ensuring tests pass on older releases is time-consuming

For more information, see [GitLab releases](https://about.gitlab.com/releases/categories/releases/).

&nbsp;
* * *
&nbsp;

## Bitbucket Server/Cloud

### Bitbucket Server

See [Bitbucket Server EOL support announcements](https://confluence.atlassian.com/bitbucketserver/end-of-support-announcements-for-bitbucket-server-776640855.html) for the latest version support and supported platforms.

### Bitbucket Cloud

Atlassian provides advance notice before ending support for features. See [Bitbucket Cloud EOL support announcements](https://support.atlassian.com/bitbucket-cloud/docs/view-end-of-support-announcements-for-bitbucket-cloud/) for current information.

&nbsp;
* * *
&nbsp;

## Azure DevOps Server / TFS

**Lifecycle resources:**
- [Search product lifecycle](https://docs.microsoft.com/en-us/lifecycle/products/)
- [Microsoft Fixed Lifecycle policy](https://docs.microsoft.com/en-us/lifecycle/policies/fixed)
- [Microsoft Modern Lifecycle policy](https://docs.microsoft.com/en-us/lifecycle/policies/modern)

&nbsp;
* * *
&nbsp;

## Gerrit

The Gerrit open-source community actively supports the last 2 releases on a best-effort basis. Older releases may receive important fixes (such as security fixes) but without guarantee. Backporting decisions are made case by case.

EOL for old releases happens implicitly when a new Gerrit version is released and is announced via the [project news](https://www.gerritcodereview.com/news.html).

For more information, see the [Gerrit support page](https://www.gerritcodereview.com/support.html).

<kbd>Last updated: December 2025</kbd>
