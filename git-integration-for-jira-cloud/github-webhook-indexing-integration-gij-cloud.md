---
title: GitHub webhook indexing integration
description: Configure webhook indexing integration for GitHub.com or GitHub Enterprise Server to work with Git Integration for Jira Cloud behind firewalls.
taxonomy:
    category: git-integration-for-jira-cloud
---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>More information:</b>
        <ul style='margin-bottom:0px;margin-top:-8px;'>
            <li><a href='/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud'>Webhook Indexing Explainer</a></li>
            <li><a href='/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud'>Feature matrix of Git Integration for Jira Cloud</a></li>
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
        Webhook indexing integration does not require indexing triggers in the git manager configuration page.
    </div>
    </div>
</div>

**On this page:**
- [Connect GitHub to Jira Cloud](#connect-github-to-jira-cloud)
- [Configure repository-level webhooks](#configure-repository-level-webhooks)
- [Configure organization-level webhooks](#configure-organization-level-webhooks)
- [Post-setup tips](#post-setup-tips)
- [Supported features](#supported-features)

&nbsp;
* * *
&nbsp;

## Connect GitHub to Jira Cloud

**Prerequisites:** Install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app on your Jira Cloud instance.

1. Go to **Apps** ➜ **Git Integration for Jira** ➜ **Settings** ➜ **Manage Integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c-2025.png)

2. Click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-2025.png)

3. Select **GitHub.com** (or **GitHub Enterprise Server** for self-hosted installations).

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-type-github-2025.png)

4. Select the **Webhook indexing** panel.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-github-2025.png)

    Webhook indexing has limited features but does not require firewall configuration.

5. Click **Add integration**. The webhook settings screen appears.

    ![](/wp-content/uploads/gij-gitcloud-webhook-indexing-github-settings-2025.png)

6. **Do not click Finish yet.** Copy the **Webhook URL** and **Secret key**, then configure webhooks in GitHub using the steps below.

&nbsp;

## Configure Repository-Level Webhooks

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/3kzzx8i8pg?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:35px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/3kzzx8i8pg'><b>here</b></a> to open in a new tab.</i>
</div>

1. Open your GitHub repository.

2. Go to **Settings** ➜ **Webhooks**.

    ![](/wp-content/uploads/gij-github-webhooks-setup-add-loc.png)

3. Click **Add webhook**.

    ![](/wp-content/uploads/gij-webhook-indexing-github-paste-sel-url-type-key.png)

4. Configure the webhook:

    a. Paste the **Webhook URL** in the **Payload URL** box.

    b. Select **application/json** as the **Content type**. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b>

    c. Paste the **Secret key** in the **Secret** box.

5. Choose which events to trigger:

    | Option | Description |
    |--------|-------------|
    | Just the push event | Sends triggers for commits and branches only |
    | Send me everything | Sends all events (may impact Jira performance) <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>NOT RECOMMENDED</b> |
    | Let me select individual events | Select **Pushes** and **Pull requests** <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b> |

6. Click **Add webhook** to save.

7. Return to Jira and click **Finish**.

&nbsp;

## Configure Organization-Level Webhooks

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/t5rrr6l1bw?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:35px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/t5rrr6l1bw'><b>here</b></a> to open in a new tab.</i>
</div>

1. Open your GitHub organization.

    ![](/wp-content/uploads/gij-github-web-acc-webhook-org-settings.png)

2. Go to **Settings** ➜ **Webhooks**.

    ![](/wp-content/uploads/gij-github-web-acc-webhook-org-add.png)

3. Click **Add webhook**.

4. Configure the webhook using the same settings as repository-level (see steps 4-5 above).

5. Click **Add webhook** to save.

6. Return to Jira and click **Finish**.

&nbsp;

## Post-Setup Tips

- Organization-level webhooks apply to all repositories within the organization.
- If webhooks fail, verify the **Payload URL**, **Secret key**, and **Content type** settings.
- Find **Webhook URL** and **Secret key** in **Actions** ➜ **Edit integration**.
- <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> Repositories appear only after triggering push or pull request events.

### Link Commits to Jira Issues

To display commits in Jira, include the Jira issue key in your commit messages. See [Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

&nbsp;

## Supported Features

The Git Roll Up tab is supported for GitHub webhook indexing integration.

![](/wp-content/uploads/gij-gitcloud-webhook-indexing-compare-vs-full.png)

| Feature | Status |
|---------|--------|
| Works behind firewall | ![](/wp-content/uploads/gij-check.png) Supported |
| View commits, branches, pull requests | ![](/wp-content/uploads/gij-check.png) Supported |
| View tags | Coming soon |
| Automation for Jira triggers | ![](/wp-content/uploads/gij-check.png) Supported |
| Smart Commits | ![](/wp-content/uploads/gij-check.png) Supported |
| Repository Browser | ![](/wp-content/uploads/gij-check.png) Supported |
| Create branches/PRs in Jira | ![](/wp-content/uploads/gij-error.png) Not supported |
| View source code | ![](/wp-content/uploads/gij-error.png) Not supported |
| Full repository history | ![](/wp-content/uploads/gij-error.png) Not supported |

**Automation triggers supported:**
- Commit created
- Branch created
- Pull request created
- Pull request declined
- Pull request merged

For complete feature details, see [Feature matrix](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud).

&nbsp;

## Related Articles

- [GitLab webhook indexing integration](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud)
- [Microsoft webhook indexing integration](/git-integration-for-jira-cloud/microsoft-webhook-indexing-integration-gij-cloud)
- [Gerrit webhook indexing integration](/git-integration-for-jira-cloud/gerrit-webhook-indexing-integration-gij-cloud)

<kbd>Last updated: December 2025</kbd>
