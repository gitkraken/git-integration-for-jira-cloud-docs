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
        <ul>
            <li>Pushes</li>
            <li>Pull requests</li>
        </ul>
    </div>
    </div>
</div>
<br>   

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/pewl2o9uk6?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/pewl2o9uk6'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before you can proceed with the steps outlined on this guide, indexing triggers must be enabled in the Git Integration for Jira app repository configuration for your Jira instance. For more details, see <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud/'><b>Indexing Triggers - Getting Started</b></a>.
    </div>
    </div>
</div>
<br>

## Setup webhooks for GitHub

Configure webhooks by logging in to your GitHub account:

1.  Select a repository.

    ![](https://bigbrassband.atlassian.net/wiki/download/attachments/171377213/new-github-webhook-setting-page(c1).png?version=1&modificationDate=1617192156368&cacheVersion=1&api=v2)

2.  Go to the **Settings** page.

3.  Select **Webhooks**.

4.  Click **Add webhook**. The following page is displayed.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171377213/web-hooks-github-settings-add(c).png?version=1&modificationDate=1617192156377&cacheVersion=1&api=v2&width=646&height=708)

5.  Paste the obtained _**Secret URL**_ from the _Git Integration for Jira_ app  ➜ **Indexing triggers** page into the _**Payload URL**_ field.

    ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171377213/jira-cloud-webhook-url-loc(c1).png?version=1&modificationDate=1617192156381&cacheVersion=1&api=v2&width=646&height=430)

    Set the _**Content type**_ to **application/json**.

7.  Select the _**Just the push event**_ option as triggering event.  This is the default option when creating a new webhook.

8.  Click **Add webhook** to save the new webhook settings.

<br>

## Pull request event webhook

The Git Integration for Jira app supports GitHub pull request webhooks now.

You will need to enable two (2) event triggers in your GitHub webhooks configuration _(Repo > Settings > Webhooks)_ for it to work properly.  Under event triggers section, choose _**Let me select individual events**_ and then select both "**Pushes**" and "**Pull request**" triggers instead as outlined above in step **7**.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171377213/github-pull-request-event-trigger-webhook.png?version=2&modificationDate=1617192156387&cacheVersion=1&api=v2&width=612&height=302)

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
        <b>VERSION 2.12.8+</b><br>
        Git Integration for Jira app will index only the updated repositories as indicated by the GitHub organization or GitLab group webhook.
    </div>
    </div>
</div>
<br>

