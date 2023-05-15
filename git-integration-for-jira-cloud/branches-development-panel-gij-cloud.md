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

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For example, <code>TST-1-new-branch</code> branch will be visible on the developer panel of the **TST-1** issue page even if the <code>TST-1-new-branch</code> branch has just been forked from master and does not have any new commit.
    </div>
    </div>
</div>

&nbsp;

## Create branch

<img src='/wp-content/uploads/gij-gitcloud-devpanel-create-branch-sel.png' style='margin:25px auto;max-width:100%;display:block;' />

Click **Create branch** on the Jira Git integration development panel to create a branch for the selected repository. The following dialog is displayed:

![](/wp-content/uploads/gij-gitcloud-issue-dev-panel-create-branch-dlg)

1.  Select a **Repository**. _(Optional - click Make default to set this repository as default for branch and PR/MR creation dialogs)._
    GITHUB If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `bbb-devs/test-repo`.
    GITLAB If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab owner name. For example, `johnsmith/webhook-test-repo`.

2.  Set **Source branch**. _(Optional - click Make default to set this branch as default for Source branch when working with branch and PR/MR creation dialogs)._

3.  The Git Integration for Jira app will populate the **Branch name** field according to the _Branch Name Template_ declared in the [**Git Integration Options**](/git-integration-for-jira-cloud/general-settings-for-administrators-gij-cloud) via **General Settings**. Enter a descriptive name or leave it as is (recommended).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>OPTIONAL</b><br>
        Jira users can provide their own PATS even if they are not required/mandated by the Jira admin.
    </div>
    </div>
</div>


<img src='/wp-content/uploads/gij-gitcloud-setup-pat-dlg.png' style='margin:25px auto;max-width:100%;display:block;' />

*   Click on the **Provide a personal access token** label. The above dialog appears.

*   Paste a valid PAT of the current user to proceed. Invalid PATs will fail the branch creation process.

*   Click on **New token** to generate a new PAT via your remote git host service.

*   Click **Update** to use this PAT and save it to the current user profile. Otherwise, click **Cancel** to discard setting up PAT.

*   Click **Create branch**. The newly-created branch is now listed in the developer panel under **Branches**.


<img src='/wp-content/uploads/gij-gitcloud-devpanel-branches-list.png' style='margin:25px auto;max-width:100%;display:block;' />

Clicking the icons adjacent to the right of the branch name will open this branch in your remote git host portal or open this branch in GitKraken git client app. 

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This feature is available on connected GitLab, GitHub, Microsoft TFS/VSTS and AWS CodeCommit git hosts for Jira Cloud.
    </div>
    </div>
</div>

&nbsp;

## Commits ahead and behind

The numbers **ahead** and **behind** represent the number of commits that are ahead/behind the main branch:

*   **Ahead**  –  number of commits in the branch which are not merged to the main branch.

*   **Behind**  –  number of commits in the main branch which are not merged to the branch.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">        
        The <b>*Branches</b> section is only visible if commits from this branch are not merged to the <i><b>main branch</b></i>. It's also not displayed if the repository is not associated with a project.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If the user does not have the <b>View Development Tools</b> <i>project permission</i> for the project, the developer panel will be unavailable for that user.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For detailed information about creating branches, see article <i><b>Creating branches</b></i>.
    </div>
    </div>
</div>

&nbsp;
* * *

[**Prev:** Development panel locations](/git-integration-for-jira-cloud/development-panel-locations-gij-cloud)

[**Next:** Pull or merge requests (Development panel)](/git-integration-for-jira-cloud/pull-or-merge-requests-development-panel-gij-cloud)


