---

title: Default repository feature
description: Learn how to set default repositories for Jira projects when using the Create Branch and Create Pull Request features.
taxonomy:
    category: git-integration-for-jira-cloud

---

Set the default repository for a Jira project when using the [Create Branch](/git-integration-for-jira-cloud/create-branch-gij-cloud) and [Create pull/merge request](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud) features.

![](/wp-content/uploads/gij-gitcloud-user-settings-default-repo-feature.png)

&nbsp;

## Search function

<img src='/wp-content/uploads/gij-gitcloud-user-settings-def-repo-search.png' style='margin:25px auto;max-width:100%;display:block;' />

If your Jira instance has multiple projects, use the search bar to find projects and assign a default repository to each.

&nbsp;

## Default repository setting

<img src='/wp-content/uploads/gij-gitcloud-user-settings-def-repo-list.png' style='margin:25px auto;max-width:100%;display:block;' />

In the **Repository** column, set default repositories using the dropdown list. Use the search function within the list to find specific repositories by name. Select the desired repository to set it as the default for the selected project.

&nbsp;

## Effect on branch and pull request dialogs

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This configuration affects <a href='/git-integration-for-jira-cloud/create-branch-gij-cloud'>Create Branch</a> and <a href='/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud'>Create Pull or Merge Requests</a>.
    </div>
    </div>
</div>

If no default repository is set, the **Create Branch** and **Create Pull/Merge Request** dialogs let users select a repository and _**make it the default**_ by clicking the corresponding button.

![](/gitcloud-jira-issue-create-branch-make-default.png)

<div align=center style='margin:15px 0 35px 0'><b>Figure 1.</b> <i>The same layout also applies to Create Pull/Merge Request dialogs.</i></div>

This sets the repository as the default selection for branch and pull request dialogs in the current project.

![](/wp-content/uploads/gij-gitcloud-jira-issue-create-branch-set-default.png)

<div align=center style='margin:15px 0 35px 0'><b>Figure 2.</b> <i>The same layout also applies to Create Pull/Merge Request dialogs.</i></div>

In the above example, the selected default repository displays a DEFAULT label. Users can clear this setting using the adjacent button. To set a new default repository for this project, select a repository from the dropdown list, then click **Make default** (see Figure 1).

&nbsp;
* * *

[**Prev:** Default branch feature](/git-integration-for-jira-cloud/default-branch-feature-gij-cloud)

[**Next:** Personal access token feature](/git-integration-for-jira-cloud/personal-access-token-feature-gij-cloud)

<kbd>Last updated: December 2025</kbd>
