---

title: Signals Teams View
description: Learn how to use the Teams View in Signals to monitor team member activities, track assignments, and view individual progress.
taxonomy:
    category: git-integration-for-jira-cloud

---

![](/wp-content/uploads/tij-gitcloud-teams-view-main-screen.png)

Teams View displays team activities. Each row represents a team member.

&nbsp;

### Member activities

Click a team member's row to view their activity information.

![](/wp-content/uploads/tij-gitcloud-teams-item-details.png)

Monitor real-time information for each team member:

*   Assigned Jira issues
*   Issues worked on
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

As you scroll, the team member's name stays at the top while displaying their related issues.

&nbsp;

### Member issue details

In the expanded member view, hover on an issue row to see brief information.

<img src='/wp-content/uploads/tij-gitcloud-teams-view-member-issue-mouse-over.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

Click a Jira issue link in the popup to open it in a new browser tab.

<img src='/wp-content/uploads/tij-gitcloud-teams-view-member-issue-dlg-link.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

Click away from the dialog to hide it.

&nbsp;

### Status progress

Hover on the status column to see task progress information.

<img src='/wp-content/uploads/tij-gitcloud-teams-view-issue-hover-status.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

This helps managers plan ahead and monitor assignment progress.

&nbsp;

### Timeline view

![](/wp-content/uploads/tij-gitcloud-teams-view-timeline-gen.png)

Use the timeline view to examine activity boxes for each team member. This provides a concise overview of daily activities and what tasks each member worked on.

<img src='/wp-content/uploads/tij-gitcloud-teams-voew-activity-log-show.png' style='margin:25px auto;max-width:100%;display:block;' />

### Column information

The table below describes each column header.

| Column | Description |
|:-------|-------------|
| **_Issue_** | Team member name with assigned issue count. Click to expand activities. |
| **_Priority_** | Issue priority level. |
| **_Status_** | Task status and progress. |
| **_Contributors_** | Contributors working on the task. |
| **_Assignee_** | Assigned member. |
| **_Days_** | Time worked on the task. |
| **_Comments_** | Comment count. |
| **_Commits_** | Commit count.<br><div class="bbb-callout bbb--alert"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">Install Git Integration for Jira to display commit data.</div></div></div> |
| Pull requests | Pull request count.<br><div class="bbb-callout bbb--alert"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">Install Git Integration for Jira to display pull request data.</div></div></div> |

### Search functions and filters

Use the search panel to set criteria and apply filters.

![](/wp-content/uploads/tij-gitcloud-teams-view-search-panel.png)

Enter search terms in the search box to find and display matching items.

#### Activity filter

![](/wp-content/uploads/tij-gitcloud-teams-view-search-activity-filter.png)

Set **Activity Dates** by selecting an interval from the drop-down list:

*   All Activity - Last 8 weeks
*   Last 4 weeks
*   Last 2 weeks
*   Last 1 week
*   Custom - Select which day from now or before for this filter.

For **Filters**, select one or both options:

*   Show Issues with Jira Activity
*   Show Issues with Git Activity (requires Git Integration for Jira)

Click **Apply selection** to confirm.

For **Contributors**, select one or more members from the drop-down list. The default is **All**. Use the search box to find specific team members. Click **Apply selection** to confirm.

Click **Clear** on each filter group to reset settings.

#### Issue filter

Issue Filters let managers assign filters to the search. Use the search box on each filter to find and select categories. Click **Apply selection** to confirm.

| Category filter | Description |
|:----------------|:------------|
| **_Project_** | Select one or more projects. |
| **_Sprints_** | Select one or more sprints. Choose **No Sprint** for projects without sprints. |
| **_Statuses_** | Select one or more statuses. |
| **_Assignees_** | Select one or more team members. |
| **_Labels_** | Select one or more labels. |
| **_Issue Types_** | Select one or more issue types. |
| **_Versions_** | Select one or more versions. Empty if no versions exist. |
| **_Priorities_** | Select one or more priority states. |
| **_Components_** | Select one or more components. Empty if no components exist. |

Click **Clear All** to reset all filters and search settings to default.

Click **Search** to display results based on your filter settings.

&nbsp;

### More Signals features


[Signals](/git-integration-for-jira-cloud/Signals-gij-cloud)

[General View](/git-integration-for-jira-cloud/Signals-general-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/Signals-backlog-view-gij-cloud)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-Signals-gij-cloud)

<kbd>Last updated: December 2025</kbd>
