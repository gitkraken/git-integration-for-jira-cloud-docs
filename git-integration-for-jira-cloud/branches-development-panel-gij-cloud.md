---
 
title: Branches (Development panel)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The **Branches** section lists the branches names, linking the selected branch to view via the Repository browser.

The branch is displayed on the developer panel and is also associated to the mentioned Jira issue by fulfilling one of the following conditions:

*   The **branch name** contains the issue key. For example, `TEST-1-fix-binaries`.

*   The branch has associated unmerged commits with the issue key in the comments. For example, `TEST-1 fixed-binaries`.


The branch panel will show a summary of all the unmerged branches (regardless of the number of commits and the number of repositories) -- that either contain the name of the issue or have unmerged commits that reference the issue. This also gives users a view into the behind/ ahead status and provide links to the Repository browser for those branch names.

For example, `TST-1-new-branch` branch will be visible on the developer panel of the **TST-1** issue page even if the `TST-1-new-branch` branch has just been forked from master and does not have any new commit.

## Create branch

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025879/gitcloud-devpanel-create-branch-sel.png?version=1&modificationDate=1637285634240&cacheVersion=1&api=v2&width=340&height=461)

Click **Create branch** on the Jira Git integration development panel to create a branch for the selected repository. The following dialog is displayed:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025879/gitcloud-create-branch-dlg.png?version=1&modificationDate=1635754515240&cacheVersion=1&api=v2&width=680&height=331)

1.  Select a **Repository**. _(Optional - click Make default to set this repository as default for branch and PR/MR creation dialogs)._
    GITHUB If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `bbb-devs/test-repo`.
    GITLAB If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab owner name. For example, `johnsmith/webhook-test-repo`.

2.  Set **Source branch**. _(Optional - click Make default to set this branch as default for Source branch when working with branch and PR/MR creation dialogs)._

3.  The Git Integration for Jira app will populate the **Branch name** field according to the _Branch Name Template_ declared in the [**Git Integration Options**](https://bigbrassband.atlassian.net/wiki/spaces/~493751811/pages/1923025087/%28gitcloud%29+General+settings#Git-Integration-Options---introduced-version-2.13.1) [](https://bigbrassband.com/git-integration-for-jira/documentation/general-settings.html#git_int_options)via **General Settings**. Enter a descriptive name or leave it as is (recommended).


OPTIONAL
Jira users can provide their own PATS even if they are not required/mandated by the Jira admin.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025879/gitcloud-setup-pat-dlg.png?version=1&modificationDate=1635934059039&cacheVersion=1&api=v2&width=442&height=292)

*   Click on the **Provide a personal access token** label. The above dialog appears.

*   Paste a valid PAT of the current user to proceed. Invalid PATs will fail the branch creation process.

*   Click on **New token** to generate a new PAT via your remote git host service.

*   Click **Update** to use this PAT and save it to the current user profile. Otherwise, click **Cancel** to discard setting up PAT.

*   Click **Create branch**. The newly-created branch is now listed in the developer panel under **Branches**.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025879/gitcloud-devpanel-branches-list.png?version=2&modificationDate=1635943185503&cacheVersion=1&api=v2&width=340&height=156)

Clicking the icons adjacent to the right of the branch name will open this branch in your remote git host portal or open this branch in GitKraken git client app. 

This feature is available on connected GitLab, GitHub, Microsoft TFS/VSTS and AWS CodeCommit git hosts for Jira Cloud.

## Commits ahead and behind

The numbers **ahead** and **behind** represent the number of commits that are ahead/behind the main branch:

*   **Ahead**  –  number of commits in the branch which are not merged to the main branch.

*   **Behind**  –  number of commits in the main branch which are not merged to the branch.


The **Branches** section is only visible if commits from this branch are not merged to the _**main branch**_.  It's also not displayed if the repository is not associated with a project.

If the user does not have the **View Development Tools** _project permission_ for the project, the developer panel will be unavailable for that user.

For detailed information about creating branches, see article _**Creating branches**_.

[« Development panel locations](/wiki/spaces/GITCLOUD/pages/1923025834/Development+panel+locations)

[Pull/merge requests (Development panel) »](/wiki/spaces/GITCLOUD/pages/1923025925)

