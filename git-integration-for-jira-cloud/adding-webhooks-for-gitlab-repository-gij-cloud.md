---

title: Adding webhooks for GitLab repository
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Merge request webhooks are now supported. <a href='/git-integration-for-jira-cloud/adding-webhooks-for-gitlab-repository-gij-cloud'>See details</a> on this page.<br>
        <p>Supported webhook events:</p>
        <ul style='margin-bottom:0px !important'>
            <li>Push events</lI>
            <li>Merge request events</li>
        </ul>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Git Integration for Jira Cloud app now supports <b>GitLab System Hooks</b> (menu Admin Area ➜ System Hooks ➜ <i>Merge Request events</i>). However, it is only available for self-hosted GitLab instances. We highly recommend that Jira administrators should use this feature as it greatly reduces the amount of configuration time to setup webhooks.
    </div>
    </div>
</div>
<br>

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/trp1frsfl4?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/trp1frsfl4'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>


<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Before you can proceed with the steps outlined on this guide, webhooks must be enabled in the Git Integration for Jira app repository configuration for your Jira Cloud instance. For more details, see <a href='/git-integration-for-jira-cloud/indexing-triggers-gij-cloud'><b>Indexing Triggers - Getting Started</b></a>.
    </div>
    </div>
</div>
<br>

## Setting up webhooks for GitLab

Configure webhook by logging in to your GitLab account:

1.  Select a repository.

    <img src='/wp-content/uploads/gij-web-hooks-gitlab-settings-c.png' width=647 height=341 style='margin:25px 0' />

2.  Go to the settings page by clicking **Settings** on the sidebar.

3.  Select **Webhooks**. The following page is displayed.

    <img src='/wp-content/uploads/gij-web-hooks-gitlab-settings-add-c.png' width=584 height=867 style='margin:25px 0' />

4.  Paste the obtained _**Secret URL**_ from the _Git Integration for Jira_ app ➜ **Webhooks** page into the _**Payload URL**_ field.

    <img src='/wp-content/uploads/gij-jira-cloud-webhook-url-loc-c1.png' width=646 height=430 style='margin:25px 0' />

5.  Select the _**Push events**_ as a triggering event option. This is the default option when creating a new webhook.

6.  Click **Add webhook** to save the new webhook settings.

<br>

## Merge request event webhook

The Git Integration for Jira app supports GitLab merge request webhooks now.

You will need to enable two (2) event triggers in your GitLab webhooks configuration _(Repo ➜ Settings ➜ Webhooks)_ for it to work properly. Select both "**Push events**" and "**Merge request events**" triggers as outlined above in **step** **5**.

<img src='/wp-content/uploads/gij-gitlab-merge-request-event-trigger-webhook.png' width=648 height=173 style='margin:25px 0;max-width:100%;display:block' />

