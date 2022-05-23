---

title: Repository browser
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The **Repository Browser** allows users to view git repositories of configured projects via the **Git** menu on the Jira dashboard.

## Getting started

**Jira Cloud**
Git Integration for Jira Cloud only has **Repository Browser:** **Compare** feature. See [Compare view](/wiki/spaces/GITCLOUD/pages/1923025590/Comparing+branches+or+tags+in+Repository+browser).

**Permissions**
Users must have the **View Development Tools** _project permission_ in order to gain access to the **Repository Browser**. For more information on assigning Jira permissions, see [**Managing Permissions in Jira**](https://confluence.atlassian.com/display/Jira/Managing+Global+Permissions).

## Apps git integration menu

After installing the Git Integration for Jira Cloud app, the **Apps** dropdown dashboard menu will have two new commands for Git integration, namely:

*   Git Integration: Manage integrations

*   Git Integration: Repository browser


The menu commands are hidden for all users if there are no repositories with Repository browser enabled for that user. The Git Integration for Jira Cloud app will always show these menu commands to Jira administrators.

The menu commands are visible to other users who have repositories with Repository browser enabled and have no history of using the Repository browser _(for example - no previously viewed or repositories set as favorite)._

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025500/gitcloud-repo-browser-page-access.png?version=2&modificationDate=1650260719272&cacheVersion=1&api=v2)

Available git repositories of configured projects are displayed.

## Repositories list

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025500/gitcloud-repo-browser-page-list.png?version=1&modificationDate=1650260840880&cacheVersion=1&api=v2)

*   On the list table, you will see git repositories, recent issues updated by users, and the last commits made.

*   Clicking **Manage integrations** at the top right of the screen will open the git integration configuration page.

*   Use the search bar to look for repositories that contains the specified name.

*   Click on a git repository name to browse its contents. See [Repository view](#Repository-view) below.

*   Click on the GitKraken icon under the Actions column to view the selected repository in GitKraken git client app.

*   Use the page navigation at the bottom right of the list to display the next list.


## Repository view

Click on a git repository to browse commits made on this repository.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025500/gitcloud-repo-browser-page-repoview-list.png?version=2&modificationDate=1650263383860&cacheVersion=1&api=v2)

The Repository browser in Git Integration for Jira Cloud only supports displaying of commits from a repository and comparing of branches.

If the selected path is a _**root**_ of the repository and no files are present, a message will be displayed instead of an empty file list.

**Administration**
Administrators can turn on/off the repository browser feature via General settings ➜ _Jira Issue View Options_ ➜ **Show Repository browser: View all repositories, Commits and Compare pages**.

[« Smart commits](/git-integration-for-jira-cloud/Smart-commits)

[Viewing list of commits in Repository browser »](/wiki/spaces/GITCLOUD/pages/1923025571/Viewing+list+of+commits+in+Repository+browser)

