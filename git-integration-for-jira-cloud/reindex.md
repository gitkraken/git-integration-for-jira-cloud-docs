---

title: Reindex
description:
taxonomy:
    category: git-integration-for-jira-cloud

---


# Reindex

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/87785473/Reindex>

* * *

This page contains related questions about git notes, reindex tracking and control.

Use the FAQ below to find answers to common questions.  Feel free to contact our support team ([support@bigbrassband.com](mailto:support@bigbrassband.com?subject=Reindex%20issues%20-)) if you don't see what you're looking for.

[What does re-index do?](/wiki/pages/resumedraft.action?draftId=87785473#Reindex-wdreindexdo)

[Is there any way to control the reindex?](/wiki/pages/resumedraft.action?draftId=87785473#Reindex-waytoctrlreidx)

[Commits are not showing right away.  Can they show up faster?](/wiki/pages/resumedraft.action?draftId=87785473#Reindex-showcommitsfast)

[Is it possible to track the specified branches when reindexing?](/wiki/pages/resumedraft.action?draftId=87785473#Reindex-idxtrackbranches)

  

* * *

## **What does re-index do?**

Re-index does 2 operations:

*   Updates the cloned repo from remote
*   Updates the indexes which contain info about every commit

## **Is there any way to control the reindex?**

In terms of kicking off the indexing based on an event, you have two options:

*   Hooks > Webhook: **[Hooks: Git add-on Webhooks](https://bigbrassband.com/hooks/jira-git-webhooks.html "Git for Jira add-on webhooks")**
*   Webhook: **[Git for Jira add-on: Configure Webhooks](https://bigbrassband.com/git-integration-for-jira/documentation/git-for-jira-webhooks.html)**

What other users have done is set a high interval and then configure one of those options.

## **Commits are not showing right away.  Can they show up faster?** 

Commits won't appear immediately. Configure webhooks via **Manage Git repositories** page to make commits show faster.

## **Is it possible to track the specified branches when reindexing?**

No.  The Git Integration for Jira app is designed to do a full index.

  

The reindex process won't start if reindex is already running.

For more information on indexing, see [Indexing Explainer for Git Integration for Jira Cloud](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/183369754/Indexing+Explainer).