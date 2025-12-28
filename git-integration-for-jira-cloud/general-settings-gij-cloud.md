---

title: General Settings
description: Configure Git Integration for Jira Cloud general settings including development panel options, branch naming, and integration features.
taxonomy:
    category: git-integration-for-jira-cloud

---

<!-- ADMINS -->

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The General Settings page is only accessible to Jira Administrators.
    </div>
    </div>
</div>

The General settings page lets administrators configure Git Integration for Jira Cloud app features. Enable or disable settings based on your organization's requirements.

**On this page:**
- [Getting started](#getting-started)
- [Enable beta features](#enable-beta-features)
- [Git Roll Up Issue Tab setting](#git-roll-up-issue-tab-setting)
- [Git Commits Issue Tab and Project Page](#git-commits-issue-tab-and-project-page)
- [Issue Git Source Code Panel setting](#issue-git-source-code-panel-setting)
- [Repository Browser settings](#repository-browser-settings)
- [Git Integration Options](#git-integration-options)
- [GitKraken Integration settings](#gitkraken-integration-settings)
- [GitLens Integration settings](#gitlens-integration-settings)
- [Jira Development Information settings](#jira-development-information-settings)

&nbsp;

* * *

&nbsp;

## Getting started

Open the **General settings** page in Jira Apps Management to enable or disable Git Integration for Jira Cloud app features.

Access **General settings** through:

*   Jira Side Bar ➜ Apps ➜ Git Integration for Jira ➜ **App settings**.

    ![](/wp-content/uploads/gij-gitcloud-gitmenu-apps-gencfg-sel-2025.png)

Click **Update** to apply your changes.

&nbsp;

* * *

&nbsp;

## Enable beta features

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        This setting is disabled in <a href='https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud'><b>Git Integration for Jira Cloud</b></a> app by default.<br>
        This setting is turned off by default in <a href='https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview'><b>Dev Info for Jira Cloud</b></a> app.
    </div>
    </div>
</div>

<img src='/wp-content/uploads/gij-gitcloud-gencfg-enable-beta-features.png' style='margin:25px auto;max-width:100%;display:block;' />

This toggle provides early access to upcoming features. Enable it to use new beta features and display them in General settings. Disable it to hide beta features.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Share feedback and ideas to help us improve current beta features. We appreciate your suggestions. If you encounter bugs or performance issues, contact us through <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>GIJ Cloud Support</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Git Roll Up Issue Tab setting

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        This setting is enabled in <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud"><b>Git Integration for Jira Cloud</b></a> app by default.<br>
        This setting is turned off by default in <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview">Dev Info for Jira Cloud</a> app.
    </div>
    </div>
</div>

### Show Git Roll Up Issue Tab

<img src='/wp-content/uploads/gij-gitcloud-gencfg-show-git-rollup-issue-tab.png' style='margin:25px auto;max-width:100%;display:block;' />

The Git Roll Up Issue tab displays a summary of files, lines, and developers who changed commits associated with a Jira issue. Toggle this setting to show or hide the **Git Roll Up** tab on Issue pages for all Jira projects.

For more details, see [**Features: Git Roll Up tab (Jira Cloud)**](/git-integration-for-jira-cloud/git-roll-up-tab-gij-cloud).

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        The <b>View developer tools</b> <i>permission</i> is required to view the Git Roll Up Issue Tab. Jira users must also have <b>Browse Project</b> <i>permissions</i> for a project associated with a repository to view.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Git Commits Issue Tab and Project Page

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        This setting is enabled in <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud" target="_blank">Git Integration for Jira Cloud</a> app by default.<br>
        This setting is turned off by default in <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview" target="_blank"><b>Dev Info for Jira Cloud</b></a> app.
    </div>
    </div>
</div>

### Show Git Commits Issue Tab and Project Page

![](/wp-content/uploads/gij-gitcloud-gencfg-show-git-commits-issue-proj-tab-2025.png)

This setting enables or disables the **Git Commits Issue tab** and the **Git Commits Project** page. These locations display git commits associated with the Jira issue and project respectively. The list groups commits by repository and sorts them by commit time.

For more details, see [**Features: Git Commits Issue tab and Project Page (Jira Cloud)**](/git-integration-for-jira-cloud/git-commits-issue-tab-and-project-pages-gij-cloud).

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        The <b>View developer tools</b> <i>permission</i> is required to view the Git Commits Issue Tab and Projects Page. Jira users must also have <b>Browse Project</b> <i>permissions</i> for a project associated with a repository to view.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Issue Git Source Code Panel setting

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        This setting is enabled in <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud" target="_blank"><b>Git Integration for Jira Cloud</b></a> app by default.<br>
        This setting is turned off by default in <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview" target="_blank"><b>Dev Info for Jira Cloud</b></a> app.
    </div>
    </div>
</div>

### Show Issue Git Source Code Panel

![](/wp-content/uploads/gij-gitcloud-gencfg-show-issue-dev-panel.png)

Toggle this setting to show or hide the _Git Integration_ section on the Jira issue developer panel.

![](/wp-content/uploads/gij-gitcloud-jira-dev-integration-panel-sel-2025.png)

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        The <b>View developer tools</b> <i>permission</i> is required to view the Git Integration panel. Jira users must also have <b>Browse Project</b> <i>permissions</i> for a project associated with a repository to view.
    </div>
    </div>
</div>

Disabling this setting improves Jira performance.

For introductory information on this feature, see [Jira git issue development panel](/git-integration-for-jira-cloud/issue-git-source-code-panel-gij-cloud).

&nbsp;

* * *

&nbsp;

## Repository Browser settings

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        <ul style='margin-bottom:0px;'>
            <li>
                This setting is enabled in <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud" target="_blank">Git Integration for Jira Cloud</a> app by default.
            </li>
            <li>
                This setting is turned off by default in <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview" target="_blank">Dev Info for Jira Cloud</a> app.
            </li>
        </ul>
    </div>
    </div>
</div>
&nbsp;

* * *

&nbsp;

## Git Integration Options

These settings take effect at the integration level for projects with connected GitLab/GitHub git hosts. Each setting is _enabled_ by default.

<img src='/wp-content/uploads/gij-gitcloud-gencfg-git-integration-options.png' style='margin:25px auto;max-width:100%;display:block;' />

### Enable create and delete branch

This setting controls branch creation and deletion functions. The Jira developer panel's ability to create or delete branches depends on this setting.

<img src='/wp-content/uploads/gij-gitcloud-dev-panel-create-branch-sel-2025.png' style='margin:25px auto;max-width:100%;display:block;' />

For detailed information on this feature, see [Creating branches](/git-integration-for-jira-cloud/create-branch-gij-cloud).

### Enable create pull or merge request

This setting controls pull/merge request creation from the Jira developer panel.

<img src='/wp-content/uploads/gij-gitcloud-dev-panel-create-PRMR-sel-2025.png'  style='margin:25px auto;max-width:100%;display:block;' />

For detailed information on this feature, see [Creating pull/merge requests](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud).

### Branch name template

<img src='/wp-content/uploads/gij-gitcloud-gencfg-branch-name-template.png' style='margin:25px auto;max-width:100%;display:block;' />

Set the **Branch Name Template** using the supported variables. Use the template to generate a default name for newly-created branches with the Create Branch dialog through the development panel of the Jira issue. Click **Examples** to view template structure examples.

Use the following template variables:

`${issuetype}` – Issue Type. The Issue type maps a custom issue type as part of the template. The mapping pattern follows this structure:<br>

`${issuetype:type0,subsitute0[,type1,substitute1,...,typeN,substituteN][,defaultsubstitute]}`

*   `typeN` - is the _**nth**_ issue type string to match.
*   `substituteN` - is the substitution string to use for _**typeN**_.
*   `defaultsubstitute` - is the substitution string to use if _**typeN**_'s match is not found. If _**defaultsubstitute**_ is blank, the lowercase version of the defined issue type is used.

`${issuekey}` – Issue Key. The Issue key appears in upper case.

`${summary}` – Issue Summary. The Summary comes from the current Jira issue and appears in lowercase; spaces are replaced with "-" (dash).

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>The Git Integration for Jira app default is:</b><br>
        <code>${issuekey}-${summary}</code><br>
        <div style='margin-bottom:-10px'>This generates the string format like "<b>PRJ-123-add-more-logging</b>" as a default value for the Create Branch and Pull/Merge Request dialogs. Where <code>PRJ-123</code> is the issue key followed by a hyphen then the summary text of the active issue page (in hyphenated lowercase form).</div>
    </div>
    </div>
</div>

`${sourcebranch}` – Source branch. The source branch from the Create Branch dialog appears in lowercase; spaces are replaced with "-" (dash).

`${projectkey}` – Project Key. The Project key appears in uppercase.

`${displayname}` -- This is the displayed name of the current user.

#### Branch name templates inner separator

<img src='/wp-content/uploads/gij-gitcloud-gencfg-branch-name-temp-inner-sep.png' style='margin:25px auto;max-width:100%;display:block;' />

This setting specifies which inner word separator to use for the branch name template. The default setting is `"-" (dash)`.

#### Max branch name length

<img src='/wp-content/uploads/gij-gitcloud-gencfg-branch-name-length.png' />

This setting lets administrators specify the maximum character length for branch names. The default value is **250** characters.

#### Branch name template examples

**Example 1:**<br>
`${issuetype}/${issuekey}-${summary}`<br>
This generates the string format like "**newfeature/PRJ-123-add-more-logging**" as a default value for branch names. Where `newfeature` is the actual issue type of the active Jira issue (in lowercase with whitespaces trimmed), `PRJ-123` is the issue key followed by a hyphen, then the summary text of the active issue page (in hyphenated lowercase form).

**Example 2:**<br>
`${issuetype:New Feature,feature,Bug Fix,bug}/${issuekey}-${summary}`<br>
This generates the string format like "**feature/PRJ-123-add-more-logging**" as a default value for branch names. This example uses a Jira issue with the _**New Feature**_ issue type—where `feature` substitutes for _issuetype_ since _type0_ matches the active Jira issue type; `PRJ-123` is the issue key followed by a hyphen, then the summary text of the active issue page (in hyphenated lowercase form).

**Example 3:**<br>
`${issuetype:Old Issue,old,Bug Fix,bug,branch}/${issuekey}-${summary}`<br>
This generates the string format like "**branch/PRJ-123-add-more-logging**" as a default value for branch names. This example uses a Jira issue with the _**New Feature**_ issue type—where `branch` substitutes for _issuetype_ since _type0..typeN_ does not match the active Jira issue type; `PRJ-123` is the issue key followed by a hyphen, then the summary text of the active issue page (in hyphenated lowercase form).

&nbsp;

* * *

&nbsp;

## GitKraken Integration settings

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        <ul style='margin-bottom:0px;'>
            <li>
                This setting is enabled in <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud" target="_blank"><b>Git Integration for Jira Cloud</b></a> app by default.
            </li>
            <li>
                This setting is turned off by default in <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview" target="_blank"><b>Dev Info for Jira Cloud</b></a> app.
            </li>
        </ul>
    </div>
    </div>
</div>

### Enable GitKraken integration

<img src='/wp-content/uploads/gij-gitcloud-gencfg-enable-gitkraken-integration-417.png' style='margin:25px auto;max-width:100%;display:block;' />

Enable deep linking to quickly move between Jira and your Git source code using the GitKraken git client. GitKraken also supports deep linking into Git Integration for Jira. For more information, see [GitKraken Integrations: Git Integration for Jira](https://support.gitkraken.com/integrations/git-integration-for-jira/).

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        The <b>View developer tools</b> <i>permission</i> is required to view git commits. Jira users must also have <b>Browse Project</b> <i>permissions</i> for a project associated with a repository to view.
    </div>
    </div>
</div>

For more details, see [Features: Deep Linking to the GitKraken Git client (Jira Cloud)](/git-integration-for-jira-cloud/deep-linking-to-the-gitkraken-client-gij-cloud).

&nbsp;

* * *

&nbsp;

## GitLens Integration settings

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        <ul style='margin-bottom:0px;'>
            <li>
                This setting is enabled in <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud" target="_blank"><b>Git Integration for Jira Cloud</b></a> app by default.
            </li>
            <li>
                This setting is turned off by default in <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview" target="_blank"><b>Dev Info for Jira Cloud</b></a> app.
            </li>
        </ul>
    </div>
    </div>
</div>

### Enable GitLens integration

<img src='/wp-content/uploads/gij-gitcloud-gencfg-enable-gitlens-integration-417.png' style='margin:25px auto;max-width:100%;display:block;' />

Enable deep linking to quickly move between Jira and your Git source code using the GitLens VSCode extension. GitLens also supports deep linking into Git Integration for Jira. For more information, see [GitLens Integrations: Git Integration for Jira](https://www.gitkraken.com/gitlens).

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        The <b>View developer tools</b> <i>permission</i> is required to view git commits. Jira users must also have <b>Browse Project</b> <i>permissions</i> for a project associated with a repository to view.
    </div>
    </div>
</div>

For more details, see [Features: Deep Linking to the GitLens (Jira Cloud)](/git-integration-for-jira-cloud/deep-linking-into-gitlens-gij-cloud).

&nbsp;

* * *

&nbsp;

## Jira Development Information settings

<img src='/wp-content/uploads/gij-gitcloud-jira-dev-info-general-settings.png' style='display:block;margin:25px auto 15px auto;max-width:100%' />

<div align=center>
    <i>The default settings for Jira Development Information are shown.</i>
</div>

### What is Jira Development Information?

[**Jira Development Information**](/git-integration-for-jira-cloud/jira-development-information-gij-cloud) is a suite of Jira Software Cloud features that put commits, branches, and pull requests in context of Jira issues. Configure these settings to push development information directly into your Jira Cloud instance.

#### General settings effect on Smart Commits commands

The following settings affect the availability of specific smart commit commands as outlined below:

<img src='/wp-content/uploads/gij-gitcloud-jira-dev-info-smart-commits-req-sel.png' style='display:block;margin:25px auto;max-width:100%' />

| When this General setting is enabled | \#time | \#label |
|:---|:---|:---|
| Jira Cloud Smart Commits | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-not-red.png) |
| Git Integration app Smart Commits | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
|Both Jira Cloud Smart and GIJ app Smart commits | ![](/wp-content/uploads/gij-matrix-open-check-green.png)<br>(doubled time and comments) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |

&nbsp;

### Send development information to Jira Cloud

<img src='/wp-content/uploads/gij-gitcloud-gencfg-jira-dev-info-send-to-cloud.png' style='display:block;margin:25px auto;max-width:100%' />

Toggle this setting to send new commit, branch, and pull request data to Jira Cloud for processing and display in various views and features.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        This setting is enabled in <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud" target="_blank"><b>Git Integration for Jira Cloud</b></a> app by default.<br>
        This setting is turned off by default in <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview" target="_blank"><b>Dev Info for Jira Cloud</b></a> app.
    </div>
    </div>
</div>

Only newly added commits, branches, and pull requests upload to Jira Cloud when enabled. To upload the entire history of an integration or repository, remove it and add it back.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        The <b>View Development Tools</b> <i>permission</i> only applies to Jira <b><i>Company-managed</i></b> projects. <b><i>Team-managed</i></b> projects do not allow permission modifications.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Turning this setting to <code>ON</code> automatically disables the <b>Enable Git Integration app Smart Commits</b> setting.
    </div>
    </div>
</div>

&nbsp;

### Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers

<img src='/wp-content/uploads/gij-gitcloud-gencfg-enable-smart-commits-automation.png' style='display:block;margin:25px auto;max-width:100%' />

This setting activates the native Atlassian Jira Cloud Smart Commit processor, supporting `#time`, `#comment`, and `#transitions` commands for triggers. It also enables [Automatic Workflow Triggers](/git-integration-for-jira-cloud/automatic-workflow-triggers-gij-cloud).

Automatic workflow triggers let you use development activity to make automatic changes in your Jira project workflows. For example, you can use workflow triggers to transition Jira issues.

For more information on Automation for Jira, see [Git Integration + Jira Automation](/git-integration-for-jira-cloud/git-integration-jira-automation-gij-cloud).

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        With both smart commits processors active, the #time and #comment commands are processed twice, resulting in duplicated results.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Compared to the other smart commit processor option, this one supports Jira Automation but lacks the <code>#label</code> command.
    </div>
    </div>
</div>

&nbsp;

### Enable Git Integration app smart commits

<img src='/wp-content/uploads/gij-gitcloud-gencfg-enable-app-smart-commits.png' style='display:block;margin:25px auto;max-width:100%' />

This setting activates GitKraken's GIJ Smart Commit processor for `#time`, `#comment`, `#transition`, and `#label` commands. For more information, see [Smart Commits documentation](/git-integration-for-jira-cloud/smart-commits-gij-cloud).

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Turning this setting to <code>ON</code> automatically disables the <b>Send Development Information to Jira Cloud</b> and <b>Enable Jira Cloud Smart Commits & Workflow Triggers</b> settings.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        With both smart commits processors active, the <code>#time</code> and <code>#comment</code> commands are processed twice, resulting in duplicated results.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Compared to the other smart commit processor option, this one does not support Jira Automation but lets you use the <code>#label</code> command.
    </div>
    </div>
</div>

&nbsp;

### Advanced: Clear Development Information

<img src='/wp-content/uploads/gij-gitcloud-gencfg-advanced-clear-dev-info.png' style='margin:25px auto;max-width:100%;display:block;' />

The **Advanced** section contains a button that lets Jira administrators clear all Development Information associated with Git Integration for Jira.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This action takes time to process and Development Information may remain visible in places until the process finishes. Expect the process to take up to one hour.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

Click **Update** to apply your configuration changes.

&nbsp;

## Related articles

[General settings for administrators](/git-integration-for-jira-cloud/general-settings-for-administrators-gij-cloud) (Git Integration for Jira Cloud)

<kbd>Last updated: December 2025</kbd>
