---

title: Setting up integrations
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Setup repositories and manage them in the Git Integration app configuration in Jira.

![](/wp-content/uploads/gij-gitcloud-managed-ui-integrations-page-2025.png)

&nbsp;

**On this page:**
- [Introduction](#introduction)
- [Menu access locations](#menu-access-locations)
- [Git integration configuration page](#git-integration-configuration-page)
- [Git service integration](#git-service-integration)
- [Plain Git integration](#plain-git-integration)
- [Reindex selected](#reindex-selected)
- [More features](#more-features)

&nbsp;

* * *

&nbsp;

## Introduction

Integrate your git repositories via the Git Integration for Jira app in Jira Cloud. The Git Integration app provides special integrations with GitHub, GitLab, Azure Repos and more. Start integrating your git repositories by clicking **Add integration**.

![](/wp-content/uploads/gij-gitcloud-managed-ui-sel-git-host-service-page-2025.png)

**Cloud-hosted** Git host services can be integrated into Jira automatically. Supported git hosts listed under this group are hosted remotely in the Cloud.

**Self-hosted** (also known as self-managed) Git host services can also be integrated into Jira automatically (except Plain git repository). Supported git hosts listed under this group are hosted by organization themselves which can also be accessed remotely by their members.

Cloud-hosted and self-hosted git host services support this feature to automatically connect multiple repositories and has an array of features not found in other types of integration. _**This is the recommended way**_.

**Webhook indexing integration** allows Jira integration for connected git repositories behind a firewall. This feature is accessible in some of the supported cloud-hosted or self-hosted git services on the list.

**Single git repository integration** (Plain Git repository) allows connections to SSH or HTTP(S) repository or specific single repositories with Jira.

&nbsp;

## Menu access locations

After the installation, the Git Integration for Jira app repository configuration page can be accessed via:

*   Jira dashboard menu Apps ➜ **Git Integration: Manage integrations**

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel-2025.png)


&nbsp;

* * *

&nbsp;

## Git integration configuration page

On this page, you will be able to setup your git repositories and connect them to Jira.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

On the **Add new integration** page, the list of supported Git host services is displayed.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-sel-git-host-service-page-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

Click on the git host service that you will be working on and connect it into Jira.

Git Integration for Jira app supports one or more integration types for specific Git host service:

*   **Git service integration** – supports automatic connection and configuration of integration repositories using your Git service account or PAT.

*   **Plain Git integration** – manually connect single HTTP/HTTPS or SSH git repositories into Jira. See supported Remote Git URL examples on the connection wizard.

&nbsp;

* * *

&nbsp;

## Git service integration

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>RECOMMENDED</b>

The following are types of integration supported by Git Integration for Jira app for automatic connection of specific git host service: 

*   OAuth Git service integration
*   PAT Git service integration
*   Webhook indexing integration

See example integration support table for popular git host services:

| Git host service | OAuth integration | PAT integration | Webhook indexing |
| :--- | :---: | :---: | :---: |
| GitHub | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> |
| GitLab | <img src='/wp-content/uploads/gij-matrix-open-not-red.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> |
| Azure Repos/VSTS | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> |
| Azure DevOps/TFS | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-not-red.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> |
| AWS CodeCommit | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-not-red.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-not-red.png' width=20 height=20 /> |
| Gerrit | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-not-red.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> |
| Bitbucket | <img src='/wp-content/uploads/gij-matrix-open-check-green.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-not-red.png' width=20 height=20 /> | <img src='/wp-content/uploads/gij-matrix-open-not-red.png' width=20 height=20 /> |

### OAuth integration

<img src='/wp-content/uploads/gij-add-new-integration-oauth-sel-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

Formerly known as Full feature auto-connect integration.

Use this type of integration to connect specific git host services to Jira. This integration supports multiple connected repositories and automates most git integration settings.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>We highly recommend this type of integration for multiple repository configuration.</b>
    </div>
    </div>
</div>

For more details on supported git host services, see the full feature integration section in our [Integration Guides](/git-integration-for-jira-cloud/integration-guide-gij-cloud/).

### PAT integration

<img src='/wp-content/uploads/git-add-new-integration-pat-sel-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

This type of integration has similar features to OAuth but uses PAT (personal access token) instead to automatically connect repository integrations.

<div class="bbb-callout bbb--error">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>GitLab</b><br>
        Support for Gitlab API v3 is deprecated. We recommend to use <b>GitLab API v4</b> when adding new integrations for increased security.
    </div>
    </div>
</div>

### Webhook indexing integration

<img src='/wp-content/uploads/gij-add-new-integration-webhook-indexing-sel-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

Connect directly to a Git service by configuring webhooks to push commit, branch, pull request, and tag data to Jira Cloud.

Webhook indexing integration allows your connected git servers to work behind a firewall. However, the downside is that your integration will have limited features. For now, the supported git servers are GitHub.com, GitLab and Microsoft. More will be coming in the future.

&nbsp;

* * *

&nbsp;

## Plain Git integration

<img src='/wp-content/uploads/gij-add-new-integration-plain-git-sel-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

Manually connect single git repositories using this setup such as git protocol, SSH, HTTP/HTTPS, etc. or simply connect one specific repository.

Connected git service integrations appear in the Manage integration configuration list.

<img src='/wp-content/uploads/gij-add-new-integration-plain-git-repo-list-view-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

1.  Use the search option and filter to control integration list display.

2.  Use the checkbox to specifically select integration/repositories from the list. Pair this with actions to perform multiple configuration for selected items.

3.  Use the column headers to sort the list in ascending or descending order.

4.  Use ![](/wp-content/uploads/actions-icon.png) **Actions** to manage integration/repository settings.

The above UI descriptions also apply to the Manage repositories page since it has a similar layout.

&nbsp;

* * *

&nbsp;

## Reindex selected

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>UPDATED FEATURE</b>

In the new managed user interface, the **Reindex all** function is further improved and superseded by (1) selecting one or more integration/repositories using the checkboxes on the Manage integrations list, and then (2) performing reindex on the selected items.

<img src='/wp-content/uploads/gij-gitcloud-gitmgr-checkboxes-reindex-selected-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

This function will perform a reindex queue of all the selected integration/repository from the list.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Note</b><br>
        Reindex is not available on <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>DISABLED</b> integrations or repositories. On multiple item selection, Reindex will ignore <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>DISABLED</b> integrations or repositories. For more information on this topic, see <a href='/git-integration-for-jira-cloud/reindexing-gij-cloud'>Reindexing</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## More features

Click the **…** to see more features such as Repository browser and App settings.

<img src='/wp-content/uploads/gij-gitcloud-gitmgr-other-features-sel-2025.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

The rest of the features can also be accessed on the left sidebar of the Manage integrations page.

<img src='/wp-content/uploads/gij-gitcloud-gitmgr-sidebar-features.png' style='display:block;max-width:100%;margin:25px auto 35px auto' />

&nbsp;

* * *

&nbsp;

[**Prev:** Git URL ports](/git-integration-for-jira-cloud/git-url-ports-gij-cloud)

[**Next:** Using the Git service integration wizard](/git-integration-for-jira-cloud/using-the-git-service-integration-wizard-gij-cloud/)

