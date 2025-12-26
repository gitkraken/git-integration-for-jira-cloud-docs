---

title: Admin Getting Started Guide
description: Essential configuration guide for Jira Admins setting up Git Integration for Jira Cloud
taxonomy:
    category: git-integration-for-jira-cloud

---

## Application Overview

Thank you for choosing Git Integration for Jira Cloud (GIJ). This guide provides Jira Admins with essential information for configuring Git Integration for Jira effectively.

GIJ is designed as a "set it and forget it" application. Jira Admins who read each page of this guide can expect to save significant time on configuration. Let's get started.

&nbsp;

## What to Expect

GIJ displays commits, branches, and pull/merge requests associated with specific Jira issues. To link items to Jira issues, include the Jira issue key in:

- The commit message
- The branch name
- The pull/merge request title

For more details, see [Linking Git Commits](/git-integration-for-jira-cloud/linking-git-commits-to-jira-issues-gij-cloud/).

### Information Displayed in Jira Issues

![Jira Issue View](/wp-content/uploads/Jira-Issue-Breakdown-2025.png)

**Activity Stream - Git Commits**

1. Git Commits tab in the activity stream, organized by repository
2. Individual commit with the developer who made it
3. Commit message
4. Commit line change summary by file
5. Link to view code diff in Jira

**Git Integration Panel**

6. Options to create a branch or pull request directly from a Jira issue
7. Associated branches and pull requests with status icons

&nbsp;

## Security Restrictions and Policies

Before configuring the application, discuss your team's needs and security requirements. Consider:

- Whether your team has restrictions on third-party applications cloning code
- Whether you need to restrict code visibility between Jira projects

Use [Project Association Permissions](/git-integration-for-jira-cloud/setting-project-permissions-gij-cloud/) to limit visibility between Jira projects. See [Permissions](/git-integration-for-jira-cloud/permissions-gij-cloud/) for details on limiting visibility of GIJ panels and data between Jira users.

&nbsp;

---

[<b style='background-color:#FFFCC3; padding:1px 5px; color:#181D28; border-radius:3px; margin: 0 5px; font-size: medium;'>NEXT</b>](/git-integration-for-jira-cloud/Getting-Started-Guide-App-operations-and-planning) <a href="https://help.gitkraken.com/git-integration-for-jira-cloud/Getting-Started-Guide-App-operations-and-planning/">Application Operations and Integration Structure Planning</a>

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
