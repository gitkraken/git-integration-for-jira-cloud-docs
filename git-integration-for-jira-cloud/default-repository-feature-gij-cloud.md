---

title: Default repository feature
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This feature allows users to set the default repository for a Jira project when using the [Create Branch](/git-integration-for-jira-cloud/create-branch-gij-cloud) and [Create pull/merge request](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud) features.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1741094916/gitcloud-user-settings-default-repo-feature.png?version=1&modificationDate=1623726181829&cacheVersion=1&api=v2&width=680&height=332)

## Search function

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1741094916/gitcloud-user-settings-def-repo-search.png?version=1&modificationDate=1623726181845&cacheVersion=1&api=v2&width=340&height=48)

If your Jira instance have multiple projects, use the search bar to look for a project or several projects (using the search criteria) to work on and assign a default repository for each project.

## Default repository setting

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1741094916/gitcloud-user-settings-def-repo-list.png?version=1&modificationDate=1623726181867&cacheVersion=1&api=v2&width=442&height=279)

On the **Repository** column, default repositories can be set using the dropdown list. Utilize the search function on the list to return specific repositories according to the search name. Select the desired repository to set it as default repository for the selected project.

## Effect on branch and pull request dialogs

This configuration affects the [Create Branch](/git-integration-for-jira-cloud/create-branch-gij-cloud), [Create Pull or Merge Requests](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud).

If no default repository is set, the **Create Branch** and **Create Pull/Merge Request** dialogs will allow users to select a repository and _**make it as default**_ by clicking the corresponding button.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1741094916/gitcloud-jira-issue-create-branch-make-default.png?version=1&modificationDate=1623726181869&cacheVersion=1&api=v2&width=680&height=361)

**Figure 1.** _The same layout also applies to Create Pull/Merge Request dialogs._


This will set the repository as the default selection of the branch and pull request dialogs for the current project from now on.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1741094916/gitcloud-jira-issue-create-branch-set-default.png?version=1&modificationDate=1623726181872&cacheVersion=1&api=v2&width=680&height=361)

**Figure 2.** _The same layout also applies to Create Pull/Merge Request dialogs._


Referring to the above example image, the selected default repository has a label DEFAULT. Users can clear this setting using the adjacent button. Reselect a repository from the dropdown list to set a new default repository for this project, then click **Make default** (see Figure 1).

