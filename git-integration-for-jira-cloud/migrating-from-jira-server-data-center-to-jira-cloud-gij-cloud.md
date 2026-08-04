---
title: "Migrating from Jira Data Center to Jira Cloud"
description: "Step-by-step guide for migrating Git Integration for Jira Data Center to Jira Cloud using the Jira Cloud Migration Assistant (JCMA)"
product: "Git Integration for Jira Cloud"
feature: "Migrating from Jira Data Center to Jira Cloud"
content_type: "integration"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: ["GitHub Cloud", "GitHub self-hosted", "GitLab Cloud", "GitLab self-hosted", "Azure DevOps Cloud", "Azure DevOps self-hosted"]
role_required: "Jira Administrator"
version_required: "4.29.5, 5.5.3, 6.1.3"
status: "GA"
last_verified: "2026-08"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "integration", "admin", "migration", "JCMA"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: August 2026</kbd>

**What’s on this page:**
- [Let us assist you with your migration to Jira Cloud!](#let-us-assist-you)
- [Important Notes](#important-notes)
- [Migrating through the Jira Cloud Migration Assistant (JCMA)](#migrating-through-the-jcma)
- [Manual steps to migrate](#manual-steps-to-migrate)
- [Links](#links)

&nbsp;
* * *

<p id='let-us-assist-you'>&nbsp;</p>

## ![](/wp-content/uploads/gij-handshake-icon.png) Let us assist you with your migration to Jira Cloud!

Use this page as a resource to get all the information you need to start your migration. If you need additional support or one-on-one assistance, we'll be glad to help. Contact us at [GIJ Cloud Support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support).

<p id='important-notes'>&nbsp;</p>

## ![](/wp-content/uploads/gij-notes-two.png) Important Notes

**Associations from Git data**<br>
Indexing Jira issues via commit messages is the same in Jira Data Center and Jira Cloud. All the associations will be preserved.

**Self-hosted Git servers**<br>
When connecting a self-hosted git server to [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) the git server must have a publicly addressable and routable address. [GitHub.com](http://GitHub.com), [Azure DevOps](https://dev.azure.com), [GitLab.com](http://GitLab.com) and other services hosted on the “public cloud” work without any administrator intervention.

For more information, see: [**Allowlist (whitelist) GIJ Cloud**](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud)

<p id='migrating-through-the-jcma'>&nbsp;</p>

## Migrating through the Jira Cloud Migration Assistant (JCMA)

- <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT</b> Minimum required versions based on your Jira version:
    
    * Jira 9: v4.29.5

    * Jira 10: v5.5.3

    * Jira 11: v6.1.3

1. In Jira Data Center, go to System > Migrate to Cloud.

2. In the Migration Dashboard, create a new migration and verify all the required steps. For more information on migrations, review the [**Atlassian's migration guide**](https://www.atlassian.com/migration/plan/cloud-guide#introduction).

3. When you get to the "Assess your Apps" section, for the Git Integration for Jira app, make sure the Decision column is set to "Needed in Cloud" and click on Done.

![](/wp-content/uploads/gij-mig-needed-in-cloud.png)

4. In the "Prepare your Apps" section, click on "View Policy", confirm, and click on Done.

![](/wp-content/uploads/gij-mig-view-policy.png)
![](/wp-content/uploads/gij-mig-policy-agree.png)

5. In the "Connect to your cloud site" section, choose the name, migration stage, cloud destination site and migration options. We recommend you first test the migration in a cloud test instance.

![](/wp-content/uploads/gij-mig-connect-cloud.png)

6. Select what data you will migrate. Make sure the Git Integration for Jira is selected in the apps section.

7. In the "Pre-migration checks" section, review all possible errors. All checks should be green. Ignore the warning: "Some apps selected for this migration have low or unknown migration success rates" if Git Integration is the only application listed. Then click **Review Migration**.

![](/wp-content/uploads/gij-mig-ignore-warning.png)

8. Review the migration. Ignore the warning for Git Integration for Jira and click on Run.

![](/wp-content/uploads/gij-mig-ignore-warning-2.png)

9. The migration will take place. The duration will depend on the number of elements being migrated.

![](/wp-content/uploads/gij-mig-complete-summary.png)

10. After the migration completes, you can go to the Manage Integrations screen and you will see the migrated integrations. Jira will show a yellow banner indicating that a synchronization of elements is taking place in the background.

![](/wp-content/uploads/gij-mig-after.png)

<p id='manual-steps-to-migrate'>&nbsp;</p>

## ![](/wp-content/uploads/gij-pencil-icon.png) Manual steps to migrate

The Jira Cloud Migration Assistant (JCMA) will move all your integrations and manual commits. There is no need to migrate things manually, but if you prefer that route, simply recreate the integrations in the Cloud site. After indexing, all the links will be re-established.

<p id='links'>&nbsp;</p>

## ![](/wp-content/uploads/gij-links-icon.png) Links

*   [Dual licensing](https://www.atlassian.com/migration/assess/calculate-pricing/dual-licensing)<br>To alleviate any concerns about paying for "double licensing" during your transition, please see the following article.

*   [Git Integration Server/Data Center vs Jira Cloud](/git-integration-for-jira-cloud/git-integration-server-data-center-vs-jira-cloud-feature-comparison-gij-cloud)<br>
Evaluating a move to Jira Cloud? Learn more about the similarities and differences.

*   [Official Jira Cloud Migration guide.](https://www.atlassian.com/migration/plan/cloud-guide#introduction)<br>
All the official Jira Cloud migration resources.


&nbsp;

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If you need additional support - contact <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>GIJ Cloud Support</a>.
    </div>
    </div>
</div>

&nbsp;

<br>
