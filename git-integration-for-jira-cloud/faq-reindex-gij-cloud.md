---

title: Reindex
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This page contains related questions about git notes, reindex tracking and control.

Use the FAQ below to find answers to common questions.  Feel free to contact our [support team](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/) if you don't see what you're looking for.

- [What does re-index do?](#what-does-re-index-do)
- [Is there any way to control the reindex?](#is-there-any-way-to-control-the-reindex)
- [Commits are not showing right away.  Can they show up faster?](#commits-are-not-showing-right-away-can-they-show-up-faster)
- [Is it possible to track the specified branches when reindexing?](#is-it-possible-to-track-the-specified-branches-when-reindexing)

* * *

## What does re-index do?

Re-index does 2 operations:

*   Updates the cloned repo from remote
*   Updates the indexes which contain info about every commit

## Is there any way to control the reindex?

In terms of kicking off the indexing based on an event:

*   Webhook: [Configure Webhooks](/git-integration-for-jira-cloud/indexing-triggers-formerly-webhooks-gij-cloud)

What other users have done is set a high interval and then configure one of those options.

## Commits are not showing right away.  Can they show up faster?

Commits won't appear immediately. Configure webhooks via **Manage Git repositories** page to make commits show faster.

## Is it possible to track the specified branches when reindexing?

No. The Git Integration for Jira app is designed to do a full index.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The reindex process won't start if reindex is already running.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For more information on indexing, see [Indexing Explainer for Git Integration for Jira Cloud](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud/).
    </div>
    </div>
</div>

