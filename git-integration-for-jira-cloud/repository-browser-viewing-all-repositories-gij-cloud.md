---

title: Repository Browser - Viewing all repositories
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
        <b>Default Settings</b><br>
        <ul style='margin-bottom:0px'>
            <li>
                By default, <a href="https://marketplace.atlassian.com/4984" target="_blank">Git Integration for Jira</a> ) has the Repository Browser enabled. (<a href="#">How to disable</a>)
            </li>
            <li>
                By default, <a href="https://marketplace.atlassian.com/1219270" target="_blank">Dev Info for Jira</a> has the Repository Browser disabled. (<a href="#">How to enable</a>)
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
        The <b>View developer tools</b> <i>permission</i> is required to view the Git Roll Up Issue Tab (Jira developer panel). Jira users must also have the <b>Browse Project</b> <i>permissions</i> to a project associated with a repository to view.
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

## Introduction

The Repository Browser is a feature that offers a view into your connected repositories into Jira Cloud. From the Repository browser page you can see summaries of the following:

*   Repository

*   Most recent issue associated by a commit

*   Last updated by commit author

*   Last commit date/time

*   [Personal Access Token management](#Personal-access-column)

&nbsp;

## Repository browser

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-access-feature.png)

To access the Repository browser:

1.  On your Jira Cloud dashboard, go to menu Apps ➜ **Git Integration: Repository browser**; or

2.  On your Jira Cloud dashboard, go to menu Apps ➜ Git Integration: Manage Git repositories ➜ **Repository browser** (sidebar).

<br>

While on the Repository browser page:

*   Use the search function to search for one or more repository containing the specified name

*   Click on a repository to view Commits and Compare tabs.

*   Click on **Go to User Settings: Git integration** to access the [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) page for setting up connected apps, default repositories, default branches and personal access tokens configuration.

*   Click on **Manage Git repositories** to go to the Git integration repositories configuration page.

<br>

## Personal access column

Jira administrators can configure git integrations (example: GitHub, GitLab) to require that Jira users create and provide their own [Personal Access Token](/git-integration-for-jira-cloud/personal-access-token-feature-gij-cloud) to enable features like creating branches, pull request or merge request via Jira Git integration development panel inside Jira.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The personal access column and configuration is relocated to <a href='/git-integration-for-jira-cloud/user-settings-gij-cloud'>User settings</a>.
    </div>
    </div>
</div>
<br>



<br>

## How can a Jira administrator enable or disable the Repository browser?

1.  Install the [Git Integration for Jira](https://marketplace.atlassian.com/4984) or the [Dev Info for Jira](https://marketplace.atlassian.com/1219270) app.

2.  Navigate to the [General settings](/git-integration-for-jira-cloud/general-settings-gij-cloud) page of the application.

3.  Enable or disable the setting – **Show Repository browser: View all repositories, Commits and Compare pages**.

4.  Click **Update** button.

    ![](/wp-content/uploads/gij-gitcloud-gencfg-repo-browser-new.png)

<br>

For detailed information about this feature, see [Documentation: Repository browser](/git-integration-for-jira-cloud/repository-browser-gij-cloud).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:support@gitkraken.com'>support@gitkraken.com</a>.
    </div>
    </div>
</div>
<br>

