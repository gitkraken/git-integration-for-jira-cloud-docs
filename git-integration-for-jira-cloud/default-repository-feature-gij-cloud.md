---

title: Default repository feature
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This feature allows users to set the default repository for a Jira project when using the [Create Branch](/git-integration-for-jira-cloud/create-branch-gij-cloud) and [Create pull/merge request](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud) features.

![](/wp-content/uploads/gij-gitcloud-user-settings-default-repo-feature.png)

&nbsp;

## Search function

<img src='/wp-content/uploads/gij-gitcloud-user-settings-def-repo-search.png' style='margin:25px auto;max-width:100%;display:block;' />

If your Jira instance have multiple projects, use the search bar to look for a project or several projects (using the search criteria) to work on and assign a default repository for each project.

&nbsp;

## Default repository setting

<img src='/wp-content/uploads/gij-gitcloud-user-settings-def-repo-list.png' style='margin:25px auto;max-width:100%;display:block;' />

On the **Repository** column, default repositories can be set using the dropdown list. Utilize the search function on the list to return specific repositories according to the search name. Select the desired repository to set it as default repository for the selected project.

&nbsp;

## Effect on branch and pull request dialogs

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This configuration affects the <a href='/git-integration-for-jira-cloud/create-branch-gij-cloud'>Create Branch</a>, <a href='/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud'Create Pull or Merge Requests</a>.
    </div>
    </div>
</div>

If no default repository is set, the **Create Branch** and **Create Pull/Merge Request** dialogs will allow users to select a repository and _**make it as default**_ by clicking the corresponding button.

![](/gitcloud-jira-issue-create-branch-make-default.png)

<div align=center style='margin:15px 0 35px 0'><b>Figure 1.</b> <i>The same layout also applies to Create Pull/Merge Request dialogs.</i></div>

This will set the repository as the default selection of the branch and pull request dialogs for the current project from now on.

![](/wp-content/uploads/gij-gitcloud-jira-issue-create-branch-set-default.png)

<div align=center style='margin:15px 0 35px 0'><b>Figure 2.</b> <i>The same layout also applies to Create Pull/Merge Request dialogs.</i></div>

Referring to the above example image, the selected default repository has a label DEFAULT. Users can clear this setting using the adjacent button. Reselect a repository from the dropdown list to set a new default repository for this project, then click **Make default** (see Figure 1).

&nbsp;
* * *

[**Prev:** Default branch feature](/git-integration-for-jira-cloud/default-branch-feature-gij-cloud)

[**Next:** Personal access token feature](/git-integration-for-jira-cloud/personal-access-token-feature-gij-cloud)

