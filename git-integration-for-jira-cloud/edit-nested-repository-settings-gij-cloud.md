---

title: Edit nested repository settings
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Modify nested repository settings via the Manage repositories page.

1.  Go to the **Manage repositories** configuration page and navigate to the nested repository to manage. Click &nbsp;<img src='/wp-content/uploads/actions-icon.png' /> Action ➜ **Edit repository**.

    ![](/wp-content/uploads/gij-cloud-edit-nested-repository-actions.png)

2.  With screens similar to the Repository Settings page, make some necessary changes to the selected nested repository and then click **Save** to save your changes.
   

3.  With screens similar to the Edit repository settings page (see [next section]()), make some necessary changes to the selected nested repository and then click Save to save your changes.

&nbsp;

For single connected nested repository integration, click on <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ **Edit integration** to modify/update nested repository settings.

![](/wp-content/uploads/gij-cloud-edit-nested-single-integration-settings.png)

&nbsp;

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For Azure DevOps Server and GitHub Enterprise, by default, only PAT is available for editing. Regardless of whether the integration was previously installed with user/password or not.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        When adding a nested repository to an integration - no SSH key is inherited from the integration because it does not carry the SSH key.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The login credentials are not inherited with nested repositories to interact with external APIs and .git is based on the integration's credentials.
    </div>
    </div>
</div>

&nbsp;

## Edit nested repository connection settings

Utilize the options below for configuring repository settings:

| Option | Description | Type |
| :--- | :--- | :--- |
| _**Display Name**_ | This is the alias that will appear in the Repository/Integration column. | HOSTED<br>EXTERNAL |
| _**Repository origin**_ | Full URL to the Git origin from where the repository was cloned. | HOSTED<br>EXTERNAL |
| _**Manage credentials**_ | This section allows you to update or modify the username and password credentials, if this integration uses a HTTP(S) authentication. However, if this integration is based on SSH authentication, change or update the SSH key and passphrase (if configured). | EXTERNAL |
| _**SSL Verify**_ | If set to `Disabled`, the Git Integration for Jira app will ignore verification of SSL certificates when connecting to a remote Git server. | EXTERNAL |
| _**Main Branch**_ | Set the main branch. Default is `master`. | HOSTED<br>EXTERNAL |
| _**Indexing triggers**_ | This is the webhook URL that you can use to to [setup webhook indexing triggers](https://link.bigbrassband.com/docs-webhooks-jira-cloud) for this integration. | HOSTED<br>EXTERNAL |
| _**Tags**_ | Set whether to show all tags or show on tags with matching regex pattern. For more information on git tags, see [Git tags](/git-integration-for-cloud/git-tags-gij-cloud). | HOSTED<br>EXTERNAL |
| _**Smart Commits**_ | Allows or disallows users to use the smart commits feature. | HOSTED<br>EXTERNAL |
| _**Project Permissions: Restrict to projects**_ | The default setting is **Associate with all projects**. You can restrict access to the Repository Browser and Git Commit tabs (Advanced) for the selected repository by setting the project associations. | HOSTED<br>EXTERNAL |
| _**Web Linking**_ | _Optional._<br><br>The web linking feature adds links to your git hosting provider directly into the Git Commits tab. For special integrations (Auto-Connect), this feature is configured automatically. For more information on about this topic, see [Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud/). | HOSTED<br>EXTERNAL |

&nbsp;
* * *

[**Prev:** Connecting a nested repository](/git-integration-for-jira-cloud/adding-a-nested-repository-gij-cloud)

[**Next:** Remove a nested repository](/git-integration-for-jira-cloud/remove-a-nested-repository-gij-cloud)


