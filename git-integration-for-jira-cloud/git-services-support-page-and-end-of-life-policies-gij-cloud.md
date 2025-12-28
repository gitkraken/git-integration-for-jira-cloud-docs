---

title: Git Services Support Page and End-of-Life Policies
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Git Integration for Jira app currently supports all the cloud hosted versions and the officially supported versions of the self-hosted git services:

- [GitHub Enterprise](#github-enterprise-eol)
- [GitLab CE/EE](#gitlab-ceee-eol-support-policy)
- [Bitbucket Server/Cloud](#bitbucket-servercloud-eol-support-policy)
- [Azure DevOps Server / TFS](#azure-devops-server-lifecycle-policies)
- [Gerrit](#gerrit-end-of-life-eol)

Most offered services have their own End-of-Life (EOL) policies that ranges from one year or more. For most cases, it's generally one year following its release date.

&nbsp;

* * *

&nbsp;

## GitHub Enterprise (EOL)

The End-of-life (EOL) for a major release of GitHub Enterprise server is generally one year following its release date.

For example, GitHub Enterprise Server 2.16.0 was released on January 22, 2019 and had an EOL date of January 22, 2020. Similarly, 2.17.0 was released on May 23, 2019 and had an EOL date of May 23, 2020.

GitHub's [**Releases page**](https://enterprise.github.com/releases) can be used to get these dates, as well as release notes for any given version. EOL notices are also published [at the top of documentation pages](https://docs.github.com/en/enterprise/2.17) for their respective version, as well as in the [**Release notes** for patches leading up to EOL](https://enterprise.github.com/releases/2.17.25/notes).

&nbsp;

* * *

&nbsp;

## GitLab CE/EE EOL Support Policy

GitLab's current policy is to support one stable release at any given time, but for medium-level security issues, GitLab may backport security fixes to the previous two monthly releases. For critical security issues, there is precedent to backport security fixes to even more monthly releases of GitLab. This decision is made on a case-by-case basis.

The patch releases **only include bug fixes** for the current stable released version of GitLab.

These two policies are in place because:

1.  GitLab has Community and Enterprise distributions, doubling the amount of work necessary to test/release the software.

2.  Backporting to more than one release creates a high development, quality assurance, and support cost.

3.  Supporting parallel version discourages incremental upgrades which over time accumulate in complexity and create upgrade challenges for all users. GitLab has a dedicated team ensuring that incremental upgrades (and installations) are as simple as possible.

4.  The number of changes created in the GitLab application is high, which contributes to backporting complexity to older releases. In several cases, backporting has to go through the same review process a new change goes through.

5.  Ensuring that tests pass on the older release is a considerable challenge in some cases, and as such is very time-consuming.

For more informaiton, see [GitLab releases](https://about.gitlab.com/releases/categories/releases/).

&nbsp;

* * *

&nbsp;

## Bitbucket Server/Cloud EOL Support Policy

### Bitbucket Server

End of life support for the latest version, older versions and supported platforms are listed in the [Bitbucket EOL support announcement page](https://confluence.atlassian.com/bitbucketserver/end-of-support-announcements-for-bitbucket-server-776640855.html).

### Bitbucket Cloud

Atlassian occasionally remove existing features and functions from Bitbucket Cloud in order to provide the best user experience possible. An advanced notice is provided to everyone using a feature before support is ended for that feature. For more information, see [Bitbucket Cloud EOL support announcement](https://support.atlassian.com/bitbucket-cloud/docs/view-end-of-support-announcements-for-bitbucket-cloud/).

&nbsp;

* * *

&nbsp;

## Azure DevOps Server Lifecycle Policies

For information on product lifecycle and policies, see the topic links below:

**Search product lifecycle**
[https://docs.microsoft.com/en-us/lifecycle/products/](https://docs.microsoft.com/en-us/lifecycle/products/)

**Microsoft Fixed Lifecycle policy**
[https://docs.microsoft.com/en-us/lifecycle/policies/fixed](https://docs.microsoft.com/en-us/lifecycle/policies/fixed)

**Microsoft Modern Lifecycle policy**
[https://docs.microsoft.com/en-us/lifecycle/policies/modern](https://docs.microsoft.com/en-us/lifecycle/policies/modern)

&nbsp;

* * *

&nbsp;

## Gerrit End of Life (EOL)

The Gerrit open-source community actively supports the last 2 releases on a best effort basis. Older releases are not actively maintained but may still receive important fixes (e.g. security fixes), but there is no guarantee for this. Which fixes are backported to these old releases is decided on a case by case basis.

For more information, see [Gerrit support page](https://www.gerritcodereview.com/support.html).

End of life for old release happens implicitly when a new Gerrit version is released, and is announced via the [project news](https://www.gerritcodereview.com/news.html).

