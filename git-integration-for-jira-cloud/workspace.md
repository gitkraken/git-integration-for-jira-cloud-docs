---

title: Workspace
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Workspace

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/86900944/Workspace>

* * *

This page contains related questions on Git Integration for Jira add-on user experience in Jira.

Use the FAQ below to find answers to common questions.  Feel free to contact our support team ([support@bigbrassband.com](mailto:support@bigbrassband.com?subject=Commits%20display%20issues%20-)) if you don't see what you're looking for.

[How do I see if work has really started on an issue?](#Workspace-seeworkstarted)

[How do I see who has worked on an issue?](#Workspace-seewhoworked)

[How do I see how long ago since someone worked on it?](#Workspace-seesinceworked)

[How do I see what is being changed in this ticket?](#Workspace-seerecentchanges)

  

* * *

  

## **How do I see if work has really started on an issue?**

Open an issue in your browser and click on the **Git Commits** tab.

If the tab says that no Git log entries have been found, then work has not yet started on the ticket.

![View Jira issue git commits](https://bigbrassband.com/images/bbb/jira-issue-git-commits.png)

_See all Git commits associated with an issue in Jira_

  
  

## **How do I see who has worked on an issue?**

Open an issue in your browser and click on the **Git Commits** tab.

Everyone listed in the "Author/Committer" column has worked on the issue.

  

## **How do I see how long ago since someone worked on it?**

Open an issue in your browser and click on the **Git Commits** tab.

All changes to source code are listed from newest to oldest.  The date/time in the "Date/Revision" column on the first line is the last time changes to the issue have been submitted into Git.

  

## **How do I see what is being changed in this ticket?**

Open an issue in your browser and click on the **Git Commits** tab.

When a developer submits a change to Git, they can type a brief message that summarizes the changes.  These messages show up under the Committer/Author's name.

The files that were changed by the developer appear as clickable links. column.  Click on the file links to view the actual source code that was changed.