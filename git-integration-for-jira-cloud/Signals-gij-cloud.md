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

### Installation

Starting February 11, 2025, Team Insights for Jira Cloud merged with Git Integration for Jira Cloud.

1.  Visit the Atlassian Marketplace and search for [Git Integration for Jira by GitKraken](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud).

![](/wp-content/uploads/gij-gitcloud-new-installation-trial-buy-c.png)

2.  Click **Try it free** to start the free 30-day trial.

![](/wp-content/uploads/gij-gitcloud-try-new-git-for-jira-cloud-app-c.png)

3.  Log in to your Jira account when prompted.

For pricing details, see [Git Integration for Jira Cloud pricing and subscription tiers](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=pricing). The system configures the license key automatically for free trials.

After installation, a confirmation message appears:

![](/wp-content/uploads/gij-gitcloud-installation-success-msg-balloon-c.png)

*   Click **Get started** to open the Manage integrations page and configure git repositories.

*   Click **Manage app** to open the Manage apps page and view app properties, version, and license details.

Installation is complete.

&nbsp;

### Migration of Standalone TIJ Cloud data to GIJ\+TIJ Cloud

#### Do I need to migrate TIJ Cloud standalone to the merged GIJ+TIJ Cloud app?

No. Migration happens automatically.

#### Does the TIJ extension become inaccessible when the GIJ app expires?

No. The TIJ extension operates independently. Your TIJ data remains accessible.

&nbsp;

### Feature matrix

Signals displays activity across projects, epics, and sprints.

| Feature   | TIJ Only  | GIJ + TIJ |
|:----------|:----------|:----------|
| Identify stale issues or issues that revert in status | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| See activities for sprint planning, stand ups, and retrospectives<sup>1</sup> | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Helpful insights for executives, managers, and individual contributors<sup>1</sup> | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Enable all team members to identify and contribute improvements | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Valuable for all departments that use Jira in your organization | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Easily see issue status progress over time, where it changed, and how long it remained in that state | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Identify pull requests that remain open too long<sup>2</sup> | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| View commits and other git related data for your team | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Create branches and pull/merge requests in Jira issues for your team | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Link webhooks to your Git and Jira for faster display of git data | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Manage git integrations and repository connections | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Assign other users to manage integrations and repository connections | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |

<b><sup>1</sup></b> With Git Integration for Jira app also installed, git data displays in more detail.

<b><sup>2</sup></b> Requires Git Integration for Jira app installed to see pull request status and information.

&nbsp;

### Permissions

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT!</b>

Jira user permissions control access to Signals data. Users who can view Jira issues can also view Signals data.

&nbsp;

### Accessing Signals

![](/wp-content/uploads/tij-gitcloud-menu-access-location.png)

Access Signals from the Jira dashboard: **Apps** ➜ **Git Integration: Team Insights**.

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

View timelines by Epics, Issues, and Sub-tasks. Filter by project, sprint, team members, issue status, and more. Sort tasks by days since last status update or by commit count.

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

Focus on issues that demand immediate attention. See user actions and timing across multiple issues. Identify tasks at risk of missing deadlines, team members with excessive workloads, stagnant issues, reverted closed issues, and pull requests open too long.

&nbsp;

#### Enhance team collaboration

Use Signals views during sprint, epic, and backlog planning. Analyze data to identify recurring patterns, detect trends, and find areas for improvement.

&nbsp;

#### Track and improve team productivity

Signals displays your team's Jira and Git activity over time. Track current tasks and monitor progress.

Signals shows Jira activity for all users. When you install [Git Integration for Jira](https://www.gitkraken.com/git-integration-for-jira), branches, commits, pull requests, and tags appear automatically in views.

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

<kbd>Last updated: December 2025</kbd>
