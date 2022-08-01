---

title: How to trigger Automation for Jira with Builds and Deployments
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Jira automation allows teams to control processes and workflows using rules to automate actions within Jira. Automation rules have 3 parts:

*   **Triggers** – Listens for events and starts the execution of a rule when a set condition is met.

*   **Conditions** – Set the scope of a rule with specific events tailored for your team.

*   **Actions** – Set automated tasks to perform when a condition is met.

Git Integration for Jira supports triggers for branches, commits, and pull requests. Adding the CI/CD for Jira extension enables the use of additional triggers:

*   Build status changed, failed, and successful

*   Deployment status changed, failed, and successful.

<img src='/wp-content/uploads/gij-cloud-cicd-a4j-1.png' height=574 width=562 style='margin: 15px auto 25px auto; max-width: 100%' />


To create new rules, go to Project settings ➜ Automation ➜ **Create Rule**. For more information on setting up Automation for Jira rules, visit the [A4J help article](/git-integration-for-jira-cloud/git-integration-jira-automation-gij-cloud/).

