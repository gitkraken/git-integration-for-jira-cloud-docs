---

title: Microsoft webhook indexing integration
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
        For more information on Webhook indexing:
        <ul style='margin-bottom:0px;margin-top:-8px;'>
            <li>
                <a href='/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud'>Webhook Indexing Explainer</a>
            </li>
            <li>
                <a href='/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud'>Feature matrix of Git Integration for Jira Cloud</a>
            </li>
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
        With webhook indexing integration, there’s no need to enable indexing triggers in the git manager configuration page.
    </div>
    </div>
</div>

&nbsp;

### Video Guide

For a step-by-step setup guide, watch the following demonstration video:

#### Project Level

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/5ztyu5vu5l?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:35px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/5ztyu5vu5l'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

### Connect Azure Repos, Azure DevOps, Azure DevOps Server, VSTS or TFS using the Webhook Indexing integration type to Jira Cloud

The steps outlined below requires that [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app is already installed on your Jira Cloud instance. Otherwise, install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app first from the Atlassian Marketplace.

1.  On your Jira Cloud dashboard, go to Apps ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-c.png)

2.  On the Manage integrations page, click **Add integration**.

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png)

3.  For the following screen, click **Visual Studio Team Services (VSTS)** to start integration with this git service. If you're using **Azure DevOps Repos**, choose that instead.

    ![](/wp-content/uploads/https://help.gitkraken.com/wp-content/uploads/gij-gitcloud-managed-ui-git-integration-azure-vsts.png)

4.  On the following screen, click on the **Git service integration** panel for your integration type.

    ![](/wp-content/uploads/gij-gij-gitcloud-managed-ui-webhook-idx-ms-vsts.png)

5.  For this guide, click on the **Webhook indexing** panel to select it.

    While webhook indexing integration has limited features (such as no branch/pull/merge request creation etc.), this type Git service integration does not require specific configuration behind a firewall.

6.  Click **Add integration** to proceed. The screen below shows the webhook indexing settings for use with the Microsoft Azure Repos / VSTS / TFS git service webhook setup. This also adds the current webhook indexing integration to the manage integration list.

    ![](/wp-content/uploads/gij-gitcloud-webhook-indexing-github-settings.png)

7.  ![](/wp-content/uploads/bbb-alert-20.png) Before clicking **Finish**, make sure to configure webhook for your git service. Use the **Webhook URL** and the **Secret key** then **follow the steps below** for repository level or organization level webhook setup.

&nbsp;

#### Microsoft service hook setup (PROJECT LEVEL)

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>PROJECT LEVEL</b>

Open a new browser tab and login to your Microsoft web portal to setup webhook triggers for the selected _**project**_. Configure a webhook on your git service by performing the following steps:

![](/wp-content/uploads/gij-gitcloud-ms-azure-project-sel.png)

1.  On your Microsoft web portal, open a project to work on.

    ![](/wp-content/uploads/gij-gitcloud-ms-azure-project-cfg-srv-hooks.png)

2.  On the sidebar, go to **Project Settings**.

3.  Click **Service hooks**. The service hooks configuration page is displayed.

4.  Click **Create subscription** (_If there are existing configuration in the list, click_ ![](/wp-content/uploads/gij-icon-add.png) _to add a new subscription instead_). The Service hook wizard is displayed.

    ![](/wp-content/uploads/gij-gitcloud-ms-azure-svc-hook-wiz-01.png)

5.  Select a service to integrate with by scrolling down to **Web Hooks**, click on it then click **Next**. The Trigger screen is displayed.

    ![](/wp-content/uploads/gij-ms-azure-svc-hooks-trigger-screen.png)

6.  Select an event to trigger on and configure any filters. We recommend to setup the following three (3) event triggers in separate webhook subscriptions:

    i.  Code pushed

    ii.  Pull request created

    iii.  Pull request updated

7.  Set all **FILTERS** to any then click **Next** to continue. The Action screen is displayed.

    ![](/wp-content/uploads/gij-ms-azure-svc-hooks-actions-screen.png)

    a.  On the Settings - **URL** box, paste the **Webhook URL** that you got from the webhook indexing integration (_settings screen with the Finish button_).

    b.  <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> On the Settings - **Basic authentication password** box, paste the the **Secret key** from the previous section.

8.   Review your service hook setup and we recommend to test your settings. For example, test **Code push** event and **Pull request** events if it fails or succeeds.

    ![](/wp-content/uploads/gij-ms-azure-test-notification.png)

    If it returns no errors, click **Finish** on this subscription wizard to save the service hook configuration.

9.  The service hook configuration is added to the service hook list.

    ![](/wp-content/uploads/gij-ms-azure-svc-hooks-cfg-list.png)

10. Create subscriptions for **Pull request created** and **Pull request updated** with the steps outlined in [Microsoft service hook setup **PROJECT LEVEL**](#microsoft-service-hook-setup-project-level).

&nbsp;

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> After you’re done setting up the service hook with your git service (Microsoft), switch to the Jira Cloud browser tab where you left off. Click <b>Finish</b> to complete this setup.

&nbsp;

#### Microsoft service hook setup (REPOSITORY LEVEL)

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>REPOSITORY LEVEL</b>

Open a new browser tab and login to your Microsoft web portal to setup webhook triggers for the selected _**repository**_. Do the steps similar to the project level setup but choose a repository instead (see **step 7 below**).

![](/wp-content/uploads/gij-gitcloud-ms-azure-project-sel.png)

1.  On your Microsoft web portal, open a project to work on.

    ![](/wp-content/uploads/gij-gitcloud-ms-azure-project-cfg-srv-hooks.png)

2.  On the sidebar, go to **Project Settings**.

3.  Click **Service hooks**. The service hooks configuration page is displayed.

4.  Click **Create subscription** (_If there are existing configuration in the list, click_ ![](/wp-content/uploads/gij-icon-add.png) _to add a new subscription instead_). The Service hook wizard is displayed.

    ![](/wp-content/uploads/gij-gitcloud-ms-azure-svc-hook-wiz-01.png)

5.  Select a service to integrate with by scrolling down to **Web Hooks**, click on it then click **Next**. The Trigger screen is displayed.

    ![](/wp-content/uploads/gij-ms-azure-svc-hooks-trigger-repo-level-repo-sel.png)

6.  Select an event to trigger on and configure any filters. We recommend to setup the following three (3) event triggers in separate webhook subscriptions:

    1.  Code pushed

    2.  Pull request created

    3.  Pull request updated

7.  Set all **FILTERS** to any then click **Next** to continue. The Action screen is displayed.

    ![](/wp-content/uploads/gij-ms-azure-svc-hooks-actions-screen.png)

    a.  On the Settings - **URL** box, paste the **Webhook URL** that you got from the webhook indexing integration (_settings screen with the Finish button_).

    b.  <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> On the Settings - **Basic authentication password** box, paste the the **Secret key** from the previous section.

8.   Review your service hook setup and we recommend to test your settings. For example, test **Code push** event and **Pull request** events if it fails or succeeds.

    ![](/wp-content/uploads/gij-ms-azure-test-notification.png)

    If it returns no errors, click **Finish** on this subscription wizard to save the service hook configuration.

9.  The service hook configuration is added to the service hook list.

    ![](/wp-content/uploads/gij-ms-azure-svc-hooks-cfg-list.png)

10. Create subscriptions for **Pull request created** and **Pull request updated** with the steps outlined in [Microsoft service hook setup **REPOSITORY LEVEL**](#microsoft-service-hook-setup-repository-level).

&nbsp;

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> After you’re done setting up the service hook with your git service (Microsoft), switch to the Jira Cloud browser tab where you left off. Click <b>Finish</b> to complete this setup.

&nbsp;

### Post webhook setup tips

*   If you see any issues with the newly added service hook, verify that the **Webhook URL** from the Microsoft webhook indexing page is copied and pasted properly to the **URL** box in the Service hook wizard. Edit the these settings and try again.

*   Edit integration settings via **Actions** on the Manage Git repository page. In here, you will find **Webhook URL** and **Secret key** for use with service hook setup with your Microsoft git service.

*   <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT!</b> The events are detected only after the Webhook indexing integration. If you see no repositories in the Manage repositories page, make sure to trigger either the push (commit) or pull/merge request events of the working repository.

### How to link commits, branches and pull requests to a Jira issue?

Make a commit if you don’t see commits in the Git Commits tab of an associated Jira issue.

For information on this topic, see [Linking git commits, associating branches and pull requests to a Jira issue](/git-integration-for-jira-cloud/how-to-link-commits-branches-and-pull-requests-to-a-jira-issue-gij-cloud).

### Git Roll Up tab

The Git Roll Up tab is now supported for MS VSTS/Azure webhook indexing integration.

<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>NOTE!</b> MS VSTS/Azure doesn't provide information about changed files. It provides only commit message and hashes, dates and author information.

### Limited features for Microsoft webhook indexing integration

The feature table displays the supported git features for the selected git server. For more information, see [Feature matrix for Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud/).

![](/wp-content/uploads/gij-gitcloud-webhook-indexing-compare-vs-full-gitlab.png)

#### Works with git servers behind firewall

The webhooks indexing integration limits the features available. However, networks hosting git do not need to be updated to allow incoming requests as long as outbound requests can be made. See [Webhook Indexing explainer](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud) for more information.

#### ![](/wp-content/uploads/gij-check.png) View commits, branches, pull requests in Jira

Commits, branches, pull requests are visible in the **Jira Development Information** panel as well as in the **Git Commits issue** tab and **Git Integration** side panel of the Jira issue. Jira administrators can regulate access to these displays using the _View development tools_ permission.

![](/wp-content/uploads/gij-gitcloud-jira-issue-git-commits-tab-wh-idx-azure.png)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira issue Git Roll Up tab</b><br>
        With Microsoft webhook indexing integration, the Git Roll Up tab only provides commit message and hashes, dates and author information. It does not offer information about changed files.
    </div>
    </div>
</div>

&nbsp;

#### View tags in Jira

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b>

&nbsp;

#### ![](/wp-content/uploads/gij-check.png) Support for Automation for Jira + Smart Commits

**Automation for Jira** - the following triggers are supported:

1.  `Commit created`

2.  `Branch created`

3.  `Pull request created`

4.  `Pull request declined`

5.  `Pull request merged`

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Smart Commits:</b><br>
        Atlassian’s Smart Commits are enabled by default. Additional Smart Commit commands are available. See <a href='/git-integration-for-jira-cloud/smart-commits-gij-cloud'>Smart Commits</a> for more information.
    </div>
    </div>
</div>

&nbsp;

#### ![](/wp-content/uploads/gij-check.png) Repository Browser

The Repository Browser allows users to view commits in git repositories by branch1. Users can manually link and unlink commits to Jira issues2.

*   Click a git repository on the **View all repositories** page to start from here.

![](/wp-content/uploads/gij-gitcloud-wh-idx-repo-browser-sel.png)

#### ![](/wp-content/uploads/gij-error.png) Create branches and pull requests in Jira

This feature is not supported with webhook indexing integration. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud)

#### Support for large number of commits in git pushes

Git servers may truncate how much of the activity is captured in a webhook on large git push events resulting in some git activity. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud).

#### ![](/wp-content/uploads/gij-error.png) Indexing full repository history

Webhook indexing integration will only show new commit/branch/pull request activity once webhooks are configured on the git server according to this wizard. For more information, see [Feature matrix of Git Integration for Jira Cloud](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud).

#### ![](/wp-content/uploads/gij-error.png) View source code in Jira

Webhook indexing integration does not have this option as webhooks do not contain source code.

&nbsp;

### Other supported webhook indexing integration articles

[GitHub webhook indexing integration](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud)

[GitLab webhook indexing integration](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud)

**Microsoft webhook indexing integration** (this page)

_Gerrit webhook indexing integration (Coming soon)_

