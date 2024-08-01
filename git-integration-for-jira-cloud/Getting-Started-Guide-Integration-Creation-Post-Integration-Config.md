---

title: Git Integration for Jira Cloud Getting Started Guide
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
# Integration Types
## Full Featured vs. Webhook Indexing

The two main integration types that will be utilized by the majority of our clients will be either a “Full Featured” or “Webhook Indexing” integration. Full featured integrations are active 2 way connections, while Webhook indexing integrations are one way passive connections.

The main determining factor when choosing between the two will be whether or not your company allows your code to be cloned, and if your Git Server is publicly reachable from the internet. 

It is important to note that when utilizing full featured integrations, in order to provide Code Compare and Code Diff functionality directly from Jira, our application does require us to clone your repositories. Your repositories will be cloned to our AWS storage, to a directory assigned specifically for your install. We encrypt all of your traffic/data in transit and at rest. You can review our Security and Trust page for an overview of how we secure your data. https://www.gitkraken.com/git-integration-for-jira/security-and-trust. 

Full Featured integrations are our recommended integration type for clients, as this will allow you to utilize our full feature set. If your git server is behind a firewall/proxy, you can still utilize this integration type, but you will have to do some whitelisting of our IP’s, and make sure that the URL for your git service is publicly routable: https://help.gitkraken.com/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud/

Webhook Indexing integrations are designed to accommodate clients with security restrictions surrounding Code cloning, or for clients that are utilizing self-hosted git servers that are behind firewalls/proxies and cannot make those servers routable from the public internet. Details about how Webhook Indexing integrations work can be found here: https://help.gitkraken.com/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud/. To summarize, this integration type has a limited feature set and relies on webhooks delivered from your git service with basic git data to update Jira Issue. 

The full feature matrix between the integration types can be found here:https://help.gitkraken.com/git-integration-for-jira-cloud/feature-matrix-of-git-integration-for-jira-cloud-gij-cloud/.


## Plain Git Connections
If you are not using one of the major Git services (Github,Gitlab,Azure DevOps,Bitbucket, AWS), we still have you covered! We support plain git connections, which are also feature limited. These integrations must be created to each individual repository. Please see the feature matrix linked above for details on the limitations on plain git connections.

# Indexing Behavior
Now that you have determined what kind of integration type will fit your needs best, we can go over how our application Indexes updates from your Repositories.

## First Time Indexing
 The initial indexing phase only happens the first time that an integration is added to GIJ, or a new repository is added to an existing integration. This initial indexing phase is comprised of 2 different actions that are performed on each repository included in each integration, or the new repository:
First, we will clone all of your repositories/ the newly created repository. Second, we will scan the entire git history for each repository searching for Jira issues. This allows us to link any git data that previously referenced Jira issues in the appropriate places in order to provide the most comprehensive historical git data in Jira possible. This initial indexing phase tends to take a lot longer than all of the subsequent indexes, as we are performing a lot more intensive operations during this phase. The time that this will take can vary wildly depending on the specifics of your repositories, but in general if your repositories contain a long git history, with a lot of branches and pull/merge requests, the longer this will take. The number of repositories included in the integration will also have an impact on this indexing time.

## Normal Indexing Operations
After all of your integrations/repositories have been indexed, by default the application will index everything periodically based on an adaptive timer. The frequency of how often specific repositories are indexed will vary based on a few different factors, such as how often there are changes detected in that repository, but most active repositories will be indexed every 20 minutes or so. The amount of time that it takes us to complete all of the indexing tasks will also affect the indexing frequency. For a more comprehensive explanation of our indexing process, please see Classic Indexing explainer: https://help.gitkraken.com/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud/

## Indexing Triggers
We suggest utilizing Indexing Triggers: https://help.gitkraken.com/git-integration-for-jira-cloud/indexing-triggers-gij-cloud/ alongside your integrations. These indexing triggers are webhooks that are created/sent from your repositories whenever there are updates to your repositories. When we receive the webhook, we will automatically index that repository outside of the normal indexing timer, allowing near real-time updates.

## Webhook Indexing
Despite the name, there is no actual indexing taking place when utilizing Webhook Indexing integrations. Since this is a one way passive integration, we do not clone/scan/index your repositories at any point. Instead, we rely on metadata included in the webhooks themselves to update the Jira Issues. With webhook indexing, we do not receive specific code change information, and do not have specific repository information. We add a record of any new repositories that we receive updates from. We will only update jira issues when we receive webhooks from your repositories containing Jira issue keys as part of the changes. There is no periodic or scheduled indexing. This means that all changes are updated in near real time by default.

# Integration structure planning

Now that you have a better understanding of what to expect with GIJ, how the application works, and what kind of security restrictions you need to take into consideration, we would suggest you take some time to plan out the best way to structure your integrations. There are a few more things to take into consideration when you are planning out your integrations. It is important to note that there are some soft performance limitations to consider when planning your integrations, so please review our known performance limitations page for some guidelines to follow when planning out your integrations: https://help.gitkraken.com/git-integration-for-jira-cloud/known-performance-limitations-gij-cloud/

1. Total Number of Repositories you wish to connect to Jira. The higher the number of repositories that will be included, the more challenging it can become to manage them, especially if you wish to utilize project associations. The larger the amount of repositories that are created, the more likely you are to run into rate limiting issues as well.
2. The structure of your repositories in your git services. Do you have your repositories organized by organization/groups in your git service, or is everything included in a single group/org? The more structured your repositories, the easier it becomes to create integrations.

Generally speaking, it is more preferable to create multiple integrations to the same git service, each connecting to a different org/group rather than one large integration containing all of your repositories. If you only have a small number of repositories, then this might not be necessary for your needs, but if you have a large number of repos and wish to limit visibility between Jira projects, then it will be easier to manage if they are broken up over multiple integrations.
Usually the best way to do this is to create an integration per Org/group, as long as the total number of repositories included in each integration is less than 2000. If a group/org has more than 2000 repos, then you will have to create multiple integrations to that same org/group in order to get the total number of repos to around 2000 or less. This can be done either by manually selecting the repositories in the UI, or by applying Custom API Path https://help.gitkraken.com/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud/ and/or JMESPath filtering https://help.gitkraken.com/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud/ .

Rate limiting can become an issue for large instances when there are a large number of repositories included, or some of the repositories have long and complex git histories with a lot of Branches and or Pull/Merge requests. If this is a concern for your instance, then the best way to address it will vary based on a few factors, but the general suggestion is to generate multiple service accounts on your git service, and spread out the authentication for your various integrations across the different accounts. Since the API calls will then be spread out across more accounts, and over a longer period of time, this should help avoid hitting your git services rate limits.




<br>

### Next - Application operations and Integration structure planning

[Initial setup guide](/git-integration-for-jira-cloud/

