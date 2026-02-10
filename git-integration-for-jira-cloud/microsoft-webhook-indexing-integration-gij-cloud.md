---
title: Microsoft webhook indexing integration
description: Configure webhook indexing integration for Azure DevOps, Azure Repos, VSTS, or TFS to work with Git Integration for Jira Cloud behind firewalls.
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
            <li><a href='/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud'>Feature matrix of Git Integration for Jira Cloud</a></li>
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
- [Video guide](#video-guide)
- [Connect Microsoft git services to Jira Cloud](#connect-microsoft-git-services-to-jira-cloud)
- [Configure project-level service hooks](#configure-project-level-service-hooks)
- [Configure repository-level service hooks](#configure-repository-level-service-hooks)
- [Post-setup tips](#post-setup-tips)
- [Supported features](#supported-features)

&nbsp;
* * *
&nbsp;

## Video Guide

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/5ztyu5vu5l?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:35px'>
    <i>Right click <a href='https://gitkraken.wistia.com/medias/5ztyu5vu5l'><b>here</b></a> to open in a new tab.</i>
</div>

&nbsp;

## Connect Microsoft Git Services to Jira Cloud

**Prerequisites:** Install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app on your Jira Cloud instance.

1. Go to **Apps** ➜ **Git Integration for Jira** ➜ **Settings** ➜ **Manage Integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c-2025.png)

2. Click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-2025.png)

3. Select **Visual Studio Team Services (VSTS)** or **Azure DevOps Repos**.

    ![](/wp-content/uploads/https://help.gitkraken.com/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-azure-vsts-2025.png)

4. Select the **Webhook indexing** panel.

    ![](/wp-content/uploads/gij-gij-gitcloud-managed-ui-webhook-idx-ms-vsts-2025.png)

    Webhook indexing has limited features but does not require firewall configuration.

5. Click **Add integration**. The webhook settings screen appears.

    ![](/wp-content/uploads/gij-gitcloud-webhook-indexing-azure-settings-2025.png)

6. **Do not click Finish yet.** Copy the **Webhook URL** and **Secret key**, then configure service hooks in Microsoft using the steps below.

&nbsp;

## Configure Project-Level Service Hooks

1. Open your Microsoft project.

    ![](/wp-content/uploads/gij-gitcloud-ms-azure-project-sel.png)

2. Go to **Project Settings** ➜ **Service hooks**.

    ![](/wp-content/uploads/gij-gitcloud-ms-azure-project-cfg-srv-hooks.png)

3. Click **Create subscription** (or ![](/wp-content/uploads/gij-icon-add.png) if subscriptions already exist).

    ![](/wp-content/uploads/gij-gitcloud-ms-azure-svc-hook-wiz-01.png)

4. Select **Web Hooks** and click **Next**.

    ![](/wp-content/uploads/gij-ms-azure-svc-hooks-trigger-screen.png)

5. Create three separate subscriptions for these events:

    | Event | Purpose |
    |-------|---------|
    | Code pushed | Indexes commits and branches |
    | Pull request created | Indexes new pull requests |
    | Pull request updated | Indexes pull request changes |

6. Set all **FILTERS** to **Any** and click **Next**.

    ![](/wp-content/uploads/gij-ms-azure-svc-hooks-actions-screen.png)

7. Configure the action:

    a. Paste the **Webhook URL** in the **URL** box.

    b. Paste the **Secret key** in the **Basic authentication password** box. <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b>

8. Test the configuration.

    ![](/wp-content/uploads/gij-ms-azure-test-notification.png)

9. Click **Finish** to save.

    ![](/wp-content/uploads/gij-ms-azure-svc-hooks-cfg-list.png)

10. Repeat steps 3-9 for each event type.

11. Return to Jira and click **Finish**.

&nbsp;

## Configure Repository-Level Service Hooks

Follow the same steps as project-level setup, but select a specific repository in step 6 instead of **Any**.

![](/wp-content/uploads/gij-ms-azure-svc-hooks-trigger-repo-level-repo-sel.png)

&nbsp;

## Post-Setup Tips

- If service hooks fail, verify the **URL** and **Basic authentication password** settings.
- Find **Webhook URL** and **Secret key** in **Actions** ➜ **Edit integration**.
- <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> Repositories appear only after triggering push or pull request events.

### Link Commits to Jira Issues

To display commits in Jira, include the Jira issue key in your commit messages. See [Linking git commits to Jira issues](/git-integration-for-jira-cloud/how-to-link-commits-branches-and-pull-requests-to-a-jira-issue-gij-cloud).

&nbsp;

## Supported Features

The Git Roll Up tab is supported for Microsoft webhook indexing integration.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Microsoft webhooks provide commit messages, hashes, dates, and author information only. Changed file information is not available.
    </div>
    </div>
</div>

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

For complete feature details, see [Feature matrix](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud).

&nbsp;

## Related Articles

- [GitHub webhook indexing integration](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud)
- [GitLab webhook indexing integration](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud)
- [Gerrit webhook indexing integration](/git-integration-for-jira-cloud/gerrit-webhook-indexing-integration-gij-cloud)

<kbd>Last updated: December 2025</kbd>
