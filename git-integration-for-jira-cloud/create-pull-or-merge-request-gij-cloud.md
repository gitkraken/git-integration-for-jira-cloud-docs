---

title: Create pull or merge request
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira administrator notes</b><br>
        <ul>
            <li>
                Jira users can now provide their own personal access tokens (PAT) even if they are not required/mandated by the Jira admin. See <a href="/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud">Require Personal Access Tokens for user actions (create branch/pull request)</a> for instructions on how to configure this feature.
            </li>
            <li>
                The <b>View developer tools</b> <i>permission</i> is required to view the Source Code panel (see more in <a href="/git-integration-for-jira-cloud/issue-git-source-code-panel-gij-cloud">Issue Git Source Code Panel</a>. Jira users must also have the <b>Browse Project</b> <i>permissions</i> to a project associated with a repository to view.
            </li>
            <li>
                Creating branch feature can be disabled for all Jira users (regardless of permissions) in <a href="/git-integration-for-jira-cloud/git-integration-options-gij-cloud#enable-create-pull--merge-request">General settings</a>.
            </li>
        </ul>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>GitLab note</b><br>
        GitLab uses the term Merge Request rather than Pull Request (used by the other major git services). In this article, Pull Request and Merge Request can be used interchangeably.
    </div>
    </div>
</div>
<br>

## Introduction

The **Create pull request** feature offers Jira users the ability to create a git pull request directly from the Jira issue.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/733315235/create-pull-request.png?version=2&modificationDate=1599320965937&cacheVersion=1&api=v2&width=933&height=349)

For information about creating a branch from a Jira issue - see [Create branch](/git-integration-for-jira-cloud/create-branch-gij-cloud).

## Advantages

When creating a pull request from within Jira:

*   Automatically populates the pull request title with issue key (necessary for pull request ↔ issue association) and issue summary.

*   Require each Jira user to provide their Personal Access Token for creating pull requests. This option adds some friction to creating pull requests/branches but enabling this setting will enforce the git server user permissions as well as give better attribution for the actions. See [Require Personal Access Tokens for user actions (create branch/pull request)](/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud) for more information.

*   Each Jira user can set a **Default repository** for the current Jira project. (See User settings for more information).

## Supported

*   Full feature integrations:

    *   GitHub
    *   GitLab
    *   Bitbucket Cloud
    *   AWS CodeCommit
    *   Azure DevOps
    *   Microsoft Visual Studio Team Services (VSTS)
    *   Microsoft Team Foundation Server (TFS)

*   Supported in the Atlassian Jira Cloud [iOS](https://www.atlassian.com/software/jira/mobile-app), [Android](https://www.atlassian.com/software/jira/mobile-app) and [MacOS](https://www.atlassian.com/software/jira/mac).

*   Company-managed and Team-managed Jira projects supported.

*   New and old Jira Issue View supported.

## Steps to creating a git pull request in Jira

1.  **Prerequisite:** Jira administrator configures a Full feature integration in the Git Integration for Jira Cloud app. See [Integration Guide](/git-integration-for-jira-cloud/integration-guide-gij-cloud) for more information.

2.  To access the Create pull request action - do one of the following:

    *   Enable the **Git Development panel** or

    *   Open the [Issue Git Source Code Panel](/git-integration-for-jira-cloud/issue-git-source-code-panel-gij-cloud)

3.  Click **Create pull request** in one of the panels from step 2.

4.  Select git repository.

    *   Optional: designate the repository to be the default selected repository for current Jira project.  To configure default repositories for more than one Jira project - use the [User settings](user-settings-gij-cloud/) page.

    *   Use the search box to look for the specific name of the repository that will be used.

5.  If a [personal access token is required](/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud) (and not yet provided) - follow on screen instructions to provide a [personal access token](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud) with correct permissions for selected repository.

6.  Select source branch.

7.  Select target branch.

8.  Verify pull request title is correct. Edit as desired. Note: the Jira issue key must remain in the pull request name to create the pull request ↔ Jira issue association.

9.  Click **Create pull request**.

## Video: Creating pull request from Git Development panel

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='582' src='https://fast.wistia.com/embed/iframe/rsccl5wxps?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/rsccl5wxps'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

## Video: Creating pull request from Git Source Code panel

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='582' src='https://fast.wistia.com/embed/iframe/zbjshija1o?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/zbjshija1o'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).

