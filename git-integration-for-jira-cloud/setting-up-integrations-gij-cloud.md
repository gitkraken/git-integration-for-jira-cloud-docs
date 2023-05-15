---

title: Setting up integrations
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Setup repositories and manage them in the Git Integration app configuration in Jira.

![](/wp-content/uploads/gij-gitcloud-managed-ui-integrations-page.png)

## Introduction

Integrate your git repositories via the Git Integration for Jira app in Jira Cloud. The Git Integration app provides special integrations with GitHub, GitLab, Azure Repos and more. Start integrating your git repositories by clicking **Add integration**.

![](/wp-content/uploads/gij-gitcloud-managed-ui-sel-git-host-service-page.png)

**Cloud-hosted** Git host services can be integrated into Jira automatically. Supported git hosts listed under this group are hosted remotely in the Cloud.

**Self-hosted** (also known as self-managed) Git host serices can also be integrated into Jira automatically (except Plain git repository). Supported git hosts listed under this group are hosted by organization themselves which can also be accessed remotely by their members.

Cloud-hosted and self-hosted git host services support this feature to automatically connect multiple repositories and has an array of features not found in other types of integration. _**This is the recommended way**_.

**Webhook indexing integration** allows Jira integration for connected git repositories behind a firewall. This feature is accessible in some of the supported cloud-hosted or self-hosted git services on the list.

**Single git repository integration** (Plain Git repository) allows connections to SSH or HTTP(S) repository or specific single repositories with Jira.

## Menu access locations

After the installation, the Git Integration for Jira app repository configuration page can be accessed via:

*   Jira dashboard menu Apps ➜ **Git Integration: Manage integrations**

    ![](/wp-content/uploads/gij-gitcloud-jira-apps-manage-integrations-sel.png)

*   Jira dashboard menu Jira Settings ➜ Apps ➜ **Manage integrations** (sidebar)

    ![](/wp-content/uploads/gij-gitcloud-managed-ui-system-apps-access.png)

&nbsp;

* * *

&nbsp;

[**Prev:** Git URL ports](/git-integration-for-jira-cloud/git-url-ports-gij-cloud)

[**Next:** Git integration configuration page](/git-integration-for-jira-cloud/git-integration-configuration-page-gij-cloud)

