---

title: Pull Request timeline for Signals
description: Learn about pull request timeline reindexing and permission requirements for GitHub and GitLab integrations with Signals.
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This feature requires Git Integration for Jira to display pull request data in Signals.
    </div>
    </div>
</div>

The pull request timeline feature captures pull/merge request (PR/MR) event history and projects reindex data to Signals. Install Git Integration for Jira to see detailed information in tasks and Backlog View.

Currently supported git services: GitHub and GitLab.

&nbsp;

### Understanding permission errors

If you do not configure the required extended permissions, reindex errors occur. The git host generates logs that detail the error cause.

**Example GitHub error log:**

```json
{
  "locations":[{"line":1,"column":1615}],
  "type":"INSUFFICIENT_SCOPES",
  "message":"Your token has not been granted the required scopes to execute this query. The 'email' field requires one of the following scopes: ['user:email', 'read:user'], but your token has only been granted the: ['admin:org_hook', 'admin:public_key', 'admin:repo_hook', 'read:org', 'repo'] scopes. Please modify your token's scopes at: https://github.com/settings/tokens."
}
```

&nbsp;

### Configuring project access token permissions

Git administrators must set these minimum permission requirements in the organization or group settings.

&nbsp;

#### GitHub organization permissions

| Permission | Description |
|:-----------|:------------|
| admin:org ➜ **read:org** | Enable **read:org** under the **admin:org** scope. This grants permission to read organization and team membership along with organization projects. Required to read user information for organization types.<br><img src='/wp-content/uploads/tij-gitcloud-pull-req-timeline-reindex-github-org-setting.png' style='margin:15px auto 0px auto;max-width:100%;display:block;' /> |
| user ➜ **user:email** | Enable **user:email** under the **user** scope. This grants read-only access to user email addresses. Required to match users with Jira. |
| user ➜ **read:user** | Optional. Grants read access to all user profile data. |
| **read:discussion** | Optional. Grants read access to team discussions. |

&nbsp;

#### GitLab group permissions

| Permission | Description |
|:-----------|:------------|
| **Role** | Minimum: Reporter role. |
| **Scope** | Minimum: read_api scope. |

&nbsp;

### Setting GitHub App integration scopes

When configuring a GitHub App integration, set these required scopes:

*   **read:org** – Grants permission to read organization and team membership, and organization projects

*   **user:email** – Grants read-only access to user email addresses

&nbsp;

### More on Signals

[Signals](/git-integration-for-jira-cloud/Signals-gij-cloud)

[General View](/git-integration-for-jira-cloud/Signals-general-view-gij-cloud)

[Teams View](/git-integration-for-jira-cloud/Signals-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/Signals-backlog-view-gij-cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
