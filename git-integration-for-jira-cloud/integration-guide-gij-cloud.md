---
title: "Integration Guide"
description: "Guide to connecting Git repositories with Jira Cloud using Git Integration for Jira"
product: "Git Integration for Jira Cloud"
feature: "Integration Guide"
content_type: "overview"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "integration", "developer"]
llms_include: true
taxonomy:
    category: git-integration-for-jira-cloud
custom_fields:
    nav_category: "integration-guide-gij-cloud"
    nav_label: "Integration Guide"
    nav_order: 80
    nav_parent: ""
    page_type: "index"
---
<kbd>Last updated: March 2026</kbd>

The Integration Guide helps Jira administrators choose the right setup document for each supported git host in Git Integration for Jira Cloud. Use this page when you need the correct host-specific guide for GitHub, GitLab, Azure DevOps, Bitbucket, AWS CodeCommit, or a Plain Git repository.

---

| Git host or setup path | Best for | Typical integration method | Start here when you need |
| :--- | :--- | :--- | :--- |
| GitHub and GitLab | Cloud-hosted or self-hosted git services with multi-repository support | Git service integration | OAuth or PAT-based setup guidance |
| Azure DevOps or TFS | Microsoft-hosted or self-hosted repositories | Git service integration or webhook indexing | Microsoft-specific setup and repository selection steps |
| AWS CodeCommit and Bitbucket Cloud | Service-specific connection requirements | Git service integration or HTTP/SSH | Provider-specific authentication and repository setup steps |
| Plain Git repository | One SSH or HTTP(S) repository | Single repository integration | Direct repository connection outside the multi-repository flows |

For a comparison of integration types before choosing a git-host guide, see **[Introduction to Git integration](/git-integration-for-jira-cloud/introduction-to-git-integration-gij-cloud)**.

## How to choose the right Git Integration for Jira Cloud guide

Select the git host that matches the repository platform you want to connect. If you need to connect only one repository over SSH or HTTP(S), use the Plain Git repository guide instead of the multi-repository host guides.

<br>


<p>&nbsp;</p>
