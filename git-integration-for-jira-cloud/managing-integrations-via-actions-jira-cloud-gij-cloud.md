---

title: Managing integrations via Actions (Jira Cloud)
description: How to use Actions to manage Git integrations and repositories
taxonomy:
    category: git-integration-for-jira-cloud

---

After integrating your repository or git host service, you can perform a set of Actions by clicking the Gear icon under the **Actions** column on the integration/repository configuration list.

&nbsp;

## Action Commands (Integration)

![](/wp-content/uploads/gij-gitcloud-manage-integration-actions-menu.png)

Use the following actions to manage integrations in Jira Cloud:

| Action | Description |
| :--- | :--- |
| _**Reindex integration**_ | Immediately starts synchronization with the selected integration and its repositories. |
| _**Edit integration**_ | Opens the page to manage connection and feature settings for the selected integration. |
| _**Disable integration**_ | Disables specific integrations if you are not using them with Jira. Enable them again when needed. |
| _**View logs**_ | Opens a dialog showing the indexing log of the selected integration. |
| _**Disconnect integration**_ | Disconnects the selected integration and removes its settings from the Git Integration for Jira Cloud app integration configuration page. |

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <b>Show integration repositories</b> command is deprecated. Integration repositories are now on the <b>Manage repositories</b> page.
    </div>
    </div>
</div>
<br>

Jump to [Edit integration](/git-integration-for-jira-cloud/edit-integration-gij-cloud) settings page documentation.

&nbsp;

## Action Commands (Repositories)

![](/wp-content/uploads/gij-gitcloud-manage-repositories-actions-menu.png)

Use the following actions to manage repositories in Jira Cloud:

| Action | Description |
| :--- | :--- |
| _**Reindex repository**_ | Immediately starts synchronization with the selected repository. |
| _**Edit repository**_ | Opens the page to manage connection and feature settings for the selected repository. |
| _**View log**_ | Opens a dialog showing the indexing log of the selected repository. |
| _**Disable repository**_ | Disables specific repositories if you are not using them with Jira. Enable them again when needed. |

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Disconnecting unused repositories</b><br>
        Disconnect or disable selected repositories if they are not used for faster integration reindex.
        <p style=margin-bottom:-10px>To disconnect a repository integration (plain git), use the relative action command from the Manage integrations page to remove its settings and clone data from Git Integration for Jira Cloud.</p>
    </div>
    </div>
</div>
<br>

Jump to [Edit repository](/git-integration-for-jira-cloud/edit-repository-gij-cloud) settings page documentation.

&nbsp;

## Action Commands (Group Selection)

Group action becomes available when selecting multiple integrations and repositories, providing streamlined processing of selected items.

![](/wp-content/uploads/gij-gitcloud-actions-group-selection-feature.png)

&nbsp;
* * *

[**Prev:** Managing repository or integration configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud)

[**Next:** Edit integration settings](/git-integration-for-jira-cloud/edit-integration-gij-cloud)

&nbsp;

### More Related Topics About Managing Repository/Integration Configuration

[Managing integration or repository configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

**Managing integrations via Actions (Jira Cloud)** (this page)

[Edit integration settings](/git-integration-for-jira-cloud/edit-integration-gij-cloud/) (Git Integration for Jira Cloud)

[Edit repository settings](/git-integration-for-jira-cloud/edit-repository-gij-cloud/) (Git Integration for Jira Cloud)

[Edit nested repository settings](/git-integration-for-jira-cloud/edit-nested-repository-settings-gij-cloud/) (Git Integration for Jira Cloud)

[SSL verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud/) (Git Integration for Jira Cloud)

[View repository indexing logs](/git-integration-for-jira-cloud/view-repository-indexing-logs-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect an integration or repository configuration](/git-integration-for-jira-cloud/removing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect a nested repository configuration](/git-integration-for-cloud/remove-a-nested-repository-gij-cloud/) (Git Integration for Jira Cloud)

[Associating project permissions](/git-integration-for-jira-cloud/associating-project-permissions-gij-cloud/) (Git Integration for Jira Cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
