---

title: Adding webhooks for GitHub repository
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
        Pull request webhooks are now supported. <a href='/git-integration-for-jira-cloud/adding-webhooks-for-github-repository-gij-cloud'>See details</a> on this page.<br>
        <p>Supported webhook events:</p>
        <ul style='margin-bottom:0px;'>
            <li>Pushes</li>
            <li>Pull requests</li>
        </ul>
    </div>
    </div>
</div>

&nbsp;
<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before you can proceed with the steps outlined on this guide, indexing triggers must be enabled in the Git Integration for Jira app repository configuration for your Jira instance. For more details, see <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'><b>Indexing Triggers - Getting Started</b></a>.
    </div>
    </div>
</div>

&nbsp;

### Setup webhooks for GitHub

Configure webhooks by logging in to your GitHub account:

1.  Select a repository.

    ![](/wp-content/uploads/gij-new-github-webhook-setting-page-c1.png)

2.  Go to the **Settings** tab.

3.  On the sidebar, select **Webhooks**.

4.  Click **Add webhook**. The following page is displayed.

    ![](/wp-content/uploads/gij-web-hooks-github-settings-add-c.png)

5.  Paste the obtained _**Secret URL**_ from the _Git Integration for Jira_ app ➜ **Indexing triggers** page into the _**Payload URL**_ field.

    ![](/wp-content/uploads/gij-gitcloud-gitmgr-indexing-triggers-url-link-loc-2025.png)

    *   Set the _**Content type**_ to **application/json**.
    *   Enter the **Secret key** into the _**Secret**_ field.

7.  Select the _**Just the push event**_ option as triggering event. This is the default option when creating a new webhook.

    Leave the **Active** setting as is. Deactivating this option will stop sending event triggers from the selected repository.

8.  Click **Add webhook** to save the new webhook settings.

&nbsp;

### Pull request event webhook

The Git Integration for Jira app supports GitHub pull request webhooks now.

You will need to enable two (2) event triggers in your GitHub webhooks configuration _(Repo ➜ Settings ➜ Webhooks)_ for it to work properly.  Under event triggers section, choose _**Let me select individual events**_ and then select both "**Pushes**" and "**Pull request**" triggers instead as outlined above in step **7**.

<img src='/wp-content/uploads/gij-github-pull-request-event-trigger-webhook.png' style='display:block;margin:25px auto;height:auto;max-width: 100%;' />

For the figure above:

*   **Just the** `push` event – This is the default configuration and this works only for commits.

*   **Send me** `everything` – This would send commits/pull requests events but is very verbose. We don't recommend this configuration.

*   **Let me select individual events** (`Pushes`/`Pull requests`) – This would work better than the second option and we recommend this configuration.

<br>

Indexing triggers will be automatically registered for each GitHub repository connected to Jira Cloud to instantly index your commits. For this to work, the connecting GitHub user must be the Organization Owner or have repository **ADMIN** rights.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Indexing triggers for GitHub will be deleted when GitHub integration is disconnected from Git Integration for Jira Cloud.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Git Integration for Jira app will index only the updated repositories as indicated by the GitHub organization or GitLab group webhook.
    </div>
    </div>
</div>
<br>

