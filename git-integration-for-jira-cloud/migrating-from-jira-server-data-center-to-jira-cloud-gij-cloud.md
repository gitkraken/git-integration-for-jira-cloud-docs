---

title: Migrating from Jira Server + Data Center to Jira Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---


**What’s on this page:**

## Let us assist you with your migration to Jira Cloud!

Use this page as a resource to get all the information you need to start your migration. If you need additional support or one-on-one assistance, we'll be glad to help. Contact us at [BigBrassBand Support](https://bigbrassband.atlassian.net/servicedesk/customer/portals/).

## Important Notes

**Licensing:** We’re happy to assist our customers migrate to Jira Cloud from Jira Server or Jira Data Center. To alleviate any concerns about paying for "double licensing" during your transition we will provide discount codes so you will only have to pay for one platform (either Cloud or Server/Data Center). We’ll do this by verifying your active license on one platform and we’ll provide a promotion code for the license on the other.

**Associations from Git data:** Indexing Jira issues via commit messages is the same in Jira Server + Data Center as Jira Cloud. All the associations will be preserved.

**Manual commit associations:** At this time, manual commit <--> Jira issue associations cannot be migrated automatically but request [**BigBrassBand Support**](https://bigbrassband.atlassian.net/servicedesk/customer/portals) for instructions on how to check.

**Self-hosted Git servers:** When connecting a self-hosted git server to [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) the git server must have a publicly addressable + route-able address. [GitHub.com](http://GitHub.com), [Azure DevOps](https://dev.azure.com), [GitLab.com](http://GitLab.com) and other services hosted on the “public cloud” work without any administrator interventions.

For more information, see: [**Allowlist (whitelist) BigBrassBand Cloud**](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud)

**Known Atlassian issue:** We highly recommend testing your Jira migration to the Cloud on a test Jira Cloud site. [AC-1528](https://ecosystem.atlassian.net/browse/AC-1528) is a bug in Atlassian Jira Cloud that breaks all Jira Cloud Atlassian Marketplace apps when a new project import is made. When migrating your users to Jira Cloud – we recommend installing and configuring the Git Integration for Jira Cloud app **after** all of your Jira users/projects/issues data is imported and verified.

## Links

*   [Git Integration Server/Data Center vs Jira Cloud](/git-integration-for-jira-cloud/git-integration-server-data-center-vs-jira-cloud-feature-comparison-gij-cloud) - Evaluating a move to Jira Cloud? Learn more about the similarities and differences.

*   [Atlassian Migration Program](https://www.atlassian.com/migration/cloud) - Leverage the Atlassian Migration Program for step-by-step migration resources, free tools, and dedicated support.

*   [Self-guided Server to Cloud migration guide](https://www.atlassian.com/migration/cloud/guide/introduction/overview) - Migrate to Cloud using Atlassian's step-by-step guide, tools and best practices.

*   [Enterprise migration guide](https://www.atlassian.com/migration/cloud/enterprise) - For teams migrating 1,000 users or more, Atlassian offers additional resources and support.


## Steps to migrate

Currently there are not automatic steps to migrate from Jira Server + Data Center to Jira Cloud.

*   Create a **test** Jira Cloud instance. See below note.
*   Install [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) on a test Jira Cloud instance
*   Verify self-hosted git servers have a a publicly addressable + rout-able address. For more information, see [Whitelist BigBrassBand Cloud](https://bigbrassband.atlassian.net/git-integration-for-jira-cloud/).
*   Configure your git repositories via Full feature integrations or single, plain git repositories. For guides on connecting git servers + repositories to Jira Cloud, see [Integration Guide](/git-integration-for-jira-cloud/integration-guide-gij-cloud)

*   Connect GitHub.com to Jira Cloud - see guide: [GitHub.com](/git-integration-for-jira-cloud/github-com-gij-cloud)
*   Connect GitHub Enterprise to Jira Cloud - see guide: [GitHub Enterprise](/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud)
*   Connect GitLab.com to Jira Cloud - see guide: [GitLab.com](/git-integration-for-jira-cloud/gitlab-com-gij-cloud)
*   Connect GitLab CE/EE to Jira Cloud - see guide: [GitLab CE/EE](/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud)
*   Connect AWS CodeCommit to Jira Cloud - see guide: [AWS CodeCommit](/git-integration-for-jira-cloud/aws-codecommit-gij-cloud)
*   Connect Bitbucket Cloud to Jira Cloud - see guide: [Bitbucket Cloud](/git-integration-for-jira-cloud/bitbucket-cloud/)
*   Connect Microsoft Azure DevOps (Cloud) to Jira Cloud - see guide: [Azure DevOps | Visual Studio Team Services (VSTS)](/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud)
*   Connect Microsoft Azure DevOps Server to Jira Cloud - see guide: [Azure DevOps Server | Team Foundation Services (TFS)](/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud)
*   Connect Gerrit to Jira Cloud - see guide: [Gerrit](/git-integration-for-jira-cloud/gerrit-gij-cloud)

*   Once indexing is completed, verify Jira issues are showing commits, branches, and pull requests as expected.

If you need additional support - contact [BigBrassBand Support](https://bigbrassband.atlassian.net/servicedesk/customer/portals/).