---
title: Deprecation notice (GIJ Cloud)
description: Features and functionality being deprecated or removed from Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This page lists features and functionality that are deprecated or scheduled for removal from Git Integration for Jira Cloud.

| Feature | Date | Details |
|---------|------|---------|
| Personal access tokens | Varies by Git service | Some Git services like GitLab and GitHub require personal access tokens for authentication. TFS 2017+ enforces PAT authentication. TFS 2013/2015 does not support PAT. |
| `${username}` variable | April 29, 2019 | The `${username}` variable in branch name templates is deprecated. Atlassian no longer provides usernames. |
| Ignore unmatching webhooks | September 14, 2021 | Git Integration for Jira no longer reindexes all repositories by default when a webhook arrives without a matching repository. |
| GitLab legacy integrations | June 6, 2023 | Support for GitLab legacy integrations dropped in v4.19+. |
| GitLab legacy integrations removal | End of March 2024 | GitLab legacy integrations deprecated in the Manage integrations screen. Upgrade your GitLab server, remove legacy integrations, and connect a new GitLab CE/EE integration. |

<kbd>Last updated: December 2025</kbd>
