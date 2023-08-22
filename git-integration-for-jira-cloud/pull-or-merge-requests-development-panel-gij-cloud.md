---

title: Pull or merge requests (Development panel)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

The **Pull Requests** (GitHub or other connected git hosts) or **Merge Requests** (if GitLab is connected) section lists the merge/pull requests and their status. All merge/pull requests from all types of sources are shown here (for now, GitLab/GitHub/Azure/TFS/VSTS).

The displayed information depends on which supported git hosts are connected to Jira. For example:

*   GitLab integrations only  –  merge requests

*   Other integrations  –  pull requests

*   Both GitLab and GitHub integrations  –  separate sections for merge requests and pull requests

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For necessary permissions that GitLab users must have for creating pull/merge requests, see <a href='https://docs.gitlab.com/ee/user/permissions.html'><b>GitLab Documentation: Permissions</b></a>.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This function does not work for single git repository connections. Use the Full feature integration instead.
    </div>
    </div>
</div>

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

&nbsp;

### Getting started

<img src='/wp-content/uploads/gij-gitcloud-devpanel-create-pullreq-sel.png' style='margin:25px auto;max-width:100%;display:block;' />

If a git host is connected to Jira, create a pull/merge request by clicking **Create pull request** or **Create merge request** label link on the Jira Git integration development panel. The following dialog is displayed.

![](/wp-content/uploads/gij-gitcloud-create-pull-req-dlg)

*   Select **Repository** from the list.
    
    <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>GITHUB</b> If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name.<br>For example, `BigBrassBand/second-webhook-test-repo`.

    <b style='background-color:#FFEED1; padding:1px 5px; color:#CC5900; border-radius:3px; margin: 0 5px; font-size: small;'>GITLAB</b> If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab owner name.<br>For example, `johnsmith/second-webhook-test-repo`.

*   Choose a branch as the **Source branch**. This branch will be merged to the target branch.

*   Set _**master**_ as the **Target branch**.

*   Enter a descriptive **Title** or leave it as is (recommended).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>OPTIONAL</b><br>
        Jira users can provide their own PATS even if they are not required/mandated by the Jira admin. Click on the <b>Provide a personal access token</b> label. A dialog for setting up personal access tokens is displayed (see below).
    </div>
    </div>
</div>

<img src='/wp-content/uploads/gij-gitcloud-setup-pat-dlg.png' style='margin:25px auto;max-width:100%;display:block;' />

*   Paste a valid PAT of the current user to proceed. Invalid PATs will fail the branch creation process.

*   Click on **New token** to generate a new PAT via your remote git host service.

*   Click **Update** to use this PAT and save it to the current user profile. Otherwise, click **Cancel** to discard setting up PAT.


Click **Create pull request** on the Create pull request dialog. The newly-created pull request is now listed in the developer panel under **Pull requests**.

This feature is available on connected GitLab, GitHub, Microsoft TFS/VSTS and AWS CodeCommit git hosts for Jira Cloud.

&nbsp;

### GitLab merge request

If you want to create a merge request for GitLab, click **Create merge request**. It has the same process described in the pull request creation steps above.

The merge request is displayed on the developer panel and will also be associated to the mentioned Jira issue by fulfilling the following condition:

*   Merge request **Title** contains the issue key. For example, `TEST-1-Fix-binaries`.

This will also allow a service user to associate a Merge/Pull Request with multiple Jira issues regardless of commit associations.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        BigBrassBand recommends service users to enable pull/merge requests webhook trigger events. This way, any changes to pull/merge requests gets reindexed quickly.
    </div>
    </div>
</div>

The Pull/merge request list provides status information about the pull/merge request if it is opened or merged. For example:

<img src='/wp-content/uploads/gij-gitcloud-devpanel-merge-req.png' style='margin:25px auto;max-width:100%;display:block;' />


Hover the mouse pointer on the pull/merge request label to see information of the repository and branch where it belongs.

<img src='/wp-content/uploads/gij-gitcloud-devpanel-merge-req-hover.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;
* * *

### Video Guide

<b style='background-color:#FFEED1; padding:1px 5px; color:#CC5900; border-radius:3px; margin: 0 5px; font-size: small;'>UPDATED VIDEO COMING SOON</b>

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/1jwzeex5qa?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin:12px 0 25px 0'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/1jwzeex5qa'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

&nbsp;
* * *

[**Prev:** Branches (Developer panel)](/git-integration-for-jira-cloud/branches-development-panel-gij-cloud)

[**Next:** Git tags](/git-integration-for-jira-cloud/git-tags-gij-cloud)

&nbsp;

### More related topics about Jira Git integration development panel

[Jira Git integration development panel](/git-integration-for-jira-cloud/jira-git-integration-development-panel-gij-cloud/) (Git Integration for Jira Cloud)

[Development panel locations](/git-integration-for-jira-cloud/development-panel-locations-gij-cloud/) (Git Integration for Jira Cloud)

[Branches (Development panel)](/git-integration-for-jira-cloud/branches-development-panel-gij-cloud/) (Git Integration for Jira Cloud)

**Pull or merge requests (Development panel)** (this page)

[Git tags](/git-integration-for-jira-cloud/git-tags-gij-cloud) (Git Integration for Jira Cloud)

