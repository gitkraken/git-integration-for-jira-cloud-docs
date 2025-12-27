---

title: CI/CD for Jira Cloud
description: Learn how to use CI/CD for Jira Cloud to connect your DevOps pipelines with Jira's builds and deployments features.
taxonomy:
    category: git-integration-for-jira-cloud

---

[CI/CD for Jira](https://marketplace.atlassian.com/apps/1228578/ci-cd-for-jira?hosting=cloud&tab=overview) is a free extension to Git Integration for Jira, connecting your CI/CD DevOps pipelines with Jira Cloud's builds and deployments features. Similar to how Git Integration for Jira exposes commits, branches, and pull requests, CI/CD for Jira adds in build and deployment information associated with Jira issues.

CI/CD for Jira tracks builds/deployments by Pull Requests, and supports classic pipelines, and YAML pipelines only for builds. If you are running your deployments via the build YAML pipeline, the deployments are not displayed.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>On this page:</b><br>
        <ul style='margin-bottom:0px;'>
            <li><a href='#supported-services'>Supported services</a></li>
            <li><a href='#setup'>Setup</a></li>
            <li><a href='#associating-issues'>Associating issues</a></li>
            <li><a href='#does-this-extension-support-sending-builddeployment-information-via-webhook'>Does this extension support sending build/deployment information via webhook?</a></li>
            <li><a href='#viewing-builds-and-deployments-in-a-jira-issue'>Viewing builds and deployments in a Jira issue</a></li>
            <li><a href='#how-to-enable-deployment-view-in-jira'>How to enable Deployment View in Jira</a></li>
            <li><a href='#how-to-use-jql-searches-for-builds-and-deployments'>How to use JQL searches for builds and deployments</a></li>
            <li><a href='#how-to-trigger-automation-for-jira-with-builds-and-deployments'>How to trigger Automation for Jira with builds and deployments</a></li>
        </ul>
    </div>
    </div>
</div>

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

* * *

&nbsp;

## Viewing builds and deployments in a Jira issue

When an issue is associated with a build or deployment, additional information will be available in the right hand panel.

<img src='/wp-content/uploads/gij-cloud-cicd-Issuepanel-1-2025.png' height=588 width=514 style='margin: 15px auto 25px auto; max-width: 100%' />

Builds and Deployments will show as successful or failed based on the icon to the right (<img src='/wp-content/uploads/bbb-tips-20.png' style='' /> green checkmark). Clicking on a build or a release will pop up a new window with a link out to the pipeline for more information.

For pipeline errors, wherein a step within your pipeline has failed, there are several external factors that is causing it to fail. For example:

*   a misconfiguration in your deployment too
*   an incorrectly set environment variable

If a pipeline fails, you have the option to rerun the whole pipeline, or any failed steps. For more information, see Atlassian docs on [How to view your pipeline](https://support.atlassian.com/bitbucket-cloud/docs/view-your-pipeline/#Viewyourpipeline-CI_RerunStep).

<img src='/wp-content/uploads/gij-cloud-cicd-Issuepanel-2-2025.png' height=215 width=933 style='margin: 15px auto 25px auto; max-width: 100%' />

Clicking on **Open Git Integration** will open a view that rolls up all commits by file and developer, and reports change statistics. From here you can click individual commits, builds, and deployments to see more information.

<img src='/wp-content/uploads/gij-cloud-cicd-Issuepanel-3-2025.png' height=726 width=519 style='margin: 15px auto 25px auto; max-width: 100%' />

&nbsp;

* * *

&nbsp;

## How to enable Deployment View in Jira

Jira includes a timeline that shows deployments across environments. You can search deployments by issues, environments, types and more.

<img src='/wp-content/uploads/gij-cloud-cicd-deployments-view-1.png' height=226 width=428 style='margin: 15px auto 25px auto; max-width: 100%' />

By default this feature is turned off, and must be turned on.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        You must be a project admin to enable and disable features on a project. You must also have the <b>View Development Tools</b> permission to enable the Deployments feature.
    </div>
    </div>
</div>
<br>

1.  Navigate to your project.

2.  Go to Project settings ➜ **Features**.

    <img src='/wp-content/uploads/gij-cloud-cicd-deployments-view-2.png' height=204 width=227 style='margin: 15px auto 25px auto; max-width: 100%' />

3.  Enable the Deployments feature.

    <img src='/wp-content/uploads/gij-cloud-cicd-deployments-view-3.png' height=196 width=956 style='margin: 15px auto 25px auto; max-width: 100%' />

A new menu item, Deployments, will be added to the left-hand project menu (under Operations).

More information on using the deployments view, visit [Atlassian Docs - Enable deployments](https://support.atlassian.com/jira-software-cloud/docs/enable-deployments/)

&nbsp;

* * *

&nbsp;

## How to use JQL searches for builds and deployments

Jira Query Language (JQL) is a powerful and flexible way to search within Jira. With CI/CD for Jira you can now query on build and deployment information.

From the Jira search bar, select JQL on the far right to begin writing your query.

<img src='/wp-content/uploads/gij-cloud-cicd-jql-1.png' height=215 width=933 style='margin: 15px auto 25px auto; max-width: 100%' />

When you begin typing, Jira will offer some guidance on syntax:

<img src='/wp-content/uploads/gij-cloud-cicd-jql-2.png' height=162 width=229 style='margin: 15px auto 25px auto; max-width: 100%' />

### Deployments JQL functions

| Function | Description |
| :--- | :--- |
| `deploymentEnvironmentName` | Name of your deployment environment |
| `deploymentEnvironmentType` | Type of environment |
| `deploymentState` | Current status of the deployment |
| `deploymentName` | Name of the specific deployment |

**Example syntax:**<br>
`deploymentEnvironmentType` ~ **Production**<br>
Shows all issues where the latest deployment is in the production environment

### Builds JQL functions

| Function | Description |
| :--- | :--- |
| `buildState` | Status of a build |
| `buildName` | Name of a build |

**Example syntax:**<br>
`buildState` ~ successful<br>
Show all issues where the latest build was successful

&nbsp;

* * *

&nbsp;

## How to trigger Automation for Jira with builds and deployments

Jira automation allows teams to control processes and workflows using rules to automate actions within Jira. Automation rules have 3 parts:

*   **Triggers** – Listens for events and starts the execution of a rule when a set condition is met.

*   **Conditions** – Set the scope of a rule with specific events tailored for your team.

*   **Actions** – Set automated tasks to perform when a condition is met.

Git Integration for Jira supports triggers for branches, commits, and pull requests. Adding the CI/CD for Jira extension enables the use of additional triggers:

*   Build status changed, failed, and successful

*   Deployment status changed, failed, and successful.

<img src='/wp-content/uploads/gij-cloud-cicd-a4j-1.png' height=574 width=562 style='margin: 15px auto 25px auto; max-width: 100%' />


To create new rules, go to Project settings ➜ Automation ➜ **Create Rule**. For more information on setting up Automation for Jira rules, visit the [Git Integration + Jira Automation](/git-integration-for-jira-cloud/git-integration-jira-automation-gij-cloud/) article.

<kbd>Last updated: December 2025</kbd>

