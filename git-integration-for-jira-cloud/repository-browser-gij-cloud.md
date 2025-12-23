---

title: Repository browser
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

The **Repository Browser** allows users to view git repositories of configured projects via the **Git** menu on the Jira dashboard.

&nbsp;

**On this page:**
- [Getting started](#getting-started)
- [How to enable or disable the Repository browser](#how-to-enable-or-disable-the-repository-browser)
- [Apps git integration menu](#apps-git-integration-menu)
- [Repositories list](#repositories-list)
- [Repository view - Viewing list of commits](#repository-view---viewing-list-of-commits)
- [Comparing branches or tags](#comparing-branches-or-tags)
- [General settings](#general-settings)

&nbsp;

* * *

&nbsp;

## Getting started

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default Settings</b><br>
        <ul style='margin-bottom:0px'>
            <li>
                By default, <a href="https://marketplace.atlassian.com/4984" target="_blank">Git Integration for Jira</a> has the Repository Browser enabled.
            </li>
            <li>
                By default, <a href="https://marketplace.atlassian.com/1219270" target="_blank">Dev Info for Jira</a> has the Repository Browser disabled.
            </li>
        </ul>
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
        The <b>View developer tools</b> <i>permission</i> is required to view the Repository Browser. Jira users must also have the <b>Browse Project</b> <i>permissions</i> to a project associated with a repository to view. For more information on assigning Jira permissions, see <a href='https://confluence.atlassian.com/display/Jira/Managing+Global+Permissions'><b>Managing Permissions in Jira</b></a>.
    </div>
    </div>
</div>

The Repository Browser offers a view into your connected repositories in Jira Cloud. From the Repository browser page you can see summaries of:

*   Repository
*   Most recent issue associated by a commit
*   Last updated by commit author
*   Last commit date/time
*   Personal Access Token management

&nbsp;
## To access the Repository browser:

On any Jira Cloud page, go to Side Menu ➜ Apps ➜ **Git Integration for Jira** ➜ click the 'Repositories' button

![](/wp-content/uploads/GIJ-Cloud-Accessing-Repo-Browser-2025.png)

&nbsp;

* * *

&nbsp;

## Repositories list

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-list-2025.png)

*   On the list table, you will see git repositories, recent issues updated by users, and the last commits made.

*   Clicking **Manage integrations** at the top right of the screen will open the git integration configuration page.

*   Use the search bar to look for repositories that contains the specified name.

*   Click on a git repository name to browse its contents. See [Repository view](#repository-view---viewing-list-of-commits) below.

*   Click on the GitKraken icon under the Actions column to view the selected repository in GitKraken git client app.

*   Use the page navigation at the bottom right of the list to display the next list.

*   Click on **User Settings** to access the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page for setting up connected apps, default repositories, default branches and personal access tokens configuration.

&nbsp;

* * *

&nbsp;

## Repository view - Viewing list of commits

On the Repository browser page, click a repository to open it in **Commits** view and browse commits made for this repository.

The list of commits for the currently selected project is displayed in descending order:

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-repoview-list-new-2025.png)

1.  Click on the repository selector dropdown list to select the repository to view.

2.  Select the branch from the dropdown list to browse repository contents for that branch _(default view is the master branch)_.

3.  Select filter to show all commits, linked commits or unlinked commits that were not associated to a Jira issue.

4.  Displays the Jira issue key associated with this commit or pull/merge request (for example, `DMO-8`).

5.  Click on the **Change icon** ![](/wp-content/uploads/gij-edit-icon-dark.png) to edit/manage associated Jira issue keys to the selected commit.

6.  Click on the GitKraken icon at the far right of the row to view this commit in [GitKraken git client](https://www.gitkraken.com/git-client/features) app.

7.  Click on the GitLens icon at the far right of the row to view this commit in [GitLens for VSCode extension](https://www.gitkraken.com/gitlens).

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
        If the selected path is a <i><b>root</b></i> of the repository and no files are present, a message will be displayed instead of an empty file list.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Comparing branches or tags

On the Repository browser (_Jira dashboard ➜ Apps menu ➜ **Git Integration: Repository browser**_), click the **Compare** page tab.

On this page, two branches from the current repository can be compared.

A diff between the _**base**_ branch and the _**compare**_ branch is displayed:

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-compare-view-2025.png)

To view desired results, use the following selection scenarios:

*   select **master** as compare; select the most recent branch as base.

*   select **master** as compare; select a tag with a version release.

*   select different branches as base and compare. (Example: `TYT-212` against `TYT-316`)

![](/wp-content/uploads/gij-gitcloud-repo-browser-compare-view-swap-2025.png)

Click **…** to swap the base and the compare selection.

The **Summary** page displays the _**Commits**_, _**Aggregated Lines by Developers**_ and _**Files**_. Click on a file to view its code diff.

Click **Commits** on the sidebar to view the list of commits resulting from this compare. The adjacent figure indicates the number of commits associated to this compare.

Click **Diff** on the sidebar to view code diffs of the selected range of commits with the path and name of the affected files.

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-compare-isues-view-2025.pngg)

Click **Issues** on the sidebar to view list of unique Jira issues related to commits.

On the **Issues** page, clicking the **View in issue navigator** label will open the search page with passed query of a list of Jira issues found based from the compare criteria.

&nbsp;

* * *
&nbsp;

[**Prev:** Smart commits](/git-integration-for-jira-cloud/smart-commits-gij-cloud)

[**Next:** Viewing commit code diffs](/git-integration-for-jira-cloud/viewing-commit-code-diffs-gij-cloud)

