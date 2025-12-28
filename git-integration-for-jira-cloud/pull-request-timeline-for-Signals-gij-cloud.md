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

This feature supports pull/merge request (PR/MR) event history and projects PR/MR reindex data to Signals. Install Git Integration for Jira to see detailed information in tasks and backlog view.

Currently supported git services: GitHub and GitLab.

&nbsp;

### What happens if these extended permissions are not set?

Reindex errors will occur. The git host generates logs detailing the error cause.

Example GitHub generated error log:

```json
{
  "locations":[{"line":1,"column":1615}],
  "type":"INSUFFICIENT_SCOPES",
  "message":"Your token has not been granted the required scopes to execute this query. The 'email' field requires one of the following scopes: ['user:email', 'read:user'], but your token has only been granted the: ['admin:org_hook', 'admin:public_key', 'admin:repo_hook', 'read:org', 'repo'] scopes. Please modify your token's scopes at: https://github.com/settings/tokens."
}
```

&nbsp;

### Permission requirements for project access token

Git administrators must set these minimum permission requirements in the organization/group:

#### GitHub org

| Permissions | Description |
|:-----------------------|:------------|
| admin:org ➜ **read:org** | Enable **read:org** under **admin:org** scope. Grants permission to read org and team membership and org projects. Required to read user information for organization types.<br><img src='/wp-content/uploads/tij-gitcloud-pull-req-timeline-reindex-github-org-setting.png' style='margin:15px auto 0px auto;max-width:100%;display:block;' /> |
| user ➜ **user:email** | Enable **user:email** under **user** scope. Grants read-only access to user email addresses. Required to match users with Jira. |
| user ➜ **read:user** | Optional. Grants read access to all user profile data. |
| **_read:discussion_** | Optional. Grants read access to team discussions. |

&nbsp;

#### GitLab group

| Permissions | Description |
|:------------|:------------|
| **_Role_** | At least Reporter role. |
| **_Scope_** | At least read_api scope. |

&nbsp;

### Which permission scopes should be set for GitHub App integration?

Required scopes for GitHub App integration:

*   **read:org** – Read org and team membership, and org projects

*   **user:email** – Access user email addresses (read-only)

&nbsp;

### More on Signals

[Signals](/git-integration-for-jira-cloud/Signals-gij-cloud)

[General View](/git-integration-for-jira-cloud/Signals-general-view-gij-cloud)

[Teams View](/git-integration-for-jira-cloud/Signals-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/Signals-backlog-view-gij-cloud)

<kbd>Last updated: December 2025</kbd>
