---

title: Signals Backlog View
description: Learn how to use the Backlog View in Signals to track sprint progress, identify work risks, and manage backlog priorities.
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='382' src='https://www.youtube.com/embed/nxp_D7UuVU8' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='' style='margin-top:12px;margin-bottom:40px;'>
    <i>Right click <a href='https://www.youtube.com/watch?v=nxp_D7UuVU8'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

Backlog View tracks work progress and highlights items needing attention.

&nbsp;

### Introduction

Backlog View helps identify work risks before missed deadlines. It organizes issues into sprints for easy tracking.

Use Backlog View to:

*   View Git repository activity during sprint planning
*   Identify at-risk issues and adjust plans
*   Run faster, more effective standups

&nbsp;

### Getting started

![](/wp-content/uploads/tij-gitcloud-backlog-view-main-screen.png)

Click the Backlog View tab at the top of the Signals page.

Backlog View groups issues by sprint, similar to Epics mode in General View. Use the Project filter to manage your backlog. Sprints sort by rank when the view loads.

&nbsp;

### Activity timeline

The Activity timeline displays sprint duration and user activity. A two-week sprint shows two weeks of work. Longer sprints appear here as well.

![](/wp-content/uploads/tij-gitcloud-backlog-view-activity-timeline.png)

&nbsp;

### Auditing activity

Hover over activity boxes to view sprint changes in a popup. Track issue additions, removals, and status changes. This audit window shows progress and modifications.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Hover over daily activities to see work performed that day.
    </div>
    </div>
</div>

&nbsp;

### Issues

Click **\>** to expand a sprint and view issue activities.

![](/wp-content/uploads/tij-gitcloud-backlog-view-open-item-detail.png)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Hover on issue rows to display the active date period beside the status column.
    </div>
    </div>
</div>

&nbsp;

#### Status column

Hover to view progress status and completion percentage.

<img src='/wp-content/uploads/tij-gitcloud-backlog-view-show-status-detail.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

#### Alert symbols

Hover over <img src='/wp-content/uploads/bbb-alert-20.png' style='margin:0 3px 0 3px;display:inline-block;' /> alert icons to compare calculated versus expected progress. Review remaining sprint time and completed issue count.

<img src='/wp-content/uploads/tij-gitcloud-backlog-view-show-calc-progress-detail.png' style='margin:25px auto;max-width:100%;display:block;' />

In this example, the sprint has two days left with 18% calculated progress, indicating few completed issues.

This view shows whether the sprint is on track or at risk of missing deadlines.

&nbsp;

#### Code diffs

Click **Show diff** to display issues with code changes. Click **Hide diff** to disable.

![](/wp-content/uploads/tij-gitcloud-backlog-view-show-diff.png)

&nbsp;

#### Actions menu

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Requires Jira write permissions.
    </div>
    </div>
</div>

<img src='/wp-content/uploads/tij-gitcloud-backlog-view-actions-menu.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

Click **\[...\]** to open the Actions menu.

| Action | Description |
|:-------|:------------|
| **_Edit_** | Modify sprint settings. |
| **_Start_** | Begin the sprint. Status: <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>IN PROGRESS</b>. |
| **_Finish_** | Complete the sprint. Status: <b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>DONE</b>. |
| **_Move up_** | Increase priority. |
| **_Move down_** | Decrease priority. |
| **_Delete_** | Remove the sprint. |

&nbsp;

### Edit sprint

Click **\[...\]** ➜ **Edit** to modify sprint properties:

<img src='/wp-content/uploads/tij-gitcloud-backlog-view-actions-edit-dlg.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

Modify sprint properties using these fields:

| Field | Description |
|:------|:------------|
| **_Name_** | Sprint name. |
| **_Goal_** | Completion goal for planning. |
| **_Start Date_** | Sprint start for resource planning. |
| **_End Date_** | Sprint deadline for accountability. |
| **_Timeline_** | Drag slider to adjust period. Only end date changes. |

&nbsp;

### Timeline editing

Drag the timeline slider to adjust sprint duration. Only the end date changes.

<img src='/wp-content/uploads/tij-gitcloud-backlog-view-timeline-drag-sel.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

### Sorting and filtering

Use search and sort filters at the top to refine displayed data.

![](/wp-content/uploads/tij-gitcloud-backlog-view-search-panel.png)

Enter text to search for issues. Apply filters to narrow results.

&nbsp;

#### Sprint type filter

![](/wp-content/uploads/tij-gitcloud-backlog-view-search-pane-typel.png)

Select sprint types: active, future, or backlog. The counter shows matches per type.

Click **Apply selection** to apply. Click **Clear** to reset.

&nbsp;

#### Activity filter

![](/wp-content/uploads/tij-gitcloud-backlog-view-search-pane-activity.png)

Select an activity date interval. Default: **All**.

Choose **Custom** for specific dates. Click **Clear** to reset.

&nbsp;

#### Project filter

![](/wp-content/uploads/tij-gitcloud-backlog-view-search-pane-project.png)

Select a project to search. Use the search box when filtering multiple projects.

&nbsp;

#### Assignee filter

Select users to filter by assignee. Default: **All**.

&nbsp;

#### Reset filters

Click **Clear All** to reset all filters.

Click **Search** to apply filters.

&nbsp;

### Column sorting

Click column headers to toggle sort order:

-   **Rank** – List position
-   **Issue Name** – Issue title
-   **Priority** – Priority level
-   **Assignee Name** – Assigned user
-   **Status** – Current state

&nbsp;

### More on Signals features

[Signals for Jira Cloud](/git-integration-for-jira-cloud/Signals-gij-cloud)

[Sprints/Epics View](/git-integration-for-jira-cloud/Signals-general-view-gij-cloud)

[Teams View](/git-integration-for-jira-cloud/Signals-teams-view-gij-cloud)

**Backlog View** (this page)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-Signals-gij-cloud/)

<kbd>Last updated: December 2025</kbd>
