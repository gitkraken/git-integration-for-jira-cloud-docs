---
title: "Code syntax highlighter"
description: "Step-by-step guide to Code syntax highlighter in Git Integration for Jira Cloud, for Jira Cloud users."
product: "Git Integration for Jira Cloud"
feature: "Code syntax highlighter"
content_type: "integration"
audience: "all"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "all"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "integration"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

The code diff dialog view has been improved. The Git Integration for Jira app uses the correct syntax highlighting when viewing the code diff of the file based on its file extension:

|     |     |
| --- | --- |
| **File Extension** | **Language ID** |
| **css** | CSS |
| **js** | Javascript |
| **cpp** | C++ |
| **cs** | C#  |
| **sh** | Bash |
| **java** | Java |
| **sql** | SQL |
| **py** | Phyton |
| **rb** | Ruby |
| **php, phtml, php3, php4, php5** | PHP |
| **html, html, xhtml, xml** | Markup |
| **c, h, m, mm, pl, pm** | CLike |

There is no language auto-detection in the diff dialog. The detection is based on file extension.

This feature will only display properly on browsers supported by Atlassian for specific versions of Jira:

<!--*   [**Jira 6.3 supported platforms**](https://confluence.atlassian.com/jira063/supported-platforms-683541780.html)-->

*   [**Jira 7.x supported platforms**](https://confluence.atlassian.com/adminjiraserver0713/supported-platforms-964983071.html)

*   [**Jira 8.x supported platforms**](https://confluence.atlassian.com/adminjiraserver/supported-platforms-938846830.html)
