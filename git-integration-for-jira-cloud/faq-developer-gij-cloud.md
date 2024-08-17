---

title: Developer - FAQ
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This page contains solutions targeted for developers.

Use the FAQ below to find answers to common questions.  Feel free to contact our [support team](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/)  if you don't see what you're looking for.

[How do Git commits get associated with a Jira issue?](#how-do-git-commits-get-associated-with-a-jira-issue)

[How do I ensure people are following our organization's process for source code?](#how-do-i-ensure-people-are-following-our-organizations-process-for-source-code)

[What will happen to Jira issue associations with commits if the Jira issue is moved to a new project?](#what-will-happen-to-jira-issue-associations-with-commits-if-the-jira-issue-is-moved-to-a-new-project)

[Can the plugin be configured to handle or scan multiple keys for one project?  How is this supposed to work?](#can-the-plugin-be-configured-to-handle-or-scan-multiple-keys-for-one-project-how-is-this-supposed-to-work)

&nbsp;
* * *
&nbsp;

### How do Git commits get associated with a Jira issue?

On every Git commit, make sure the message includes the exact issue ID at the beginning of the text. The Git Integration for Jira Cloud app will automatically index new commits and associate the referenced issue.

To create a link between your Git commit and a Jira issue, developers must include the issue key into the commit comment.

Example git commit message:

"`PROJ-913 - Plugin version change from 2.6.7 to 2.6.8`"; where **_PROJ-913_** is the issue key that links the commit message to the Jira issue.

&nbsp;

### How do I ensure people are following our organization's process for source code?

Open the project summary in your browser and click on the **Git Commits** tab.

All changes that developers have submitted will be listed in reverse chronologically order.  From this view, you can audit all of the changes that developers have recently submitted.

&nbsp;

### What will happen to commit associations if a Jira issue is moved to a new Jira project?

For GIJ Cloud users, moving Jira issues to a different project is not recommended, especially for repositories with extensive git commit histories. This is because associated git commits from the old project do not automatically transfer to the new project due to the different name.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Git Integration for Jira Cloud app allows users to manually associate git commits to a Jira issue via the Repository browser.
    </div>
    </div>
</div>

To manually associate git commits to a Jira issue in Jira Cloud:

1.  Go to Jira dashboard menu Apps ➜ **Git Integration: Repository browser**.
2.  Click a repository to work on. The list defaults to the Compare view.
3.  Click on the **Commits** tab.
4.  On the right of the list item, click on the edit ![](/wp-content/uploads/gij-edit-icon-dark.png) icon to manage Jira issue association for the selected git commit.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Git Integration for Jira Cloud app also supports multiple issue keys in a commit message.
    </div>
    </div>
</div>

For Jira administrators planning to migrate from Jira Server/Data Center to Jira Cloud, please read this first - [Export project from Jira Server to Jira Cloud](https://community.atlassian.com/t5/Jira-questions/Export-project-from-Jira-server-to-Jira-Cloud/qaq-p/2191398&ved=2ahUKEwjr5eqBzvmHAxXUn2MGHcd9AmwQFnoECB4QAw&usg=AOvVaw0QNt6X4OFeIZ1KvZWmz4Y4).

When transitioning from Jira self-hosted to Jira Cloud, maintaining the same project name will retain all git commit associations after the migration.

&nbsp;

### Can the plugin be configured to handle or scan multiple keys for one project?  How is this supposed to work?

Yes – the Git Integration for Jira Cloud app supports multiple Jira issue keys in a multiple-line commit message.

For more information, see **[Smart Commits »](/git-integration-for-jira-cloud/smart-commits-gij-cloud)**.

