---

title: Using Smart Commits
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<!-- INTRODUCTION TO GIT INTEGRATION -->

Smart Commits enable users to perform actions on Jira issues from a single commit. In a commit message, enter the issue key and some desired action such as resolving an issue, closing an issue, time tracking or all of them.

<img src='/wp-content/uploads/gij-gitcloud-smart-commit-example.png' style='display:block;margin:25px auto;max-width:100%' />

<p align=center style='margin-bottom:35px'><i>Above image example transitions the Jira issue to <b>IN PROGRESS</b>, adds <br>the comment "Refactor code" to the <b>Comments</b> tab and logs <br></b>1d 12h 30m</b> as the total time worked on the task.</i></p>

For example, if a user wants to log specified time with worklog comment, adds a comment, and resolve the issue TEST-100, enter the commit message as follows:

<img src='/wp-content/uploads/gij-gitcloud-using-smart-commits-sample-msg.png' style='display:block;margin:25px auto;max-width:100%' />

Enable/disable this feature via:

*   **Integration level** -- Manage integrations page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ Edit integration ➜ **Feature Settings** ➜ Smart Commits

*   **Repository level** -- Manage repositories page ➜ ![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit repository**  ➜ Smart Commits

*   **Application-settings** -- General settings (sidebar) ➜  **Jira Development Information**


See our [Smart Commits Overview](/git-integration-for-jira-cloud/smart-commits-overview-gij-cloud) to learn further about syntax and structure; then follow the link at the bottom of that page to learn more information on advanced syntax.

&nbsp;
* * *

[**Prev:** Link git commits to Jira issue](/git-integration-for-jira-cloud/link-git-commits-to-jira-issue-gij-cloud/)

[**Next:** Using the Repository Browser](/git-integration-for-jira-cloud/using-the-repository-browser-gij-cloud/)

