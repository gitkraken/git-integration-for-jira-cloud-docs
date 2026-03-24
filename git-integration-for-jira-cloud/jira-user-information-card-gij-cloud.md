---
title: "Jira user information card"
description: "How to view user information cards in Git Integration for Jira Cloud"
product: "Git Integration for Jira Cloud"
feature: "Jira user information card"
content_type: "integration"
audience: "developer"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "User"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "integration", "developer"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

Git Integration for Jira Cloud shows a Jira user information card from the issue view so Jira users can inspect assignee or reporter details without leaving the issue. Use this card when you need quick profile context for a user; configure Git user identity first if the card does not appear.

**Requirements**

- Jira Cloud with Git Integration for Jira Cloud installed
- Permission to view the Jira issue
- Git user identity configured for the user you want to inspect

## Where to find the Jira user information card

The Jira user card is available on the following screens:

*   Jira issue → Developer panel (_Assignee / Reporter_)

<img src='/wp-content/uploads/gij-gitcloud-git-user-profile.png' style='margin:25px auto;max-width:100%;display:block;' />

## How to open and use the Jira user information card

Hover the mouse pointer on the name of the user. A small information box appears containing information such as email, zone and time, and avatar for that user.

Click **Reported issues** to view the latest reported issues by that user.

Click **View profile** to view this user's profile.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <a href='/git-integration-for-jira-cloud/git-user-identity-gij-cloud'><b>Git user identity</b></a> must be configured for the specific user. Otherwise, the user card information will not be displayed for that user.
    </div>
    </div>
</div>

&nbsp;
* * *

[**Prev:** Git user identity](/git-integration-for-jira-cloud/git-user-identity-gij-cloud)

[**Next:** Jira issue page](/git-integration-for-jira-cloud/jira-issue-page-gij-cloud)

<p>&nbsp;</p>

