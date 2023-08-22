---

title: How to link branches to a Jira issue?
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

### Git service (GitHub example)

Associate branches to a Jira issue by inserting the Jira issue key to the branch name when creating them.

<img src='/wp-content/uploads/gij-github-web-create-branch-sample.png' style='margin:25px auto;max-width:100%;display:block;' />

Create a branch and associate it to a Jira issue:

1.  Select the _master_ branch dropdown.

2.  Enter a new branch name on the search box. Mention a Jira issue key in the name to associate it to the said Jira issue.

3.  Click the result to create the new branch.


### Git Integration for Jira app

This can also be easily done via Jira issue Git integration developer panel:

1.  Open a Jira issue.

2.  On the right sidebar, click on **Git Integration**. This opens the Jira issue Git integration developer panel.

3.  Click **Create branch**.

4.  Select a repository.

5.  Select the Source branch to use as base.

6.  The Branch name is automatically generated populated from the issue summary with inserted Jira issue key.

7.  Edit the proposed name but leave the Jira issue key as is or... accept the generated branch name as it is.


