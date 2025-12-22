---

title: Issue Git Source Code Panel
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Features</b><br>
        <ul style='margin-bottom:0px'>
            <li>
                By default, <a href="https://marketplace.atlassian.com/4984" target="_blank">Git Integration for Jira</a> has the Git Source Code Panel enabled. (<a href="#how-can-a-jira-administrator-enable-or-disable-the-issue-git-source-code-panel">How to disable</a>)
            </li>
            <li>
                By default, <a href="https://marketplace.atlassian.com/1219270" target="_blank">Dev Info for Jira</a> has the Git Source Code Panel disabled. (<a href="#how-can-a-jira-administrator-enable-or-disable-the-issue-git-source-code-panel">How to enable</a>)
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
        The <b>View developer tools</b> <i>permission</i> is required to view the Git Source Code Panel (Git integration panel). Jira users must also have the <b>Browse Project</b> <i>permissions</i> to a project associated with a repository to view.
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

### Introduction

The Issue Git Source Code Panel displays:

*   Git Commits: # of commits and link to [Git Commits Issue Tab](/git-integration-for-jira-cloud/git-commits-issue-tab-and-project-page-gij-cloud), link to [Git Roll Up Issue Tab](/git-integration-for-jira-cloud/git-roll-up-issue-tab-gij-cloud)

*   Branches: Create branch function, list of branches associated to Jira issue (Jira issue key must be in branch title)

*   Pull/Merge Requests: Create pull/merge request function, list of pull/merge requests associated to Jira issue (Jira issue key must be in PR/MR title), status of pull/merge request

*   Tags: git tags associated to Jira issue (via associated commit). Tags are sometimes referred to as Releases in some products.

&nbsp;

### Git Source Code Panel (old issue view)

![](/wp-content/uploads/gij-git-cloud-oldview-source-code-panel.png)

&nbsp;

### Git Source Code Panel (New issue view & next-gen projects)

The Git Commits Issue tab lists the git commits associated to the Jira issue grouped by repository and sorted by commit time. 

![](/wp-content/uploads/gij-git-cloud-newview-source-code-panel.png)

&nbsp;

### How can a Jira administrator enable or disable the Issue Git Source Code Panel?

1.  Install the [Git Integration for Jira](https://marketplace.atlassian.com/4984) or the [Dev Info for Jira](https://marketplace.atlassian.com/1219270) app

2.  Navigate to the **General settings** page of the application.

3.  Enable or disable the setting: [Show Git Source Code Panel](/git-integration-for-jira-cloud/general-settings-gij-cloud#issue-git-source-code-panel-setting).

4.  Click **Update** button.

![](/wp-content/uploads/gij-gitcloud-general-settings-git-source-code-panel-1455.png)

&nbsp;

For detailed information about this feature, see [Documentation: Jira Git integration development panel](/git-integration-for-jira-cloud/jira-issue-page-gij-cloud#jira-git-integration-development-panel).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a>  or email us at <a href='mailto:support@gitkraken.com'>support@gitkraken.com</a>.
    </div>
    </div>
</div>

### See more features

[Deep linking feature](/git-integration-for-jira-cloud/deeplinking-feature-gij-cloud/)

[CI / CD for Jira Cloud](/git-integration-for-jira-cloud/cicd-getting-started-with-ci-cd-for-jira-gij-cloud/)

[Git Integration + Jira Automation](/git-integration-for-jira-cloud/git-integration-jira-automation-gij-cloud/)

[Jira Development Information](/git-integration-for-jira-cloud/jira-issue-page-gij-cloud#jira-development-information)

[JQL Searching for Commits and Pull Requests](/git-integration-for-jira-cloud/jql-searching-for-commits-and-pull-requests-gij-cloud/)

[Jira Cloud Smart Commits and Workflow Triggers](/git-integration-for-jira-cloud/smart-commits-gij-cloud#jira-cloud-smart-commits-and-workflow-triggers)

[Git Roll Up Issue Tab features](/git-integration-for-jira-cloud/git-roll-up-issue-tab-gij-cloud/)

[Git Commits Issue Tab and Project Pages](/git-integration-for-jira-cloud/git-commits-issue-tab-and-project-pages-gij-cloud/)

**Issue Git Source Code Panel** (this page)

[Create branch](/git-integration-for-jira-cloud/create-branch-gij-cloud/)

[Create pull or merge request](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud/)

[Repository Browser – Viewing all repositories](/git-integration-for-jira-cloud/repository-browser-gij-cloud)

[Classic Indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud/)

[Webhook Indexing Explainer](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud/)

[Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud/)

[Git Integration Server/Data Center vs Jira Cloud – Feature Comparison](/git-integration-for-jira-cloud/git-integration-server-data-center-vs-jira-cloud-feature-comparison-gij-cloud/)

[Migrating from Jira Server + Data Center to Jira Cloud](/git-integration-for-jira-cloud/migrating-from-jira-server-data-center-to-jira-cloud-gij-cloud/)

[User Settings](/git-integration-for-jira-cloud/user-settings-gij-cloud/)

