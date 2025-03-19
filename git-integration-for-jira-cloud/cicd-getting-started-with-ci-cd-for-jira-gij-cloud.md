---

title: Getting Started with CI/CD for Jira
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

[CI/CD for Jira](https://marketplace.atlassian.com/apps/1228578/ci-cd-for-jira?hosting=cloud&tab=overview) is a free extension to Git Integration for Jira, connecting your CI/CD DevOps pipelines with Jira Cloud’s builds and deployments features. Similar to how Git Integration for Jira exposes commits, branches, and pull requests, CI/CD for Jira adds in build and deployment information associated with Jira issues.

CI/CD for Jira tracks builds/deployments by Pull Requests, and supports classic pipelines, and YAML pipelines only for builds. If you are running your deployments via the build YAML pipeline, the deployments are not displayed.

&nbsp;

## Supported services

[CI/CD for Jira](https://marketplace.atlassian.com/apps/1228578/ci-cd-for-jira?hosting=cloud&tab=overview) currently supports the following tools for Build and Deployment information:

*   GitHub Actions (Cloud or Self Hosted)
*   GitLab CI/CD (Cloud or Self Hosted)
*   Azure DevOps Pipelines (Cloud or Self Hosted)
*   Bitbucket Pipelines (Cloud)

&nbsp;

## Setup

After adding the CI/CD for Jira extension from the Atlassian Marketplace, there are no additional steps needed to start seeing build and deployment information in Jira. Just ensure your previously connected repositories have been reindexed.

&nbsp;

## Associating issues

A build is automatically linked to a Jira issue if one of the build's commits includes the Jira issue key in its commit message. A deployment to an environment, such as production or testing, is linked if a commit that is associated with the deployment contains the Jira issue key in its commit message.

&nbsp;

## Does this extension support sending build/deployment information via webhook?

CI/CD for Jira Cloud does not currently support sending build/deployment information via webhook event. Furthermore, if you are using webhook indexing, CI/CD information is not supported. 

CI/CD indexing only happens during regular scheduled indexes, and cannot be triggered via indexing triggers. This can vary a little bit based on what service is being used and the way that the pipelines are configured.

&nbsp;

## Where to view builds and deployments

Within Jira, build and deployment information can be found in several locations:

*   [In the Development, Releases, and Git Integration sections within issue Details](/git-integration-for-jira-cloud/cicd-viewing-builds-and-deployments-in-a-jira-issue-gij-cloud/)

*   [In the Deployments feature under Operations](/git-integration-for-jira-cloud/cicd-how-to-enable-deployment-view-in-jira-gij-cloud/) (must be enabled)

*   [Within JQL searches](/git-integration-for-jira-cloud/cicd-how-to-use-jql-searches-for-builds-and-deployments-gij-cloud/)

*   [As Automation for Jira triggers](/git-integration-for-jira-cloud/cicd-how-to-trigger-a4j-with-builds-and-deployments-gij-cloud/)

