---

title: Repository Browser - Viewing all repositories
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
**Default Settings**

By default, [Git Integration for Jira](https://marketplace.atlassian.com/4984) has the Repository Browser enabled. ([How to disable](https://bigbrassband.atlassian.net/wiki/content-only/viewpage.action?pageId=138706958&iframeId=fallback-mode&xdm_e=https://bigbrassband.atlassian.net/&xsm_c=fallback-mode-fake-key__15971815467303463&cp=/wiki&cv=0.0.0-fallback-mode&lic=none#RepositoryBrowser:Viewallrepositories-howToEnableDisable))

By default, [Dev Info for Jira](https://marketplace.atlassian.com/1219270) has the Repository Browser disabled. ([How to enable](https://bigbrassband.atlassian.net/wiki/content-only/viewpage.action?pageId=138706958&iframeId=fallback-mode&xdm_e=https://bigbrassband.atlassian.net/&xsm_c=fallback-mode-fake-key__15971815467303463&cp=/wiki&cv=0.0.0-fallback-mode&lic=none#RepositoryBrowser:Viewallrepositories-howToEnableDisable))

The **View developer tools** _permission_ is required to view the Git Roll Up Issue Tab. Jira users must also have the **Browse Project** _permissions_ to a project associated with a repository to view.


**What’s on this page:**

* * *

## Introduction

The Repository Browser is a feature that offers a view into your connected repositories into Jira Cloud. From the Repository browser page you can see summaries of the following:

*   Repository

*   Most recent issue associated by a commit

*   Last updated by commit author

*   Last commit date/time

*   [Personal Access Token management](#Personal-access-column)


## Repository browser

![](https://bigbrassband.atlassian.net/wiki/download/attachments/138706958/gitcloud-repo-browser-page-access.png?version=1&modificationDate=1638605147556&cacheVersion=1&api=v2)

To access the Repository browser:

1.  On your Jira Cloud dashboard, go to menu Apps ➜ **Git Integration: Repository browser**; or

2.  On your Jira Cloud dashboard, go to menu Apps ➜ Git Integration: Manage Git repositories ➜ **Repository browser** (sidebar).


While on the Repository browser page:

*   Use the search function to search for one or more repository containing the specified name

*   Click on a repository to view Commits and Compare tabs.

*   Click on **Go to User Settings: Git integration** to access the [User settings](/wiki/spaces/GITCLOUD/pages/781975665/User+Settings) page for setting up connected apps, default repositories, default branches and personal access tokens configuration.

*   Click on **Manage Git repositories** to go to the Git integration repositories configuration page.


## Personal access column

Jira administrators can configure git integrations (example: GitHub, GitLab) to require that Jira users create and provide their own [Personal Access Token](/wiki/spaces/GITCLOUD/pages/107216897/Creating+Personal+Access+Tokens) to enable features like creating branches, pull request or merge request via Jira Git integration development panel inside Jira.

The personal access column and configuration is relocated to [User settings](/wiki/spaces/GITCLOUD/pages/781975665/User+Settings).

## How can a Jira administrator enable or disable the Repository browser?

1.  Install the [Git Integration for Jira](https://marketplace.atlassian.com/4984) or the [Dev Info for Jira](https://marketplace.atlassian.com/1219270) app.

2.  Navigate to the [General settings](/wiki/spaces/GITCLOUD/pages/781942911/General+Settings) page of the application.

3.  Enable or disable the setting – **Show Repository browser: View all repositories, Commits and Compare pages**.

4.  Click **Update** button.


![](https://bigbrassband.atlassian.net/wiki/download/attachments/138706958/gitcloud-gencfg-repo-browser.png?version=1&modificationDate=1636096946037&cacheVersion=1&api=v2)

For detailed information about this feature, see [Documentation: Repository browser](/wiki/spaces/GITCLOUD/pages/1923025500/Repository+browser).

If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).