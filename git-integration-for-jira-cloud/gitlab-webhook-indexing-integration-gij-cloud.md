---
title: GitLab webhook indexing integration
description: Configure webhook indexing integration for GitLab.com or GitLab CE/EE to work with Git Integration for Jira Cloud behind firewalls.
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
            <li><a href='/git-integration-for-jira-cloud/features-gij-cloud'>Feature matrix of Git Integration for Jira Cloud</a></li>
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
- [Video guides](#video-guides)
- [Connect GitLab to Jira Cloud](#connect-gitlab-to-jira-cloud)
- [Configure repository-level webhooks](#configure-repository-level-webhooks)
- [Configure group-level webhooks](#configure-group-level-webhooks)
- [Post-setup tips](#post-setup-tips)
- [Supported features](#supported-features)

&nbsp;
* * *
&nbsp;

## Video Guides

### Repository-Level Setup

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/ejgouua9x4?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:35px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/ejgouua9x4'><b>here</b></a> to open in a new tab.</i>
</div>

### Group-Level Setup

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/uh616awfnj?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:35px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/uh616awfnj'><b>here</b></a> to open in a new tab.</i>
</div>

&nbsp;

## Connect GitLab to Jira Cloud

**Prerequisites:** Install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app on your Jira Cloud instance.

1. Go to **Apps** ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2. Click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3. Select **GitLab.com** (or **GitLab Server** for self-hosted installations).

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-type-gitlab-com.png)

4. Select the **Webhook indexing** panel.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-gitlab.png)

    Webhook indexing has limited features but does not require firewall configuration.

5. Click **Add integration**. The webhook settings screen appears.

    ![](/wp-content/uploads/gij-gitcloud-webhook-indexing-github-settings.png)

6. **Do not click Finish yet.** Copy the **Webhook URL** and **Secret key**, then configure webhooks in GitLab using the steps below.

&nbsp;

## Configure Repository-Level Webhooks

1. Open your GitLab repository.

    ![](/wp-content/uploads/gij-gitlab-web-repo-webhook-cfg-portal-sample.png)

2. Go to **Settings** ➜ **Webhooks**.

3. Configure the webhook:

    ![](/wp-content/uploads/gij-webhook-indexing-GITLAB-paste-sel-url-type-key.png)

    a. Paste the **Webhook URL** in the **URL** box.

    b. Paste the **Secret key** in the **Secret token** box.

4. Select which events to trigger:

    | Event | Recommendation |
    |-------|----------------|
    | Push events | <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b> Sends triggers for commits and branches |
    | Tags push events | Coming soon |
    | Merge request events | <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b> Sends triggers for merge requests |

5. Click **Add webhook** to save.

6. Return to Jira and click **Finish**.

&nbsp;

## Configure Group-Level Webhooks

1. Open your GitLab group.

    ![](/wp-content/uploads/gij-gitlab-web-group-webhook-cfg-portal-sample-.png)

2. Go to **Settings** ➜ **Webhooks**.

3. Configure the webhook using the same settings as repository-level (see steps 3-4 above).

    ![](/wp-content/uploads/gij-webhook-indexing-GITLAB-paste-sel-url-type-key.png)

4. Click **Add webhook** to save.

5. Return to Jira and click **Finish**.

&nbsp;

## Post-Setup Tips

- Group-level webhooks apply to all repositories within the group.
- If webhooks fail, verify the **Payload URL** and **Secret key** settings.
- Find **Webhook URL** and **Secret key** in **Actions** ➜ **Edit integration**.
- <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> Repositories appear only after triggering push or merge request events.

### Link Commits to Jira Issues

To display commits in Jira, include the Jira issue key in your commit messages. See [Linking git commits to Jira issues](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud).

&nbsp;

## Supported Features

The Git Roll Up tab is supported for GitLab webhook indexing integration.

![](/wp-content/uploads/gij-gitcloud-webhook-indexing-compare-vs-full-gitlab.png)

| Feature | Status |
|---------|--------|
| Works behind firewall | ![](/wp-content/uploads/gij-check.png) Supported |
| View commits, branches, merge requests | ![](/wp-content/uploads/gij-check.png) Supported |
| View tags | Coming soon |
| Automation for Jira triggers | ![](/wp-content/uploads/gij-check.png) Supported |
| Smart Commits | ![](/wp-content/uploads/gij-check.png) Supported |
| Repository Browser | ![](/wp-content/uploads/gij-check.png) Supported |
| Create branches/MRs in Jira | ![](/wp-content/uploads/gij-error.png) Not supported |
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

- [GitHub webhook indexing integration](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud)
- [Microsoft webhook indexing integration](/git-integration-for-jira-cloud/microsoft-webhook-indexing-integration-gij-cloud)
- [Gerrit webhook indexing integration](/git-integration-for-jira-cloud/gerrit-webhook-indexing-integration-gij-cloud)

<kbd>Last updated: December 2025</kbd>
