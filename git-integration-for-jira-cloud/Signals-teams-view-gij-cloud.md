---

title: Signals Teams View
description: Learn how to use the Teams View in Signals to monitor team member activities, track assignments, and view individual progress.
taxonomy:
    category: git-integration-for-jira-cloud

---

![](/wp-content/uploads/tij-gitcloud-teams-view-main-screen.png)

Teams View displays team activities with each row representing a team member. This page explains how to use Teams View to monitor workloads and track individual progress.

&nbsp;

### Viewing member activities

To view a team member's activity information, click their row.

![](/wp-content/uploads/tij-gitcloud-teams-item-details.png)

The expanded view displays real-time information for each team member:

*   Assigned Jira issues
*   Issues the member worked on
*   Issue priorities
*   Time spent on issues
*   Git statistics (requires Git Integration for Jira)
*   Progress and status of each issue
*   Task deadlines via the timeline

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This view helps project managers quickly assess workloads and make necessary adjustments.
    </div>
    </div>
</div>

As you scroll, the team member's name stays at the top while displaying their related issues below.

&nbsp;

### Viewing member issue details

In the expanded member view, hover on an issue row to see brief information about that issue.

<img src='/wp-content/uploads/tij-gitcloud-teams-view-member-issue-mouse-over.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

To open the Jira issue in a new browser tab, click the issue link in the popup.

<img src='/wp-content/uploads/tij-gitcloud-teams-view-member-issue-dlg-link.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

To close the dialog, click anywhere outside it.

&nbsp;

### Checking status progress

To view task progress information, hover on the status column.

<img src='/wp-content/uploads/tij-gitcloud-teams-view-issue-hover-status.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

This information helps managers plan ahead and monitor assignment progress.

&nbsp;

### Using the timeline view

![](/wp-content/uploads/tij-gitcloud-teams-view-timeline-gen.png)

The timeline view shows activity boxes for each team member. This provides a concise overview of daily activities and the tasks each member worked on.

<img src='/wp-content/uploads/tij-gitcloud-teams-voew-activity-log-show.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

### Understanding the columns

The table below describes each column header in Teams View.

| Column | Description |
|:-------|:------------|
| **Issue** | Displays the team member name with their assigned issue count. Click to expand and view activities. |
| **Priority** | Shows the issue priority level. |
| **Status** | Shows the task status and progress percentage. |
| **Contributors** | Lists contributors working on the task. |
| **Assignee** | Shows the assigned member. |
| **Days** | Shows the time worked on the task. |
| **Comments** | Shows the comment count. |
| **Commits** | Shows the commit count.<br><div class="bbb-callout bbb--alert"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">Install Git Integration for Jira to display commit data.</div></div></div> |
| **Pull requests** | Shows the pull request count.<br><div class="bbb-callout bbb--alert"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">Install Git Integration for Jira to display pull request data.</div></div></div> |

&nbsp;

### Searching and filtering

Use the search panel to set criteria and apply filters.

![](/wp-content/uploads/tij-gitcloud-teams-view-search-panel.png)

Enter search terms in the search box to find and display matching items.

&nbsp;

#### Filtering by activity

![](/wp-content/uploads/tij-gitcloud-teams-view-search-activity-filter.png)

To set the activity date range, select from the **Activity Dates** dropdown:

*   All Activity - Last 8 weeks
*   Last 4 weeks
*   Last 2 weeks
*   Last 1 week
*   Custom - Select specific start and end dates

Under **Filters**, select one or both options:

*   Show Issues with Jira Activity
*   Show Issues with Git Activity (requires Git Integration for Jira)

Click **Apply selection** to confirm your choices.

Under **Contributors**, select one or more members from the dropdown. Default: **All**. Use the search box to find specific team members. Click **Apply selection** to confirm.

To reset a filter group, click **Clear**.

&nbsp;

#### Filtering by issue attributes

Issue filters let managers narrow results to specific criteria. Use the search box in each filter category to find and select items. Click **Apply selection** to confirm.

| Category filter | Description |
|:----------------|:------------|
| **Project** | Select one or more projects. |
| **Sprints** | Select one or more sprints. Choose **No Sprint** for issues without sprints. |
| **Statuses** | Select one or more statuses. |
| **Assignees** | Select one or more team members. |
| **Labels** | Select one or more labels. |
| **Issue Types** | Select one or more issue types. |
| **Versions** | Select one or more versions. Empty if no versions exist. |
| **Priorities** | Select one or more priority states. |
| **Components** | Select one or more components. Empty if no components exist. |

&nbsp;

#### Resetting filters

To reset all filters and search settings to defaults, click **Clear All**.

To apply your filter selections and display results, click **Search**.

&nbsp;

### More on Signals features

[Signals](/git-integration-for-jira-cloud/Signals-gij-cloud)

[General View](/git-integration-for-jira-cloud/Signals-general-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/Signals-backlog-view-gij-cloud)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-Signals-gij-cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
