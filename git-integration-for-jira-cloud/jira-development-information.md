---

title: Jira Development Information
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The **View Development Tools** _permission_ only applies to Jira _**Company-managed**_ projects. _**Team-managed**_ projects don't allow to modify the permission.

Only newly added commits, branches and pull requests will be uploaded to Jira Cloud when enabling the [Send Development Information to Jira Cloud](/wiki/spaces/GITCLOUD/pages/1941373145) setting. If you wish to upload the entire history of an integration or repository - remove the integration/repository and then add the integration/repository back.

## What is Jira Development Information?

Jira Development Information is a suite of new features available in Jira Software on the Cloud platform that puts commits, branches, and pull requests in context of Jira issue.

*   By default, [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) has Jira Development Information disabled. ([How to enable?](/wiki/spaces/GITCLOUD/pages/1941373145))

*   By default, [**Dev Info for Jira**](https://marketplace.atlassian.com/1219270) has Jira Development Information enabled. ([How to disable?](/wiki/spaces/GITCLOUD/pages/1941373145))


## How does Jira Development Information work?

The [**Git Integration for Jira**](https://marketplace.atlassian.com/4984) and [**Dev Info for Jira**](https://marketplace.atlassian.com/1219270) apps can be configured to "push" development information (commits, branches, and pull requests) directly into your Jira Cloud instance. Once the data is stored by Jira Cloud - the commits, branches, and pull requests can be displayed by Atlassian in a variety of locations within Jira Cloud. This data additionally enables a new of [new features](#What-other-features-are-enabled-by-Jira-Development-Information%3).

## Who can see Jira Development Information?

*   Jira users with the View development tools Jira permission for a given Jira project can. 

*   Jira administrators can verify a user's permissions using the [**Permission Helper**](https://confluence.atlassian.com/adminjiracloud/jira-admin-helper-818578850.html).


The **View developer tools** _permission_ is required to view the Jira Development Information. Jira users must also have the **Browse Project** _permissions_ to a project associated with a repository to view.

Note that the **Project Permissions** feature in the [**Git Integration for Jira**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud) and [**Dev Info for Jira**](https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview) app does not apply to Jira Development Information. All users with **View Development Tools** permission can access Jira Development Information.

## What other features are enabled by Jira Development Information?

*   [JQL searching for commits and pull requests](/wiki/spaces/GITCLOUD/pages/643596299/JQL+Searching+for+Commits+and+Pull+Requests)

*   [Development status in Jira Issue Searching](/wiki/spaces/GITCLOUD/pages/1940914287/Development+status+in+Jira+issue+searching)

*   [Release Hub](/wiki/spaces/GITCLOUD/pages/1941373081)

*   [Automatic Workflow Triggers](/wiki/spaces/GITCLOUD/pages/1940783182/Automatic+Workflow+Triggers)

*   [NextGen projects only: View commits, branches, and pull requests in Jira Boards](/wiki/spaces/GITCLOUD/pages/1940783272/Next-gen+projects+only%3A+View+commits%2C+branches%2C+and+pull+requests+in+Jira+Boards)


## More related features about Jira development information

*   Page:

    [How can a Jira administrator enable or disable Jira Development Information?](/wiki/spaces/GITCLOUD/pages/1941373145) (Git Integration for Jira Cloud)

*   Page:

    [Jira Development Information settings](/wiki/spaces/GITCLOUD/pages/1941373113/Jira+Development+Information+settings) (Git Integration for Jira Cloud)

*   Page:

    [Development Information Views](/wiki/spaces/GITCLOUD/pages/643203115/Development+Information+Views) (Git Integration for Jira Cloud)

*   Page:

    [JQL Searching for Commits and Pull Requests](/wiki/spaces/GITCLOUD/pages/643596299/JQL+Searching+for+Commits+and+Pull+Requests) (Git Integration for Jira Cloud)

*   Page:

    [Jira Cloud Smart Commits and Workflow Triggers](/wiki/spaces/GITCLOUD/pages/144310383/Jira+Cloud+Smart+Commits+and+Workflow+Triggers) (Git Integration for Jira Cloud)


**Contact Us**
If you still have a question - reach out to our [**Support Desk**](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).