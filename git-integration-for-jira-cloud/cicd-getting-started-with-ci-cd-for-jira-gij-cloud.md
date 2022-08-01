---

title: Getting Started with CI/CD for Jira
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

CI/CD for Jira is a free extension to Git Integration for Jira, connecting your CI/CD DevOps pipelines with Jira Cloud’s builds and deployments features. Similar to how Git Integration for Jira exposes commits, branches, and pull requests, CI/CD for Jira adds in build and deployment information associated with Jira issues.

## Supported services

CI/CD for Jira currently supports the following tools for Build and Deployment information:

*   GitHub Actions (Cloud or Self Hosted)
*   GitLab CI/CD (Cloud or Self Hosted)
*   Azure DevOps Pipelines (Cloud or Self Hosted)
*   Bitbucket Pipelines (Cloud)

## Setup

After adding the CI/CD for Jira extension from the Atlassian Marketplace, there are no additional steps needed to start seeing build and deployment information in Jira. Just ensure your previously connected repositories have been reindexed.

## Associating issues

A build is automatically linked to an issue if one of the build's commits includes the issue key in its commit message. A deployment to an environment, such as production or testing, is linked if a commit associated with the deploy contains the issue key in its commit message.

## Where to view builds and deployments
Within Jira, build and deployment information can be found in several locations:

*   In the Development, Releases, and Git Integration sections within issue Details

*   In the Deployments feature under Operations (must be enabled)

*   Within JQL searches

*   As Automation for Jira triggers

