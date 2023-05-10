---

title: Repository browser
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

The **Repository Browser** allows users to view git repositories of configured projects via the **Git** menu on the Jira dashboard.

## Getting started

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira Cloud</b><br>
        Git Integration for Jira Cloud only has <b>Repository Browser: Compare</b> feature. See <a href='/git-integration-for-jira-cloud/comparing-branches-or-tags-in-repository-browser-gij-cloud'>Compare view</a>.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        Users must have the <b>View Development Tools</b> <i>project permission</i> in order to gain access to the <b>Repository Browser</b>. For more information on assigning Jira permissions, see <a href='https://confluence.atlassian.com/display/Jira/Managing+Global+Permissions'><b>Managing Permissions in Jira</b></a>.
    </div>
    </div>
</div>

&nbsp;

## Apps git integration menu

After installing the Git Integration for Jira Cloud app, the **Apps** dropdown dashboard menu will have two new commands for Git integration, namely:

*   Git Integration: Manage integrations

*   Git Integration: Repository browser


The menu commands are hidden for all users if there are no repositories with Repository browser enabled for that user. The Git Integration for Jira Cloud app will always show these menu commands to Jira administrators.

The menu commands are visible to other users who have repositories with Repository browser enabled and have no history of using the Repository browser _(for example - no previously viewed or repositories set as favorite)._

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-access-new.png)

Available git repositories of configured projects are displayed.

&nbsp;

## Repositories list

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-list.png)

*   On the list table, you will see git repositories, recent issues updated by users, and the last commits made.

*   Clicking **Manage integrations** at the top right of the screen will open the git integration configuration page.

*   Use the search bar to look for repositories that contains the specified name.

*   Click on a git repository name to browse its contents. See [Repository view](#Repository-view) below.

*   Click on the GitKraken icon under the Actions column to view the selected repository in GitKraken git client app.

*   Use the page navigation at the bottom right of the list to display the next list.

&nbsp;

## Repository view

Click on a git repository to browse commits made on this repository.

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-repoview-list.png)

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Repository browser in Git Integration for Jira Cloud only supports displaying of commits from a repository and comparing of branches.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If the selected path is a <i><b>root</b></i> of the repository and no files are present, a message will be displayed instead of an empty file list.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Administration</b><br>
        Administrators can turn on/off the repository browser feature via General settings ➜ <i>Jira Issue View Options</i> ➜ <b>Show Repository browser: View all repositories, Commits and Compare pages</b>.
    </div>
    </div>
</div>

&nbsp;
* * *

[**Prev:** Smart commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud)

[**Next:** Viewing list of commits in Repository browser](/git-integration-for-jira-cloud/viewing-list-of-commits-in-repository-browser-gij-cloud)

