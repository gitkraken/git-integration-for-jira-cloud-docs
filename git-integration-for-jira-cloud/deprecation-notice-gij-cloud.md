---
title: "Deprecation notice (GIJ Cloud)"
description: "Features and functionality being deprecated or removed from Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Deprecation notice (GIJ Cloud)"
content_type: "concept"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "deprecated"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "concept", "admin", "deprecated"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

This page lists features and functionality that are deprecated or scheduled for removal from Git Integration for Jira Cloud.

| Feature | Date | Details |
|---------|------|---------|
| Personal access tokens | Varies by Git service | Some Git services like GitLab and GitHub require personal access tokens for authentication. TFS 2017+ enforces PAT authentication. TFS 2013/2015 does not support PAT. |
| `${username}` variable | April 29, 2019 | The `${username}` variable in branch name templates is deprecated. Atlassian no longer provides usernames. |
| Ignore unmatching webhooks | September 14, 2021 | Git Integration for Jira no longer reindexes all repositories by default when a webhook arrives without a matching repository. |
| GitLab legacy integrations | June 6, 2023 | Support for GitLab legacy integrations dropped in v4.19+. |
| GitLab legacy integrations removal | End of March 2024 | GitLab legacy integrations deprecated in the Manage integrations screen. Upgrade your GitLab server, remove legacy integrations, and connect a new GitLab CE/EE integration. |
