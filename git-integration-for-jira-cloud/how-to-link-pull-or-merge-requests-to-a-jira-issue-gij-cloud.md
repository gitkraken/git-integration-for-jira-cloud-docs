---

title: How to link pull or merge requests to a Jira issue?
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

### Git service

Associate pull or merge requests to a Jira issue by inserting the Jira issue key to the pull request when creating them.

![](/wp-content/uploads/gij-github-web-create-pull-request-sample.png)

Create a pull/merge request and associate it to a Jira issue:

1.  Set base and compare as required. (branch to master)

2.  Enter a new pull request title on the provided box. Mention a Jira issue key in the title to associate it to the said Jira issue.

3.  Also, mentioning a Jira issue key on the description will associate this pull request to the said Jira issue.

### Git Integration for Jira app

This can also be easily done via Jira issue Git integration developer panel:

1.  Open a Jira issue.

2.  On the right sidebar, click on **Git Integration**. This opens the Jira issue Git integration developer panel.

3.  Click **Create pull request** or **Create merge request** (GitLab).

4.  Select a repository.

5.  Select the Source branch to use as base.

6.  Select the Target branch to merge the source branch to.

6.  The PR/MR name is automatically generated populated from the issue summary with inserted Jira issue key.

7.  Edit the proposed name but leave the Jira issue key as is or... accept the generated branch name as it is.


