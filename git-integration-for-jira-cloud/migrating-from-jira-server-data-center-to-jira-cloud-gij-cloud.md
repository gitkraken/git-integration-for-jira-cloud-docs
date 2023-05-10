---

title: Migrating from Jira Server + Data Center to Jira Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

**What’s on this page:**
- [Let us assist you with your migration to Jira Cloud!](#let-us-assist-you)
- [Important Notes](#important-notes)
- [Links](#links)
- [Steps to migrate](#steps-to-migrate)

&nbsp;
* * *

<p id='let-us-assist-you'>&nbsp;</p>

## ![](/wp-content/uploads/gij-handshake-icon.png) Let us assist you with your migration to Jira Cloud!

Use this page as a resource to get all the information you need to start your migration. If you need additional support or one-on-one assistance, we'll be glad to help. Contact us at [BigBrassBand Support](https://link.bigbrassband.com/gij-gitkraken-gitcloud-support).

<p id='important-notes'>&nbsp;</p>

## ![](/wp-content/uploads/gij-notes-two.png) Important Notes

**Associations from Git data**<br>
Indexing Jira issues via commit messages is the same in Jira Server + Data Center as Jira Cloud. All the associations will be preserved.

**Manual commit associations**<br>
At this time, manual commit \<--\> Jira issue associations cannot be migrated automatically but request [**BigBrassBand Support**](https://link.bigbrassband.com/gij-gitkraken-gitcloud-support) for instructions on how to check.

**Self-hosted Git servers**<br>
When connecting a self-hosted git server to [**Git Integration for Jira Cloud**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) the git server must have a publicly addressable + route-able address. [GitHub.com](http://GitHub.com), [Azure DevOps](https://dev.azure.com), [GitLab.com](http://GitLab.com) and other services hosted on the “public cloud” work without any administrator interventions.

For more information, see: [**Allowlist (whitelist) BigBrassBand Cloud**](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud)

**Known Atlassian issue:** We highly recommend testing your Jira migration to the Cloud on a test Jira Cloud site. [AC-1528](https://ecosystem.atlassian.net/browse/AC-1528) is a bug in Atlassian Jira Cloud that breaks all Jira Cloud Atlassian Marketplace apps when a new project import is made. When migrating your users to Jira Cloud – we recommend installing and configuring the Git Integration for Jira Cloud app **after** all of your Jira users/projects/issues data is imported and verified.

## ![](/wp-content/uploads/gij-links-icon.png) Links

*   [Dual licensing](https://www.atlassian.com/migration/assess/calculate-pricing/dual-licensing)<br>To alleviate any concerns about paying for "double licensing" during your transition, please see the following article.

*   [Git Integration Server/Data Center vs Jira Cloud](/git-integration-for-jira-cloud/git-integration-server-data-center-vs-jira-cloud-feature-comparison-gij-cloud)<br>
Evaluating a move to Jira Cloud? Learn more about the similarities and differences.

*   [Atlassian Migration Program](https://www.atlassian.com/migration/cloud)<br>Leverage the Atlassian Migration Program for step-by-step migration resources, free tools, and dedicated support.

*   [Self-guided Server to Cloud migration guide](https://www.atlassian.com/migration/cloud/guide/introduction/overview)<br>Migrate to Cloud using Atlassian's step-by-step guide, tools and best practices.

*   [Enterprise migration guide](https://www.atlassian.com/migration/cloud/enterprise)<br>For teams migrating 1,000 users or more, Atlassian offers additional resources and support.

<p id='steps-to-migrate'>&nbsp;</p>

## ![](/wp-content/uploads/gij-pencil-icon.png) Steps to migrate

Currently there are not automatic steps to migrate from Jira Server + Data Center to Jira Cloud.


<ul style='list-style-type:none;'>
    <li style='line-height:180%;margin-bottom:12px;'>
      <input type="checkbox"> Create a <b>test</b> Jira Cloud instance. See below note.
    </li>
    <li style='line-height:180%;margin-bottom:12px;'>
      <input type="checkbox"> Install <a href='https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview'>Git Integration for Jira Cloud</a> on a test Jira Cloud instance.
    </li>
    <li style='line-height:180%;margin-bottom:12px;'>
      <input type="checkbox"> Verify self-hosted git servers have a a publicly addressable + rout-able address. For more information, see <a href='/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud'>Whitelist BigBrassBand Cloud</a>.
    </li>
    <li style='line-height:180%;margin-bottom:12px;'>
      <input type="checkbox"> Configure your git repositories via Git service integration or single, plain git repositories. For guides on connecting git servers + repositories to Jira Cloud, see <a href='/git-integration-for-jira-cloud/integration-guide-gij-cloud'>Integration Guide</a>.
      <ul style='list-style-type:none;margin-top:12px'>
        <li style='line-height:180%;margin-bottom:12px;'>
            <input type="checkbox"> Connect GitHub.com to Jira Cloud - see guide: <a href='/git-integration-for-jira-cloud/github-com-gij-cloud'>GitHub.com</a></li>
        <li style='line-height:180%;margin-bottom:12px;'>
            <input type="checkbox"> Connect GitHub Enterprise to Jira Cloud - see guide: <a href='/git-integration-for-jira-cloud/github-enterprise-server-gij-cloud'>GitHub Enterprise</a></li>
        <li style='line-height:180%;margin-bottom:12px;'>
            <input type="checkbox"> Connect GitLab.com to Jira Cloud - see guide: <a href='/git-integration-for-jira-cloud/gitlab-com-gij-cloud'>GitLab.com</a></li>
        <li style='line-height:180%;margin-bottom:12px;'>
            <input type="checkbox"> Connect GitLab CE/EE to Jira Cloud - see guide: <a href='/git-integration-for-jira-cloud/gitlab-ce-ee-gij-cloud'>GitLab CE/EE</a></li>
        <li style='margin-bottom:10px'>
            <input type="checkbox"> Connect AWS CodeCommit to Jira Cloud - see guide: <a href='/git-integration-for-jira-cloud/aws-codecommit-gij-cloud'>AWS CodeCommit</a></li>
        <li style='line-height:180%;margin-bottom:12px;'>
            <input type="checkbox"> Connect Bitbucket Cloud to Jira Cloud - see guide: <a href='/git-integration-for-jira-cloud/bitbucket-cloud-gij-cloud/'>Bitbucket Cloud</a></li>
        <li style='line-height:180%;margin-bottom:12px;'>
            <input type="checkbox"> Connect Microsoft Azure DevOps (Cloud) to Jira Cloud - see guide: <a href='/git-integration-for-jira-cloud/azure-devops-visual-studio-team-services-vsts-gij-cloud'>Azure DevOps | Visual Studio Team Services (VSTS)</a></li>
        <li style='line-height:180%;margin-bottom:12px;'>
            <input type="checkbox"> Connect Microsoft Azure DevOps Server to Jira Cloud - see guide: <a href='/git-integration-for-jira-cloud/azure-devops-server-team-foundation-services-tfs-gij-cloud'>Azure DevOps Server | Team Foundation Services (TFS)</a></li>
        <li style='line-height:180%;margin-bottom:12px;'>
            <input type="checkbox"> Connect Gerrit to Jira Cloud - see guide: <a href='/git-integration-for-jira-cloud/gerrit-gij-cloud'>Gerrit</a></li>
      </ul>
    </li>
    <li style='line-height:180%;margin-bottom:12px;'>
      <input type="checkbox"> Once indexing is completed, verify Jira issues are showing commits, branches, and pull requests as expected.
    </li>
</ul>

&nbsp;

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If you need additional support - contact <a href='https://link.bigbrassband.com/gij-gitkraken-gitcloud-support'>GIJ Cloud Support</a>.
    </div>
    </div>
</div>

&nbsp;

