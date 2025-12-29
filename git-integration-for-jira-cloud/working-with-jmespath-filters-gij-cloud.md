---
title: Working with JMESPath Filters
description: Learn how to use JMESPath query language to filter API results and control which repositories are integrated with Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

JMESPath is a query language for JSON. Use JMESPath filters to control which repositories Git Integration for Jira connects to your Jira instance.

For help writing expressions, contact [support](mailto:gijsupport@gitkraken.com) or submit a request through the [Support portal](/git-integration-for-jira-cloud/gij-cloud-contact-support/).

Learn more about JMESPath expressions on the [JMESPath website](http://jmespath.org/).

**On this page:**
- [Access JMESPath filter settings](#access-jmespath-filter-settings)
- [Supported git services](#supported-git-services)

&nbsp;
* * *
&nbsp;

## Access JMESPath Filter Settings

Configure JMESPath filters from two locations:

### During Integration Setup

1. Go to **Add integration** ➜ select a supported git service.
2. On the **Connection** screen, expand **Advanced**.
3. Enter your filter in the **JMESPath filter** field.

![](/wp-content/uploads/gij-cloud-connect-github-example-advanced-jmespath-2025.png)

This option is available for supported git services on the Full feature integrations panel.

### From Integration Settings

1. Go to **Manage Git repositories**.
2. Click ![](/wp-content/uploads/actions-icon.png) **Actions** ➜ **Edit integration settings**.
3. Scroll to **Integration settings** ➜ **JMESPath Filter**.
4. Enter or modify your filter.

![](/wp-content/uploads/gij-gitcloud-jmespath-actions-settings-2025.png)

This option is available for supported git services on repository or integration connections.

&nbsp;

## Supported Git Services

JMESPath filters work with these git services:

- [GitHub.com | GitHub Enterprise JMESPath filter examples](/git-integration-for-jira-cloud/github-com-github-enterprise-jmespath-filter-examples-gij-cloud)
- [GitLab.com | GitLab CE/EE JMESPath filter examples](/git-integration-for-jira-cloud/gitlab-com-gitlab-ce-ee-jmespath-filter-examples-gij-cloud)
- [Microsoft | VSTS | TFS | Azure Repos JMESPath filter examples](/git-integration-for-jira-cloud/microsoft-vsts-tfs-azure-repos-jmespath-filter-examples-gij-cloud)
- [Bitbucket JMESPath filter examples](/git-integration-for-jira-cloud/bitbucket-jmespath-filter-examples-gij-cloud)

<kbd>Last updated: December 2025</kbd>
