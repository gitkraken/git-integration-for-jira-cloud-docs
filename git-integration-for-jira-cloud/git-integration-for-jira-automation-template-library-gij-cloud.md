---

title: Git Integration for Jira automation template library
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Let automation do the work while your developers focus on what’s important.  Automation Templates for Git Integration for Jira can be implemented so you never need to start from scratch. We’ve provided some templates we think are useful so you don't need to create your own automation rules from scratch.

\*All of the templates from [Atlassian’s template library](https://www.atlassian.com/software/jira/automation-template-library/bitbucket-github-gitlab) will work with Git Integration for Jira

<img src='/wp-content/uploads/gij-automation-library-template.png' style='margin:25px auto;max-width:100%;display:block;height:auto;width:470px;' />

**With Git Integration for Jira you can integrate any Git repository with Jira.  And better yet, you can make use of any of our handy automation templates, or use Atlassian’s!**

You can write your own templates using [Atlassian's no-code Jira automation engine](https://www.atlassian.com/software/jira/features/automation).

&nbsp;
### Available templates from Atlassian for Git Integration for Jira users:

Here are some templates from Atlassian you can use as a guide for some of the most common uses:

*   [When a commit is created, then transition the Jira issue](https://www.atlassian.com/software/jira/automation-template-library/rules#/rule/1357202).

*   [When a PR is created, add a comment to the Jira issue](https://www.atlassian.com/software/jira/automation-template-library/rules#/rule/1357211).

*   [When a commit is created then send Slack message based on assignee](https://www.atlassian.com/software/jira/automation-template-library/rules#/rule/1357149).

&nbsp;

### And here’s some handy use cases for automation for Git Integration for Jira users:

*   Transition issue state when a commit arrives.

*   Transition issue state when pull/merge request is merged. For example: from IN PROGRESS to DONE.

&nbsp;

### For more powerful conditions:

*   Use [Jira Automation Smart Values](https://support.atlassian.com/jira-software-cloud/docs/what-are-smart-values/) to extract data from your commits and branches to be used in an automation action such as;

    *   Take actions based on the name of a branch. For example:

        *   only transition branches that contain a specific keyword like “WIP” (Work In Progress).

        *   add a comment to an issue when a branch contains a certain keyword.

    *   Extract the pullRequest state (Open vs Merged vs Declined) from a Pull request, and use it in an [advanced compare condition](https://support.atlassian.com/jira-software-cloud/docs/automation-conditions/)

    *   Ensure the commit message contains things you’re looking for, like issue keys, etc.

    *   Verify that only certain repos trigger the automation

    *   See the full list of [available smart values](https://support.atlassian.com/jira-software-cloud/docs/smart-values-development/)

&nbsp;

### Supported triggers:

We currently support the 5 highlighted triggers depicted below, and we will support all of these triggers in coming releases.

<img src='/wp-content/uploads/gij-jira-cloud-automation-supported-triggers.png' style='margin:25px auto;width:566px;height:auto;display:block;max-width:100%;' />

### Setup:

[Git Integration + Jira Automation](/git-integration-for-jira-cloud/git-integration-jira-automation-gij-cloud)

