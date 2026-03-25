---
title: "Known Issues for Signals"
description: "Review known issues and workarounds for the Signals feature in Git Integration for Jira Cloud."
product: "Git Integration for Jira Cloud"
feature: "Known Issues for Signals"
content_type: "troubleshooting"
audience: "all"
plan_required: "Advanced"
deployment: "Jira Cloud"
git_host_support: []
role_required: "all"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "troubleshooting", "Advanced"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Signals provides features for team leaders and project leads. This page documents known issues and their workarounds.

&nbsp;

### Users disappear from search results when typing

**Issue:** When searching for a user through a filter (contributor or assignee), typing more than a few characters causes search results to disappear.

**Details:** If your search text contains two characters or fewer, user names display correctly in the recommended list and search results. When you type more than three characters, the matching name no longer appears in the list. Searching by last name works correctly and shows expected results.

**Status:** This issue will be fixed in a future version.

&nbsp;

### Backlog page text search does not return expected Jira issues

**Issue:** The Backlog view may not display the expected Jira issue when you search by issue key.

**Cause:** This behavior results from slow data loading. This tradeoff allows users to view all Jira issues in the Backlog view.

**Workaround:** Search by issue summary using wildcards:

![](/wp-content/uploads/tij-gitcloud-search-list-example.png)

You can also search by issue key directly. When using this approach, specify a valid Jira issue key to avoid errors. Issue key search does not support wildcards:

![](/wp-content/uploads/tij-gitcloud-search-supports-jql-example.png)

Invalid issue key searches produce an error message:

![](/wp-content/uploads/tij-gitcloud-search-error-example-01.png)

&nbsp;

### More on Signals features

[General View](/git-integration-for-jira-cloud/Signals-general-view-gij-cloud)

[Teams View](/git-integration-for-jira-cloud/Signals-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/Signals-backlog-view-gij-cloud)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-Signals-gij-cloud)

<p>&nbsp;</p>
