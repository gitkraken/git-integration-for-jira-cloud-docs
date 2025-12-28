---

title: Git User Identity
description: How Git user identity is configured and displayed in Jira
taxonomy:
    category: git-integration-for-jira-cloud

---

A git user can identify themselves on their local computer using the following commands:

```bash
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

Or, for a specific repository:

```bash
$ git config user.name "John Doe"
$ git config user.email johndoe@example.com
```

Every commit is then associated with the configured user information.

Hosting services (like GitHub and Bitbucket, for example) try to match this data in commits with a particular account:

*   **If the email is unknown, the app displays the name from the commit.**
    If there is no Jira user associated with the email, Git Integration for Jira will use the author's name from the commit and display this name without any associated links.

    ![](/wp-content/uploads/gij-git-user-non-matching-email.png)

*   **If an email is configured in the local repository, the account is detected and displayed.**
    Git Integration for Jira uses the email from a commit and searches for a Jira user using this email. If a Jira user is found, the associated link to their Jira profile is displayed with the accompanying Jira avatar beside the name.

    ![](/wp-content/uploads/git-user-matching-email.png)

&nbsp;
* * *

[**Prev:** Viewing commit code diffs](/git-integration-for-jira-cloud/viewing-commit-code-diffs-gij-cloud)

[**Next:** Jira user information card](/git-integration-for-jira-cloud/jira-user-information-card-gij-cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
