---

title: Deprecation notice (GIJ Cloud)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

| Feature | Date | Details of ending support, removal or obsolescence |
| :--- | :--- | :--- |
| **Personal access tokens** | Dependent on which Git service | Some Git services such as GitLab and GitHub are enforcing authentication access for users to use personal access tokens in accessing git resources and services. TFS 2017 and newer enforces PAT authentication. Old TFS servers such as 2013 and 2015 does not support PAT. |
| **`${username}`** | Effective 29 April 2019 | The `${username}` is used when logging into Jira and in the branch name template to generate a default name for newly-created branches. This template variable is deprecated as Atlassian is no longer making usernames available. |
| **Ignore unmatching webhooks** | 14 September 2021 | We will no longer reindex all repositories by default when a webhook arrives without a matching repository. |
| GitLab legacy | 06 June 2023 | Starting v4.19+<br>We will be dropping support for GitLab legacy integrations. |
| GitLab legacy integrations | End of March 2024 | GitLab legacy integrations will be deprecated in the Manage integrations screen. To prevent any integration issues:<br><ul><li>Please upgrade your GitLab server;</li><li>Remove legacy integrations; and</li><li>Connect a new GitLab integration to your GitLab CE/EE.</li><ul> |
| _(more to come)_ |     |     |