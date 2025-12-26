---

title: Associating project permissions
description: How to configure project-level permissions for Git integrations and repositories
taxonomy:
    category: git-integration-for-jira-cloud

---

Integrations and repositories can be associated with one or more Jira projects to restrict which users can view development information. All newly-connected repositories or integrations are associated with all Jira projects by default.

This feature is displayed in the following locations:

<ul>
    <li><b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>REPOSITORY</b> Manage repositories page ➜ <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ Edit repository ➜ <b>Feature settings</b>.</li>
    <li><b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>INTEGRATION</b> Manage integration page ➜ <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ Edit integration ➜ <b>Feature settings</b>.</li>
</ul>

<img src='/wp-content/uploads/gij-gitcloud-project-permissions-setting.png' style='display:block;margin:25px auto;height:auto;max-width:100%;' />

**Restrict to projects** – One or more projects can be mapped to this repository or integration to make Git Commits tabs available in the Issue pages of the associated projects. Disable the _**Associate with all projects**_ option to access this field.

**Associate with all projects** – Enable this option to associate this repository or integration with all projects. Disable this option to use the existing mapped projects from the **Restrict to projects** field. The default setting is enabled (checked).

&nbsp;

## Project Permissions Level

There are several types of project permission levels:

- [Repository level](#repository-level)
- [Integration level](#integration-level)
- [Repository level within integration](#repository-level-within-integration)

### Repository level

<div class='embed-container' style='padding-bottom: 75.21%'>
    <iframe width='709' height='533' src='https://fast.wistia.com/embed/iframe/xvzj32nxou?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/xvzj32nxou'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<div align='center' style='margin-bottom:30px;'>(<i>Updated video coming soon</i>)</div>

To configure project permissions for single connection repositories:

1.  On the Manage repositories page, click ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit repository**.

2.  On the page that appears, scroll down to **Project Permissions**.

3.  Clear the **Associate with all projects** checkbox.

4.  Click the **Restrict to projects** field, then select one or more projects from the list.

5.  Click **Update** to save the settings.

The same process applies to other single repository connections in Jira Cloud.

&nbsp;

### Integration level

<div class='embed-container' style='padding-bottom:75.21%'>
    <iframe width='709' height='533' src='https://fast.wistia.com/embed/iframe/rnm5t639cz?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/rnm5t639cz'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<div align='center' style='margin-bottom:30px'>(<i>Updated video coming soon</i>)</div>

To configure project permissions for an integration (multiple repository connection):

1.  On the Manage integrations page, click ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit integration**.

2.  On the page that appears, click **Feature settings** on the sidebar, then scroll down to the **Project Permissions** section.

3.  Clear the **Associate with all projects** checkbox.

4.  Click the **Restrict to projects** field, then select one or more projects from the list.

5.  Click **Update** to save the settings.

<p>&nbsp;</p>

### Repository level within integration

<div class='embed-container' style='padding-bottom: 75.21%'>
    <iframe width='709' height='533' src='https://fast.wistia.com/embed/iframe/fder2qnpgw?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/fder2qnpgw'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<div align='center' style='margin-bottom:30px'>(<i>Updated video coming soon</i>)</div>

To configure project permissions for repositories within an integration:

1.  On the Manage repositories page, click <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ **Edit integration** for a repository that is part of the integration (identified by the Integration column).

    For easy access, use the integration dropdown selector.

    <img src='/wp-content/uploads/gij-gitcloud-manage-integrations-actions-selector-c.png' style='margin-top:-20px' />

2.  Click a repository name (under the Repository column) to directly open its repository settings.

3.  On the page that appears, scroll down to **Project Permissions**.

4.  Clear the **Associate with all projects** checkbox.

5.  Click the **Restrict to projects** field, then select one or more projects from the list.

6.  Click **Update** to save the settings.

<p>&nbsp;</p>

## Setting Project Permissions in Jira Cloud

Project permissions are available in Git Integration for Jira Cloud. The default setting for new repository/integration connections is **Associated with all Jira projects**.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        When you update <b>integration</b> settings for project permissions, the repository settings are overwritten.
    </div>
    </div>
</div>

Watch the video below to learn about different settings for each project permissions level.

<div class='embed-container' style='padding-bottom: 67.29%'>
    <iframe width='709' height='533' src='https://fast.wistia.com/embed/iframe/nnao2x4ses?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/nnao2x4ses'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<div align='center'>(<i>Updated video coming soon</i>)</div>

&nbsp;
* * *

[**Prev:** Disconnect a nested repository configuration](/git-integration-for-jira-cloud/removing-integration-or-repository-configuration-gij-cloud/)

[**Next:** General settings for Administrators](/git-integration-for-jira-cloud/general-settings-for-administrators-gij-cloud/)

&nbsp;

### More Related Topics About Managing Repository/Integration Configuration

[Managing integration or repository configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Managing integrations via Actions (Jira Cloud)](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud/) (Git Integration for Jira Cloud)

[Edit integration settings](/git-integration-for-jira-cloud/edit-integration-gij-cloud/) (Git Integration for Jira Cloud)

[Edit repository settings](/git-integration-for-jira-cloud/edit-repository-gij-cloud/) (Git Integration for Jira Cloud)

[Edit nested repository settings](/git-integration-for-jira-cloud/edit-nested-repository-settings-gij-cloud/) (Git Integration for Jira Cloud)

[SSL verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud/) (Git Integration for Jira Cloud)

[View repository indexing logs](/git-integration-for-jira-cloud/view-repository-indexing-logs-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect an integration or repository configuration](/git-integration-for-jira-cloud/removing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect a nested repository configuration](/git-integration-for-cloud/remove-a-nested-repository-gij-cloud/) (Git Integration for Jira Cloud)

**Associating project permissions** (this page)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
