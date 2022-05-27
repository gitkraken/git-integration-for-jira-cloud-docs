---

title: Developer
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
This page contains solutions targeted for developers.

Use the FAQ below to find answers to common questions.  Feel free to contact our support team ([support@bigbrassband.com](mailto:support@bigbrassband.com?subject=Developer%20questions%20-)) if you don't see what you're looking for.

[How do Git commits get associated with a Jira issue?](#Developer-assocgitcommits)

[How do I ensure people are following our organization's process for source code?](#Developer-followprocs)

[What will happen to Jira issue associations with commits if the Jira issue is moved to a new project?](#Developer-issuemovenewproj)

[Can the plugin be configured to handle or scan multiple keys for one project?  How is this supposed to work?](#Developer-handlemultikeys)



* * *

## **How do Git commits get associated with a Jira issue?**

On every Git commit, make sure the message includes the exact issue ID at the beginning of the text. The Git Integration for Jira Cloud app will automatically index new commits and associate the referenced issue.

To create a link between your Git commit and a Jira issue, developers must include the issue key into the commit comment.

Example git commit message:

"`PROJ-913 - Plugin version change from 2.6.7 to 2.6.8`"; where **_PROJ-913_** is the issue key that links the commit message to the Jira issue.



## **How do I ensure people are following our organization's process for source code?**

Open the project summary in your browser and click on the **Git Commits** tab.

All changes that developers have submitted will be listed in reverse chronologically order.  From this view, you can audit all of the changes that developers have recently submitted.



## **What will happen to Jira issue associations with commits if the Jira issue is moved to a new project?**

The commit retains the association even in the new project.  The Git Integration for Jira Cloud app supports history tracking.  Thus, when moving a ticket to a new project whose issue key has changed, the association will still work.

The steps below provides an outline that you can follow to verify that the issue associations with commits are retained:

1.  Associate a commit with issue (ex. **TEST-1**)
2.  Move the issue **TEST-1** to a new project (ex. **PM**)
3.  New issue key for **TEST-1** is **PM-18**
4.  Check that original commit in **TEST-1** is still available in **PM-18**.  The commit should be there (Git Commits tab).
5.  In the **Git Repositories** configuration page, perform **Reset** and **Reindex** on the selected repository to make sure that the commit was in the correct location.

The Git Integration for Jira Cloud app also supports multiple issue keys in a commit message.

## **Can the plugin be configured to handle or scan multiple keys for one project?  How is this supposed to work?**

Yes – the Git Integration for Jira Cloud app supports multiple Jira issue keys in a multiple-line commit message.

For more information, see **[Smart Commits »](/git-integration-for-jira-cloud/smart-commits-gij-cloud/)**.