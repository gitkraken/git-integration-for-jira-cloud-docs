---
title: "Hooks and Webhooks"
description: "Configure client-side hooks, server-side hooks, and indexing triggers for Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Hooks and Webhooks"
content_type: "concept"
audience: "all"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "all"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "concept"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

This section covers hooks and webhooks supported by Git Integration for Jira Cloud. Use these features to enforce commit policies and enable real-time repository indexing.

| Feature type | Runs where | Best for | Related page |
| :--- | :--- | :--- | :--- |
| Client-side hooks | Developer workstation | Validating commit messages before commit | `commit-msg` hook |
| Server-side hooks | Git server | Enforcing repository policies on push | Server-side hooks |
| Indexing triggers | Jira Cloud plus git host webhook | Faster repository reindexing after remote activity | Indexing triggers |

## How to choose between hook types and indexing triggers

### [Configure Client-Side Hooks](/git-integration-for-jira-cloud/commit-msg-hook-gij-cloud)

Set up the **commit-msg** hook as a Python script in developers' local repositories to validate commit messages before they're accepted.

### [Configure Server-Side Hooks](/git-integration-for-jira-cloud/server-side-hook-gij-cloud)

Apply project policies using server-side hooks. These scripts run before and after pushes, requiring Python on the server.

## How to use indexing triggers for reindexing

### [Set Up Indexing Triggers](/git-integration-for-jira-cloud/indexing-triggers-gij-cloud)

Configure webhooks to trigger immediate reindexing of your repositories from remote systems, providing near real-time git data in Jira.

