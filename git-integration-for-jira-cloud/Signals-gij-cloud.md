---

title: Signals - GIJ Advanced
description: Learn how to use Signals (Team Insights for Jira) to monitor team activity, track sprint progress, and identify work risks in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='382' src='https://www.youtube.com/embed/ctzCdY9CXOg' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:12px;margin-bottom:40px;'>
    <i>Right click <a href='https://www.youtube.com/watch?v=ctzCdY9CXOg'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

Signals monitors git history and Jira team activity at the project, epic, and sprint levels. Managers use Signals to prioritize work, identify risks, reveal trends, and make informed decisions about team workflows.

![](/wp-content/uploads/tij-gitcloud-main-default-view-general-tab.png)

Signals provides a complete view of team work and progress, highlighting at-risk items based on activity and progress metrics.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Install Git Integration for Jira Cloud to add Git data to your views and enhance planning workflows.
    </div>
    </div>
</div>

&nbsp;

### Installing Signals

Starting February 11, 2025, Team Insights for Jira Cloud merged with Git Integration for Jira Cloud.

To install Signals:

1.  Visit the Atlassian Marketplace and search for [Git Integration for Jira by GitKraken](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud).

    ![](/wp-content/uploads/gij-gitcloud-new-installation-trial-buy-c.png)

2.  Click **Try it free** to start the free 30-day trial.

    ![](/wp-content/uploads/gij-gitcloud-try-new-git-for-jira-cloud-app-c.png)

3.  Log in to your Jira account when prompted.

For pricing details, see [Git Integration for Jira Cloud pricing and subscription tiers](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=pricing). The system configures the license key automatically for free trials.

After installation completes, a confirmation message appears:

![](/wp-content/uploads/gij-gitcloud-installation-success-msg-balloon-c.png)

From the confirmation message:

*   Click **Get started** to open the Manage integrations page and configure git repositories.

*   Click **Manage app** to open the Manage apps page and view app properties, version, and license details.

&nbsp;

### Migration from standalone Team Insights for Jira

#### Does standalone TIJ Cloud migrate automatically to the merged GIJ+TIJ Cloud app?

Yes. Migration happens automatically when you install Git Integration for Jira. No manual migration steps required.

#### Does the TIJ extension stop working when the GIJ app license expires?

No. The TIJ extension operates independently. Your TIJ data remains accessible regardless of GIJ license status.

&nbsp;

### Feature comparison

Signals displays activity across projects, epics, and sprints. The table below compares features available with TIJ only versus GIJ + TIJ combined.

| Feature   | TIJ Only  | GIJ + TIJ |
|:----------|:----------|:----------|
| Identify stale issues or issues that revert in status | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| View activities for sprint planning, standups, and retrospectives<sup>1</sup> | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Access insights for executives, managers, and individual contributors<sup>1</sup> | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Enable all team members to identify and contribute improvements | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Support all departments that use Jira in your organization | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Track issue status progress over time, including where and how long issues remained in each state | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Identify pull requests that remain open too long<sup>2</sup> | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| View commits and other git-related data for your team | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Create branches and pull/merge requests from Jira issues | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Link webhooks to Git and Jira for faster git data display | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Manage git integrations and repository connections | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Assign other users to manage integrations and repository connections | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |

<b><sup>1</sup></b> With Git Integration for Jira installed, git data displays in more detail.

<b><sup>2</sup></b> Requires Git Integration for Jira to view pull request status and information.

&nbsp;

### Permissions

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT!</b>

Jira user permissions control access to Signals data. Users who can view Jira issues can also view the corresponding Signals data for those issues.

&nbsp;

### Accessing Signals

![](/wp-content/uploads/tij-gitcloud-menu-access-location.png)

To access Signals from the Jira dashboard, navigate to **Apps** ➜ **Git Integration: Team Insights**.

&nbsp;

### Feature highlights

Signals displays Git activity across projects and issues, revealing collaboration patterns and development progress.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Analyze Git activity to identify trends, track progress, and make data-driven decisions.
    </div>
    </div>
</div>

&nbsp;

#### Customize views across projects, epics, and sprints

View timelines by epics, issues, and sub-tasks. Filter by project, sprint, team members, issue status, and more. Sort tasks by days since last status update or by commit count.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        These sorting options reveal workflow bottlenecks and help you stay organized.
    </div>
    </div>
</div>

&nbsp;

#### Manage Jira workflows efficiently

Focus on issues that demand immediate attention. View user actions and timing across multiple issues. Identify tasks at risk of missing deadlines, team members with excessive workloads, stagnant issues, reverted closed issues, and pull requests that remain open too long.

&nbsp;

#### Enhance team collaboration

Use Signals views during sprint, epic, and backlog planning. Analyze data to identify recurring patterns, detect trends, and find areas for improvement.

&nbsp;

#### Track and improve team productivity

Signals displays your team's Jira and Git activity over time, enabling you to track current tasks and monitor progress.

Signals shows Jira activity for all users. When you install [Git Integration for Jira](https://www.gitkraken.com/git-integration-for-jira), branches, commits, pull requests, and tags appear automatically in your views.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This combination enhances team workflows with no additional setup required.
    </div>
    </div>
</div>

&nbsp;

### More on Signals features

**Signals** (this page)

[General View](/git-integration-for-jira-cloud/Signals-general-view-gij-cloud/)

[Teams View](/git-integration-for-jira-cloud/Signals-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/Signals-backlog-view-gij-cloud/)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-Signals-gij-cloud/)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
