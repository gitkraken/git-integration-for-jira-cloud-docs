---

title: How to Use JQL Searches for Builds and Deployments
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Jira Query Language (JQL) is a powerful and flexible way to search within Jira. With CI/CD for Jira you can now query on build and deployment information.

From the Jira search bar, select JQL on the far right to begin writing your query.

<img src='/wp-content/uploads/gij-cloud-cicd-jql-1.png' height=215 width=933 style='margin: 15px auto 25px auto; max-width: 100%' />

When you begin typing, Jira will offer some guidance on syntax:

<img src='/wp-content/uploads/gij-cloud-cicd-jql-2.png' height=162 width=229 style='margin: 15px auto 25px auto; max-width: 100%' />

### Deployments

| Function | Description |
| :--- | :--- |
| `deploymentEnvironmentName` | Name of your deployment environment |
| `deploymentEnvironmentType` | Type of environment |
| `deploymentState` | Current status of the deployment |
| `deploymentName` | Name of the specific deployment |

**Example syntax:**<br>
`deploymentEnvironmentType` ~ **Production**<br>
Shows all issues where the latest deployment is in the production environment

### Builds

| Function | Description |
| :--- | :--- |
| `buildState` | Status of a build |
| `buildName` | Name of a build |

**Example syntax:**<br>
`buildState` ~ successful<br>
Show all issues where the latest build was successful

