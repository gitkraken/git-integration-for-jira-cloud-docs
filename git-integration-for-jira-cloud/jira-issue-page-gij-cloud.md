---

title: Jira issue page
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

If the Git Integration for Jira app is configured and licensed successfully, new tabs and panels are added to each Jira issue.

&nbsp;

**On this page:**
- [Overview](#overview)
- [Git Roll Up tab](#git-roll-up-tab)
- [Git Commits tab](#git-commits-tab)
- [Jira Git integration development panel](#jira-git-integration-development-panel)
- [Development panel locations](#development-panel-locations)
- [Branches](#branches)
- [Pull or merge requests](#pull-or-merge-requests)
- [Git tags](#git-tags)
- [Jira Development Information](#jira-development-information)
- [Development Information Views](#development-information-views)

&nbsp;

* * *

&nbsp;

## Overview

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Some features can be switched on and off via <a href='/git-integration-for-jira-cloud/general-settings-for-administrators-gij-cloud'>General settings</a>:<br>
        <ul style='margin-bottom:0px;'>
            <li>Jira dashboard menu Apps ➜ Git Integration: Repository browser/Git Integration: Manage Git repositories ➜ <b>General settings</b> (sidebar).</li>
        </ul>
    </div>
    </div>
</div>

Users can see available features in the Jira issue page:

*   Git Commits tab
*   Git Roll Up tab
*   Git Development panel
*   Git Integration panel

![](/wp-content/uploads/gij-gitcloud-jira-issue-page-view-sel.png)

<img src='/wp-content/uploads/gij-gitcloud-jira-issue-git-idev-panel-view-new.png' style='margin:25px auto;max-width:100%;display:block;' />

| # | Feature | Description |
|:---:|:---|:---|
| **1** | **Git Commits** | In this tab, service users can see commit information such as commit author, changes to source files, as well as viewing the full commit that are associated to the current issue. |
| **2** | **Git Roll Up** | In this tab, service users can see commit statistics, diff and referenced Jira issues. |
| **3** | **Jira Development panel** | The Jira Development Panel is located on the right panel of the Jira issue page. This is a shortcut to viewing list of branches, commits and pull/merge requests. |
| **4** | **Git Integration panel** | Click to open the Git integration panel and allows service users to create branches and pull/merge requests for selected repositories inside Jira. |
| **5** | **Commit counter** | Contains git commits counter and shortcuts to Git Commits and Git Roll Up tabs. |
| **6** | **Branches** | Allows service users to create git branches against the specified repository from inside Jira. Created branches are displayed as a list. |
| **7** | **Ahead and Behind** | Represents the number of commits that are ahead/behind the main branch. |
| **8** | **Deep links** | Deep link shortcuts to view the selected branch in your git host service or in GitKraken git client app. |
| **9** | **Pull/Merge Requests** | Allows service users to create pull/merge request against the specified repository from inside Jira. Created pull/merge requests are displayed as a list. |
| **10** | **Git tags** | Lists available git tags from the connected git repositories. Use the git shortcut icons to open git tags in your git host service, GitKraken git client app or GitLens VSCode extension. |

&nbsp;

* * *

&nbsp;

## Git Roll Up tab

The **Git Roll Up** tab shows statistical information of the first and last revision of the commits and the time since the last commit was made. A summary of the files, lines and the developers who made the changes in this range of commits are also displayed.

Open a Jira issue then go to the Git Roll Up tab to view commit statistics, diffs and related git information.

<img src='/wp-content/uploads/gij-gitcloud-jira-issue-rollup-tab.png' style='margin:25px auto;max-width:100%;display:block;' />

### Category sorting

Sort the code statistics by clicking the respective **Sort** button then selecting the required sorting option.

<img src='/wp-content/uploads/gij-gitcloud-git-rollup-sort01.png' style='margin:25px auto;max-width:100%;display:block;' />

<img src='/wp-content/uploads/gij-gitcloud-git-rollup-sort02.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

Select roll up options by clicking the respective **Rollup** button.

<img src='/wp-content/uploads/gij-gitcloud-git-rollup-sort03.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

* * *

&nbsp;

## Git Commits tab

The Git Commits tab shows commit information such as commit authors, date of commit, commit messages, access to view code diffs, commit id and view full commit.

![](/wp-content/uploads/gij-gitcloud-jira-issue-git-commits-tab-chart.png)

Open an issue then go to the _**Git Commits**_ tab to view commit information:

| Pointer | Information | Description |
| :---: | :--- | :--- |
| **1** | **Repository/Indexed** | Name of the repository _(as in app config)_ and date of last synchronization with remote repository. |
| **2** | **Author/Committer** | User who performed the commit. Hover the mouse pointer on the name to view user card. |
| **3** | **Issue key/Commit message** | This is the Jira issue with the corresponding commit message. |
| **4** | **Repository name/Branch** | This is the name of the repository and the branch where the commit has been made. |
| **5** | **Commit UID** | UID of the commit and git host link. Click the UID to view the code diffs for this commit. Click the git host link to view this commit via the git host server. |
| **6** | **Commit counter indicators** | ![Git commit traffic light example](/wp-content/uploads/gij-traffic-light-example.png) The traffic light indicator shows the added/modified/deleted lines from the file code diffs. |
| **7** | **Commit ID** | Click the commit ID to view the commit code diff. Click the copy icon to copy the commit code diff to the system clipboard. |
| **8** | **Open in GitKraken** | Opens this commit in the GitKraken git client app. |
| **9** | **Open in GitLens** | Opens this commit in the GitLens extension via VSCode app. |
| **10** | **Files changed** | List of files affected by the commit. Click the file or git host link to view code diff of this commit. |
| **11** | **Web links** | Clickable web links that will open the selected file code diff directly to git host service portal in a new browser window/tab. |

View the whole commit code diff information by clicking the **View full commit** button to the right of the commit message.

View code diff information of the particular file by clicking the filename for each file adjacent to the rollup counter markers.

&nbsp;

* * *

&nbsp;

## Jira Git integration development panel

### Permissions

**Jira Cloud - Development panel**
The **View Development Tools** _permission_ only applies to Jira Classic Projects. Next-Gen Projects don't allow to modify the permission.

**Create Branches and Branch Names**
For connected GitHub git host, this feature requires enabled `public_repo` scope permissions.

**Commits Ahead and Behind**
If the user does not have the **View Development Tools** _project permission_ for the project, the developer panel will be unavailable for that user.

### Git Integration panel

Locate the Jira Git integration development panel on the right pane of the Jira issue page. Click on **Git integration** to expand its contents. GIJ does not auto-populate git data in the Git integration panel upon loading the issue page to improve Jira performance.

<img src='/wp-content/uploads/gij-cloud-jira-git-integration-panel-refresh.png' style='margin:25px auto;max-width:100%;display:block;' />

The **Refresh** action is available for manually reloading the git information on the Git Integration development panel. Use it to repopulate Git data without reloading the Jira issue page.

Git links are now available on the developer panel in the following locations:

*   Issue page
*   Search page in detailed view
*   Jira Agile screen

<img src='/wp-content/uploads/gij-gitcloud-git-integration-panel.png' style='margin:25px auto;max-width:100%;display:block;' />

The commits counter refers to the existing Git Commits view which the issue tab displays.

&nbsp;

## Development panel locations

The development panel can be accessed on the following locations.

### Issue and Search pages

In **Issue** and **Search** pages, the developer panel is visible on the right pane.

![](/wp-content/uploads/gij-gitcloud-devpanel-location-issue-page.png)

### Kanban board screen

On the Kanban board, click on an issue on the board grid. On a dialog that displays the selected Jira issue, click **Open Git integration** on the right sidebar. The Git integration panel is displayed.

![](/wp-content/uploads/gij-gitcloud-devpanel-location-kanban.png)

&nbsp;

* * *

&nbsp;

## Branches

The **Branches** section lists the branches names, linking the selected branch to view via the Repository browser.

The branch is displayed on the developer panel and is also associated to the mentioned Jira issue by fulfilling one of the following conditions:

*   The **branch name** contains the issue key. For example, `TEST-1-fix-binaries`.
*   The branch has associated unmerged commits with the issue key in the comments. For example, `TEST-1 fixed-binaries`.

The branch panel will show a summary of all the unmerged branches (regardless of the number of commits and the number of repositories) -- that either contain the name of the issue or have unmerged commits that reference the issue. This also gives users a view into the behind/ahead status and provide links to the Repository browser for those branch names.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For example, <code>TST-1-new-branch</code> branch will be visible on the developer panel of the <b>TST-1</b> issue page even if the <code>TST-1-new-branch</code> branch has just been forked from master and does not have any new commit.
    </div>
    </div>
</div>

### Create branch

<img src='/wp-content/uploads/gij-gitcloud-devpanel-create-branch-sel.png' style='margin:25px auto;max-width:100%;display:block;' />

Click **Create branch** on the Jira Git integration development panel to create a branch for the selected repository.

![](/wp-content/uploads/gij-gitcloud-issue-dev-panel-create-branch-dlg)

1.  Select a **Repository**. _(Optional - click Make default to set this repository as default for branch and PR/MR creation dialogs)._

2.  Set **Source branch**. _(Optional - click Make default to set this branch as default for Source branch when working with branch and PR/MR creation dialogs)._

3.  The Git Integration for Jira app will populate the **Branch name** field according to the _Branch Name Template_ declared in the [**Git Integration Options**](/git-integration-for-jira-cloud/general-settings-for-administrators-gij-cloud) via **General Settings**. Enter a descriptive name or leave it as is (recommended).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        After creating a branch, it is added to the Git Integration developer panel under the Branches list. The branch name does not have a commit if it is displayed in italics.<br>
        <img src='/wp-content/uploads/gij-gitcloud-devpanel-create-branch-no-commit.png' style='margin:20px auto 10px auto;max-width:100%;display:block;' />
    </div>
    </div>
</div>

<img src='/wp-content/uploads/gij-gitcloud-devpanel-branches-list.png' style='margin:25px auto;max-width:100%;display:block;' />

Clicking the icons adjacent to the right of the branch name will open this branch in your remote git host portal or open this branch in GitKraken git client app.

### Commits ahead and behind

The numbers **ahead** and **behind** represent the number of commits that are ahead/behind the main branch:

*   **Ahead** – number of commits in the branch which are not merged to the main branch.
*   **Behind** – number of commits in the main branch which are not merged to the branch.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">        
        The <b>Branches</b> list is only visible if commits from this branch are not merged to the <i><b>main branch</b></i>. It's also not displayed if the repository is not associated with a project.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Pull or merge requests

The **Pull Requests** (GitHub or other connected git hosts) or **Merge Requests** (if GitLab is connected) section lists the merge/pull requests and their status. All merge/pull requests from all types of sources are shown here (for now, GitLab/GitHub/Azure/TFS/VSTS).

The displayed information depends on which supported git hosts are connected to Jira. For example:

*   GitLab integrations only – merge requests
*   Other integrations – pull requests
*   Both GitLab and GitHub integrations – separate sections for merge requests and pull requests

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Prerequisite</b><br>
        The source branch for the pull/merge request must have a commit. Fulfill this condition to create pull/merge request via Jira Git Integration panel without issues.
    </div>
    </div>
</div>

### Create pull/merge request

<img src='/wp-content/uploads/gij-gitcloud-devpanel-create-pullreq-sel.png' style='margin:25px auto;max-width:100%;display:block;' />

If a git host is connected to Jira, create a pull/merge request by clicking **Create pull request** or **Create merge request** label link on the Jira Git integration development panel.

![](/wp-content/uploads/gij-gitcloud-create-pull-req-dlg)

*   Select **Repository** from the list.
*   Choose a branch as the **Source branch**. This branch will be merged to the target branch.
*   Set _**master**_ as the **Target branch**.
*   Enter a descriptive **Title** or leave it as is (recommended).

Click **Create pull request** on the Create pull request dialog. The newly-created pull request is now listed in the developer panel under **Pull requests**.

### Associating pull/merge request to Jira issue

A git service user can create a PR/MR via the Git host service portal and adding/inserting a Jira issue key in the PR/MR title. This is automatically added to the Pull/Merge request list in the Jira issue Git developer panel.

The merge request is displayed on the developer panel and will also be associated to the mentioned Jira issue by fulfilling the following condition:

*   Merge request **Title** contains the issue key. For example, `TEST-1-Fix-binaries`.

This will also allow a service user to associate a Merge/Pull Request with multiple Jira issues regardless of commit associations.

<img src='/wp-content/uploads/gij-gitcloud-devpanel-merge-req.png' style='margin:25px auto;max-width:100%;display:block;' />

Hover the mouse pointer on the pull/merge request label to see information of the repository and branch where it belongs.

<img src='/wp-content/uploads/gij-gitcloud-devpanel-merge-req-hover.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

* * *

&nbsp;

## Git tags

The Git Integration for Jira app supports both lightweight and annotated tags. The tags are loaded separately from the rest of the Git Source Code.

Git tags identify specific release versions of your code in a particular branch and do not change when the branch moves on. A tag is an alias for a commit hash, much like symbolic names for a given revision. It is typically used to mark a particular point in the commit. It is like a branch with a read-only attribute. The git tags are accessible in the developer panel.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Having more than one tag with the same name across different branches can become difficult to maintain.
    </div>
    </div>
</div>

Tags cannot be moved since it is linked to a specific commit and are not pushed by default.

The Git for Jira app supports two types of git tags:

*   **lightweight** – shows only the commit object
*   **annotated** – shows the message, author and the tag object followed by the commit

<img src='/wp-content/uploads/gij-gitcloud-devpanel-git-tags.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

The Git Integration for Jira app will show the last 3 and first tags if no filter is set. If the filter is set, the Git Integration for Jira app will use it and will display the tags sorted in ascending order by date.

If there are several git tags listed, click the **more...** label link to expand the list in increments of five tags.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Click the adjacent icons to the right of the tags to open this tag in your git host service portal or in GitKraken git client app.
    </div>
    </div>
</div>

### Tag information

<img src='/wp-content/uploads/gij-gitcloud-devpanel-git-tags-hover.png' style='max-width:100%;margin:25px auto;display:block;' />

Move the mouse pointer over the tag to display the following tooltip information:

*   Repository Name
*   Commit author name and email address (if available)
*   Date / Time
*   Message (if any)

### Tag associations

Tags are only associated with the Jira issue by Jira keys that are specified in commits that belong to the tag. Specifying a Jira key in the name of a tag does not associate this tag with the mentioned ticket.

&nbsp;

* * *

&nbsp;

## Jira Development Information

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <b>View Development Tools</b> <i>permission</i> only applies to Jira <b><i>Company-managed</i></b> projects. <b><i>Team-managed</i></b> projects don't allow to modify the permission.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Only newly added commits, branches and pull requests will be uploaded to Jira Cloud when enabling the <a href='/git-integration-for-jira-cloud/send-development-information-to-jira-cloud-setting-gij-cloud'>Send Development Information to Jira Cloud</a> setting. If you wish to upload the entire history of an integration or repository - remove the integration/repository and then add the integration/repository back.
    </div>
    </div>
</div>

### What is Jira Development Information?

Jira Development Information is a suite of features available in Jira Software on the Cloud platform that puts commits, branches, and pull requests in context of Jira issue.

*   By default, [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) has Jira Development Information disabled.
*   By default, [**Dev Info for Jira**](https://marketplace.atlassian.com/1219270) has Jira Development Information enabled.

### How does Jira Development Information work?

The [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) and [**Dev Info for Jira**](https://marketplace.atlassian.com/1219270) apps can be configured to "push" development information (commits, branches, and pull requests) directly into your Jira Cloud instance. Once the data is stored by Jira Cloud - the commits, branches, and pull requests can be displayed by Atlassian in a variety of locations within Jira Cloud.

### Who can see Jira Development Information?

*   Jira users with the View development tools Jira permission for a given Jira project can.
*   Jira administrators can verify a user's permissions using the [**Permission Helper**](https://confluence.atlassian.com/adminjiracloud/jira-admin-helper-818578850.html).

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <b>View developer tools</b> <i>permission</i> is required to view the Jira Development Information. Jira users must also have the <b>Browse Project</b> <i>permissions</i> to a project associated with a repository to view.
    </div>
    </div>
</div>

### How to enable or disable Jira Development Information

1.  Install the [Git Integration for Jira](https://marketplace.atlassian.com/4984) or the [Dev Info for Jira](https://marketplace.atlassian.com/1219270) app.

2.  Navigate to the General settings page of the application (![](/wp-content/uploads/actions-icon.png) Jira Settings ➜ Apps ➜ (sidebar) **General settings**).

3.  Enable or disable the setting: `Send Development Information to Jira Cloud`.

4.  Click **Update** button.

<img src='/wp-content/uploads/gij-gitcloud-gencfg-send-devinfo-to-jira-cloud.png' style='display:block;margin:25px auto 35px auto;max-width:100%' />

&nbsp;

* * *

&nbsp;

## Development Information Views

Atlassian Jira Cloud currently displays Jira Development Information in the Development Panel in Jira issues.

![](/wp-content/uploads/gij-gitcloud-jira-dev-info-views-location.png)

### Detailed view of commits

![](/wp-content/uploads/gij-gitcloud-jira-dev-info-views-commits.png)

### Detailed view of branches

![](/wp-content/uploads/gij-gitcloud-jira-dev-info-views-branches.png)

### Detailed view of pull requests

![](/wp-content/uploads/gij-gitcloud-jira-dev-info-views-pull-req.png)

### Development status in Jira issue searching

In the Jira search interface you will have a new column to add: **Development**.

This column is displayed in the following order of precedence:

1.  **Blank** (no commits or pull requests are declined/closed)
2.  **\# of Commits** (when no pull requests are associated)
3.  **Merged** (all associated pull requests are merged or closed)
4.  **Under Review** (at least one associated pull request is open)

![](/wp-content/uploads/gij-gitcloud-dev-info-dev-status-in-jira-issue-search.png)

### Release Hub - Warnings

The Release Hub can be accessed within a Jira project at the **Releases** page. Jira issues with a fix version assigned will appear in the Release Hub.

Currently two types of warnings are available:

*   **Open pull requests:** These issues have been marked complete but have open pull requests.
*   **Unreviewed Code:** These issues have been marked complete but the commits are not part of a pull request or review.

![](/wp-content/uploads/gij-gitcloud-dev-info-release-hub-warnings.png)

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <a href='https://confluence.atlassian.com/jirasoftwarecloud/using-the-release-page-to-check-the-progress-of-a-version-764478141.html'><b>More information from Atlassian</b></a>
    </div>
    </div>
</div>

### Next-gen projects: View commits, branches, and pull requests in Jira Boards

![Next-gen projects agile board view](/wp-content/uploads/gij-gitcloud-dev-info-next-gen-view-commits-etc.png)

When using the Development Information feature within a 'Next-gen' (Team-managed) Jira Cloud project - your commits, branches and pull requests will be shown in your boards.

A 'next-gen' project can be created in the Projects screen:

1.  On your Jira Cloud dashboard menu, choose Projects ➜ **View all projects**.
2.  In the top-right corner of the page, click **Create project**.
3.  On the next screen, select either **Scrum** or **Kanban**.
4.  Click **Use template** to proceed to the following screen.
5.  Choose the type of project required for your team or company.
6.  Give the new project a meaningful **Name**; set project **Key** as required.
7.  Finally, click **Create project** to complete this process.

&nbsp;

* * *

&nbsp;

[**Prev:** Jira user information card](/git-integration-for-jira-cloud/jira-user-information-card-gij-cloud)

[**Next:** Jira project page](/git-integration-for-jira-cloud/jira-project-page-gij-cloud/)

