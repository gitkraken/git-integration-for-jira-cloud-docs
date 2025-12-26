---

title: Application Operations and Planning
description: Understanding integration types, indexing behavior, and planning your Git Integration for Jira structure
taxonomy:
    category: git-integration-for-jira-cloud

---

## Integration Types

### Full Featured vs Webhook Indexing

Most users choose either Full Featured or Webhook Indexing integrations. Full Featured integrations create active two-way connections, while Webhook Indexing integrations create one-way passive connections.

Consider these factors when choosing:

1. Your company policy regarding code cloning
2. Whether your Git server is private or public

**Full Featured integrations** are recommended for most users because they provide access to all features. If your Git server is behind a firewall or proxy, you can still use this integration type by allowlisting our IPs and ensuring your Git service URL is publicly routable. See [Allowlist - GIJ Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud/) for details.

Full Featured integrations require GIJ to clone your repositories to provide Code Compare and Code Diff functionality directly from Jira. Repositories are cloned to AWS storage in a directory assigned specifically to your installation. All traffic and data is encrypted in transit and at rest. Visit our [Security and Trust](https://www.gitkraken.com/git-integration-for-jira/security-and-trust) page for an overview of security measures.

**Webhook Indexing integrations** accommodate users with security restrictions around code cloning, or users with self-hosted Git servers behind firewalls that cannot be made publicly routable. See the [Webhook Indexing Explainer](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud/) for details on how this works. This integration type has a limited feature set because it relies on webhook metadata rather than direct repository access.

See our [Feature Matrix](/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud/) for a detailed breakdown of features by integration type.

### Plain Git Connections

If you don't use a major Git service (GitHub, GitLab, Azure DevOps, Bitbucket, AWS), GIJ supports plain Git connections to individual repositories. See the Feature Matrix linked above for details on plain Git connection limitations.

&nbsp;

## Indexing Behavior

Now that you understand integration types, let's examine how Git Integration for Jira indexes updates from your repositories.

### Full Featured Integrations

Full Featured integrations go through two stages of indexing: initial indexing (happens once) and normal indexing.

### First Time Indexing

Initial indexing occurs only when you first add an integration to GIJ or add a new repository to an existing integration. This phase includes two actions:

1. Clone all repositories (or the newly created repository)
2. Scan the entire Git history for each repository, searching for Jira issue references

This scan links any Git data that previously referenced Jira issues, providing comprehensive historical Git data in Jira. Because these operations are more intensive, initial indexing takes longer than subsequent indexes. Total index time varies based on repository Git history length, number of branches and pull/merge requests, and number of repositories in the integration.

### Normal Indexing Operations

After initial indexing completes, the application automatically indexes your Git repositories periodically based on an adaptive timer. Index frequency varies based on how often changes are detected in each repository, but most active repositories index every 20 minutes or so. The time required to complete all indexing tasks also affects frequency.

For a comprehensive explanation of the indexing process, see [Classic Indexing Explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud/).

### Indexing Triggers

We recommend using [Indexing Triggers](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud/) alongside your integrations. These triggers are webhooks sent from your repositories whenever updates occur. When GIJ receives the webhook, it automatically indexes that repository outside the normal timer, enabling near real-time updates.

### Webhook Indexing

Despite the name, Webhook Indexing integrations don't actually index repositories. Since this is a one-way passive integration, GIJ never clones, scans, or indexes your repositories. Instead, it relies on metadata in the webhooks to update Jira issues.

With Webhook Indexing:

- No specific code change information is sent
- No repository information is sent
- Repository records are added after webhooks are received

GIJ only updates Jira issues when it receives webhooks containing Jira issue keys. There is no periodic or scheduled indexing, so all changes update in near real time by default.

&nbsp;

## Integration Structure Planning

Now that you understand what to expect with GIJ, take time to evaluate how to structure your integrations:

1. **Total number of repositories** you want to connect to Jira
    - More connected repositories make management more challenging, especially when using project associations
    - More repository connections increase the likelihood of rate limiting issues

2. **Repository structure** in your Git services
    - Are repositories organized by organization/group, or is everything in a single group/org?
    - More structured repositories make integration creation easier

Consider creating multiple integrations to the same Git service, each connecting to a different org/group, instead of one large integration containing all repositories. If you have fewer than 100 repositories, this may not be necessary. If you have more than 100 and want to limit visibility between Jira projects, breaking them into multiple integrations makes management easier.

The best approach is usually to create one integration per org/group, keeping each integration under 2,000 repositories. If a group/org has more than 2,000 repositories, create multiple integrations to that same org/group to keep each under 2,000 repositories. You can do this by manually selecting repositories in the UI or by applying [Custom API Path](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud/) and/or [JMESPath Filtering](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud/).

Rate limiting can become an issue for large instances with many repositories or repositories with long, complex Git histories with many branches and pull/merge requests. To address this, generate multiple service accounts on your Git service and spread authentication across different accounts. This distributes API calls across more accounts and over longer periods, helping avoid rate limits.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Review our <a href='/git-integration-for-jira-cloud/known-performance-limitations-gij-cloud/'>Known Performance Limitations</a> page for soft performance limitations to consider when planning your integrations.
    </div>
    </div>
</div>

&nbsp;

---

[<b style='background-color:#FFFCC3; padding:1px 5px; color:#181D28; border-radius:3px; margin: 0 5px; font-size: medium;'>NEXT</b>](/git-integration-for-jira-cloud/Getting-Started-Guide-Integration-Creation-Post-Integration-Config) <a href="https://help.gitkraken.com/git-integration-for-jira-cloud/Getting-Started-Guide-Integration-Creation-Post-Integration-Config/">Integration Creation and Post Integration Config</a>

[<b style='background-color:#F1F1F1; padding:1px 5px; color:#181D28; border-radius:3px; margin: 0 5px; font-size: medium;'>PREVIOUS</b>](/git-integration-for-jira-cloud/Getting-Started-Guide/) <a href="https://help.gitkraken.com/git-integration-for-jira-cloud/Getting-Started-Guide/">Getting Started</a>

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
