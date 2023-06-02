---

title: Git integration options
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This setting is part of the [**General Settings**](/git-integration-for-jira-cloud/general-settings-gij-cloud) configuration page for Git Integration for Jira Cloud.


These settings will take effect at integration level for projects with connected GitLab/GitHub git hosts. The default state for each setting is _enabled_.

<img src='/wp-content/uploads/gij-gitcloud-gencfg-git-integration-options.png' style='margin:25px auto;max-width:100%;display:block;' />


**What’s on this page:**
- [Git integration settings](#git-integration-settings)
  - [Enable create \/ delete branch](#enable-create--delete-branch)
  - [Enable create pull \/ merge request](#enable-create-pull--merge-request)
- [Branch name template](#branch-name-template)
- [Branch name templates inner separator](#branch-name-templates-inner-separator)
- [Max branch name length](#max-branch-name-length)
- [Some examples](#some-examples)

&nbsp;
* * *
&nbsp;

### Enable create \/ delete branch
This setting shows or hides the function for creating/deleting of branches. The ability to create/delete selected branches from the Jira developer panel is dependent on this setting.

<img src='/wp-content/uploads/gij-gitcloud-dev-panel-create-branch-sel.png' style='margin:25px auto;max-width:100%;display:block;' />

For detailed information on this feature, see [Creating branches](/git-integration-for-jira-cloud/create-branch-gij-cloud).

&nbsp;

### Enable create pull \/ merge request

This setting shows or hides the function for creating pull/merge requests from the Jira developer panel.

<img src='/wp-content/uploads/gij-gitcloud-dev-panel-create-PRMR-sel.png'  style='margin:25px auto;max-width:100%;display:block;' />

For detailed information on this feature, see [Creating pull/merge requests](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud).

&nbsp;

## Branch name template

<img src='/wp-content/uploads/gij-gitcloud-gencfg-branch-name-template.png' style='margin:25px auto;max-width:100%;display:block;' />

Set the **Branch Name Template** using the supported variables. Use the template to generate a default name for newly-created branches with the Create Branch dialog via the development panel of the Jira issue. Click/expand **Examples** to view template structure examples.

Use the following template variables:

`${issuetype}` – Issue Type. The Issue type is used to map a custom issue type as part of the template. The mapping pattern should look like this:<br>

`${issuetype:type0,subsitute0[,type1,substitute1,...,typeN,substituteN][,defaultsubstitute]}`

*   `typeN` - is the _**nth**_ issue type string to match.

*   `substituteN` - is the substitution string to use for _**typeN**_.

*   `defaultsubstitute` - is the substitution string to use if _**typeN**_'s match is not found. If _**defaultsubstitute**_ is blank, the lowercase version of the defined issue type is used.

`${issuekey}` – Issue Key. The Issue key is used in upper case.

`${summary}` – Issue Summary. The Summary is used from the current Jira issue your are on and will be in lowercase; spaces are substituted by "-" (dash).

 <div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>The Git Integration for Jira app default is:</b><br>
        <code>${issuekey}-${summary}</code><br>
        <div style='margin-bottom:0px'>This generates the string format like "<b>PRJ-123-add-more-logging</b>" as a default value for the Create Branch and Pull/Merge Request dialogs. Where <code>PRJ-123</code> is the issue key followed by a hyphen then the summary text of the active issue page (in hyphenated lowercase form).</div>
    </div>
    </div>
</div>

`${sourcebranch}` – Source branch. The source branch from the Create Branch dialog is used and will be in lowercase; spaces are substituted by “-” (dash).

`${projectkey}` – Project Key. The Project key is used and will be in uppercase.

`${displayname}` -- This is the displayed name of the current user.

&nbsp;

## Branch name templates inner separator

<img src='/wp-content/uploads/gij-gitcloud-gencfg-branch-name-temp-inner-sep.png'style='margin:25px auto;max-width:100%;display:block;' />'

This setting applies which inner word separator to use for the branch name template. The default setting is `"-" (dash)`.

&nbsp;

## Max branch name length

<img src='/wp-content/uploads/gij-gitcloud-gencfg-branch-name-length.png?version=1&modificationDate=1645097669336&cacheVersion=1&api=v2&width=511&height=73)

This setting allows administrators to specify the maximum character length for branch names. The default value is **250** chars.

&nbsp;
* * *
&nbsp;

## Some examples

**Example 1:**<br>
`${issuetype}/${issuekey}-${summary}`<br>
This generates the string format like "**newfeature/PRJ-123-add-more-logging**" as a default value for the branch names. Where `newfeature` is the actual issue type of the active Jira issue; in lowercase and trimmed of whitespaces, `PRJ-123` is the issue key followed by a hyphen then the summary text of the active issue page (in hyphenated lowercase form).

**Example 2:**<br>
`${issuetype:New Feature,feature,Bug Fix,bug}/${issuekey}-${summary}`<br>
This generates the string format like "**feature/PRJ-123-add-more-logging**" as a default value for the branch names. This example uses a Jira issue which has the _**New Feature**_ issue type -- where `feature` is the substituted to _issuetype_ since _type0_ matches the active Jira issue type; `PRJ-123` is the issue key followed by a hyphen then the summary text of the active issue page (in hyphenated lowercase form).

**Example 3:**<br>
`${issuetype:Old Issue,old,Bug Fix,bug,branch}/${issuekey}-${summary}`<br>
This generates the string format like "**branch/PRJ-123-add-more-logging**" as a default value for the branch names. This example uses a Jira issue which has the _**New Feature**_ issue type -- where `branch` is substituted to _issuetype_ since _type0..typeN_ does not match the active Jira issue type; `PRJ-123` is the issue key followed by a hyphen then the summary text of the active issue page (in hyphenated lowercase form).

&nbsp;
* * *

After all the settings have been configured according to your requirements, click **Update** to apply the changes.

&nbsp;

## More General settings options

[Enable beta features setting](/git-integration-for-jira-cloud/enable-beta-features-setting-gij-cloud)

[Git roll up issue tab setting](/git-integration-for-jira-cloud/git-roll-up-issue-tab-setting-gij-cloud)

[Git commits issue tab and project page](/git-integration-for-jira-cloud/git-commits-issue-tab-and-project-page-gij-cloud)

[Issue git source code panel setting](/git-integration-for-jira-cloud/issue-git-source-code-panel-setting-gij-cloud)

[Repository browser settings](/git-integration-for-jira-cloud/repository-browser-settings-gij-cloud)

[GitKraken integration settings](/git-integration-for-jira-cloud/gitkraken-integration-settings-gij-cloud)

[GitLens integration settings](/git-integration-for-jira-cloud/gitlens-integration-settings-gij-cloud)

**Git integration options** (this page)

[Jira development information settings](/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud)

[General settings for administrators](/git-integration-for-jira-cloud/general-settings-for-administrators-gij-cloud)

