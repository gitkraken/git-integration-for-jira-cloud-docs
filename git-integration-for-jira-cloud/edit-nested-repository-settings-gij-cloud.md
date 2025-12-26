---

title: Edit nested repository settings
description: How to modify nested repository configuration settings
taxonomy:
    category: git-integration-for-jira-cloud

---

Modify nested repository settings via the Manage repositories page.

1.  Go to the **Manage repositories** configuration page and navigate to the nested repository to manage. Click &nbsp;<img src='/wp-content/uploads/actions-icon.png' /> Action ➜ **Edit repository**.

    ![](/wp-content/uploads/gij-cloud-edit-nested-repository-actions.png)

2.  On the Edit repository settings page, make necessary changes to the selected nested repository and then click **Save** to save your changes.

&nbsp;

For single connected nested repository integration, click <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ **Edit integration** to modify/update nested repository settings.

![](/wp-content/uploads/gij-cloud-edit-nested-single-integration-settings.png)

&nbsp;

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For Azure DevOps Server and GitHub Enterprise, by default, only PAT is available for editing, regardless of whether the integration was previously installed with user/password or not.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        When adding a nested repository to an integration, no SSH key is inherited from the integration because it does not carry the SSH key.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The login credentials are not inherited with nested repositories to interact with external APIs, and .git is based on the integration's credentials.
    </div>
    </div>
</div>

&nbsp;

## Edit Nested Repository Connection Settings

Use the options below to configure repository settings:

| Option | Description | Type |
| :--- | :--- | :--- |
| _**Display Name**_ | This is the alias that appears in the Repository/Integration column. | HOSTED<br>EXTERNAL |
| _**Repository origin**_ | Full URL to the Git origin from where the repository was cloned. | HOSTED<br>EXTERNAL |
| _**Manage credentials**_ | This section allows you to update or modify the username and password credentials if this integration uses HTTP(S) authentication. If this integration uses SSH authentication, change or update the SSH key and passphrase (if configured). | EXTERNAL |
| _**SSL Verify**_ | If set to `Disabled`, Git Integration for Jira ignores verification of SSL certificates when connecting to a remote Git server. | EXTERNAL |
| _**Main Branch**_ | Set the main branch. Default is `master`. | HOSTED<br>EXTERNAL |
| _**Indexing triggers**_ | This is the webhook URL that you can use to [set up webhook indexing triggers](https://link.bigbrassband.com/docs-webhooks-jira-cloud) for this integration. | HOSTED<br>EXTERNAL |
| _**Tags**_ | Set whether to show all tags or show only tags with matching regex pattern. For more information on git tags, see [Git tags](/git-integration-for-cloud/git-tags-gij-cloud). | HOSTED<br>EXTERNAL |
| _**Smart Commits**_ | Allows or disallows users to use the smart commits feature. | HOSTED<br>EXTERNAL |
| _**Project Permissions: Restrict to projects**_ | The default setting is **Associate with all projects**. You can restrict access to the Repository Browser and Git Commit tabs (Advanced) for the selected repository by setting the project associations. | HOSTED<br>EXTERNAL |
| _**Web Linking**_ | _Optional._<br><br>The web linking feature adds links to your git hosting provider directly into the Git Commits tab. For special integrations (Auto-Connect), this feature is configured automatically. For more information, see [Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud/). | HOSTED<br>EXTERNAL |

&nbsp;
* * *

[**Prev:** Edit repository settings](/git-integration-for-jira-cloud/edit-repository-gij-cloud/)

[**Next:** SSL verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud/)

&nbsp;

### More Related Topics About Managing Repository/Integration Configuration

[Managing integration or repository configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Managing integrations via Actions (Jira Cloud)](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud/) (Git Integration for Jira Cloud)

[Edit integration settings](/git-integration-for-jira-cloud/edit-integration-gij-cloud/) (Git Integration for Jira Cloud)

[Edit repository settings](/git-integration-for-jira-cloud/edit-repository-gij-cloud/) (Git Integration for Jira Cloud)

**Edit nested repository settings** (this page)

[SSL verify](/git-integration-for-jira-cloud/ssl-verify-gij-cloud/) (Git Integration for Jira Cloud)

[View repository indexing logs](/git-integration-for-jira-cloud/view-repository-indexing-logs-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect an integration or repository configuration](/git-integration-for-jira-cloud/removing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect a nested repository configuration](/git-integration-for-jira-cloud/removing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Associating project permissions](/git-integration-for-jira-cloud/associating-project-permissions-gij-cloud/) (Git Integration for Jira Cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
