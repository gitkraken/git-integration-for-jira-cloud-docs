---

title: Migrating from Jira Server + Data Center to Jira Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---


**What’s on this page:**

## ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Let us assist you with your migration to Jira Cloud!

Use this page as a resource to get all the information you need to start your migration. If you need additional support or one-on-one assistance, we'll be glad to help. Contact us at [BigBrassBand Support](https://bigbrassband.atlassian.net/servicedesk/customer/portals/).

## ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Important Notes

**Licensing:** We’re happy to assist our customers migrate to Jira Cloud from Jira Server or Jira Data Center. To alleviate any concerns about paying for "double licensing" during your transition we will provide discount codes so you will only have to pay for one platform (either Cloud or Server/Data Center). We’ll do this by verifying your active license on one platform and we’ll provide a promotion code for the license on the other.

**Associations from Git data:** Indexing Jira issues via commit messages is the same in Jira Server + Data Center as Jira Cloud. All the associations will be preserved.

**Manual commit associations:** At this time, manual commit <--> Jira issue associations cannot be migrated automatically but request [**BigBrassBand Support**](https://bigbrassband.atlassian.net/servicedesk/customer/portals) for instructions on how to check.

**Self-hosted Git servers:** When connecting a self-hosted git server to [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) the git server must have a publicly addressable + route-able address. [GitHub.com](http://GitHub.com), [Azure DevOps](https://dev.azure.com), [GitLab.com](http://GitLab.com) and other services hosted on the “public cloud” work without any administrator interventions.

For more information, see: [**Allowlist (whitelist) BigBrassBand Cloud**](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/121241614/Whitelist+BigBrassBand+Cloud/)

**Known Atlassian issue:** We highly recommend testing your Jira migration to the Cloud on a test Jira Cloud site. [AC-1528](https://ecosystem.atlassian.net/browse/AC-1528) is a bug in Atlassian Jira Cloud that breaks all Jira Cloud Atlassian Marketplace apps when a new project import is made. When migrating your users to Jira Cloud – we recommend installing and configuring the Git Integration for Jira Cloud app **after** all of your Jira users/projects/issues data is imported and verified.

## ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Links

*   [Git Integration Server/Data Center vs Jira Cloud](/wiki/spaces/GITCLOUD/pages/656244758) - Evaluating a move to Jira Cloud? Learn more about the similarities and differences.

*   [Atlassian Migration Program](https://www.atlassian.com/migration/cloud) - Leverage the Atlassian Migration Program for step-by-step migration resources, free tools, and dedicated support.

*   [Self-guided Server to Cloud migration guide](https://www.atlassian.com/migration/cloud/guide/introduction/overview) - Migrate to Cloud using Atlassian's step-by-step guide, tools and best practices.

*   [Enterprise migration guide](https://www.atlassian.com/migration/cloud/enterprise) - For teams migrating 1,000 users or more, Atlassian offers additional resources and support.


## ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Steps to migrate

Currently there are not automatic steps to migrate from Jira Server + Data Center to Jira Cloud.

*   Create a **test** Jira Cloud instance. See below note.
*   Install [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) on a test Jira Cloud instance
*   Verify self-hosted git servers have a a publicly addressable + rout-able address. For more information, see [Whitelist BigBrassBand Cloud](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/).
*   Configure your git repositories via Full feature integrations or single, plain git repositories. For guides on connecting git servers + repositories to Jira Cloud, see [Integration Guide](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/)

*   Connect GitHub.com to Jira Cloud - see guide: [GitHub.com](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/)
*   Connect GitHub Enterprise to Jira Cloud - see guide: [GitHub Enterprise](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/)
*   Connect GitLab.com to Jira Cloud - see guide: [GitLab.com](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/)
*   Connect GitLab CE/EE to Jira Cloud - see guide: [GitLab CE/EE](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/)
*   Connect AWS CodeCommit to Jira Cloud - see guide: [AWS CodeCommit](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/)
*   Connect Bitbucket Cloud to Jira Cloud - see guide: [Bitbucket Cloud](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/)
*   Connect Microsoft Azure DevOps (Cloud) to Jira Cloud - see guide: [Azure DevOps | Visual Studio Team Services (VSTS)](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/)
*   Connect Microsoft Visual Studio Team Services (VSTS) to Jira Cloud - see guide: [Azure DevOps | Visual Studio Team Services (VSTS)](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/)
*   Connect Microsoft Azure DevOps Server to Jira Cloud - see guide: [Azure DevOps Server | Team Foundation Services (TFS)](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/)
*   Connect Microsoft Azure Team Foundation Server (TFS) to Jira Cloud - see guide: [Azure DevOps Server | Team Foundation Services (TFS)](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/)
*   Connect Gerrit to Jira Cloud - see guide: [Gerrit](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/86474926/Gerrit/)

*   Once indexing is completed, verify Jira issues are showing commits, branches, and pull requests as expected.

If you need additional support - contact [BigBrassBand Support](https://bigbrassband.atlassian.net/servicedesk/customer/portals/).