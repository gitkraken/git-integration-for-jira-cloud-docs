---
title: Git Services Support Page and End-of-Life Policies
description: End-of-life policies and support information for git services compatible with Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

Git Integration for Jira Cloud supports all cloud-hosted versions and officially supported versions of self-hosted git services.

**On this page:**
- [GitHub Enterprise](#github-enterprise-eol)
- [GitLab CE/EE](#gitlab-ceee-eol-support-policy)
- [Bitbucket Server/Cloud](#bitbucket-servercloud-eol-support-policy)
- [Azure DevOps Server / TFS](#azure-devops-server-lifecycle-policies)
- [Gerrit](#gerrit-end-of-life-eol)

Most git services have End-of-Life (EOL) policies ranging from one year or more following the release date.

&nbsp;
* * *
&nbsp;

## GitHub Enterprise EOL

GitHub Enterprise Server EOL is generally one year following its release date.

**Examples:**
- GitHub Enterprise Server 2.16.0: Released January 22, 2019 → EOL January 22, 2020
- GitHub Enterprise Server 2.17.0: Released May 23, 2019 → EOL May 23, 2020

**Resources:**
- [GitHub Releases page](https://enterprise.github.com/releases) for release dates and notes
- [Documentation pages](https://docs.github.com/en/enterprise/2.17) for EOL notices
- [Release notes](https://enterprise.github.com/releases/2.17.25/notes) for EOL announcements

&nbsp;
* * *
&nbsp;

## GitLab CE/EE EOL Support Policy

GitLab supports one stable release at a time. For security issues, GitLab may backport fixes:

| Security Level | Backport Policy |
|----------------|-----------------|
| Medium | May backport to previous two monthly releases |
| Critical | May backport to additional monthly releases (case-by-case) |

Patch releases include only bug fixes for the current stable version.

**Why this policy exists:**
- Community and Enterprise distributions double testing/release work
- Backporting to multiple releases creates high development and support costs
- Supporting parallel versions discourages incremental upgrades
- High volume of changes makes backporting complex

For more information, see [GitLab releases](https://about.gitlab.com/releases/categories/releases/).

&nbsp;
* * *
&nbsp;

## Bitbucket Server/Cloud EOL Support Policy

### Bitbucket Server

See the [Bitbucket EOL support announcement page](https://confluence.atlassian.com/bitbucketserver/end-of-support-announcements-for-bitbucket-server-776640855.html) for:
- Latest version support
- Older version support
- Supported platforms

### Bitbucket Cloud

Atlassian provides advance notice before removing features. See [Bitbucket Cloud EOL support announcements](https://support.atlassian.com/bitbucket-cloud/docs/view-end-of-support-announcements-for-bitbucket-cloud/).

&nbsp;
* * *
&nbsp;

## Azure DevOps Server Lifecycle Policies

**Microsoft lifecycle resources:**

- [Search product lifecycle](https://docs.microsoft.com/en-us/lifecycle/products/)
- [Microsoft Fixed Lifecycle policy](https://docs.microsoft.com/en-us/lifecycle/policies/fixed)
- [Microsoft Modern Lifecycle policy](https://docs.microsoft.com/en-us/lifecycle/policies/modern)

&nbsp;
* * *
&nbsp;

## Gerrit End of Life (EOL)

The Gerrit open-source community actively supports the last 2 releases on a best-effort basis. Older releases may receive important fixes (such as security fixes), but there is no guarantee.

EOL for old releases occurs when a new Gerrit version is released and is announced via [project news](https://www.gerritcodereview.com/news.html).

For more information, see the [Gerrit support page](https://www.gerritcodereview.com/support.html).

<kbd>Last updated: December 2025</kbd>
