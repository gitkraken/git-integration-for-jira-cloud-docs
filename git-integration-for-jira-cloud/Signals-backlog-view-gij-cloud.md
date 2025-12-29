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

Backlog View tracks work progress and highlights items needing attention. This page explains how to use Backlog View to monitor sprints and identify risks.

&nbsp;

### Overview

Backlog View helps you identify work risks before deadlines pass. The view organizes issues into sprints for easy tracking.

Use Backlog View to:

*   View Git repository activity during sprint planning
*   Identify at-risk issues and adjust plans
*   Run faster, more effective standups

&nbsp;

### Accessing Backlog View

![](/wp-content/uploads/tij-gitcloud-backlog-view-main-screen.png)

To open Backlog View, click the **Backlog View** tab at the top of the Signals page.

Backlog View groups issues by sprint, similar to Epics mode in General View. Use the Project filter to manage your backlog. Sprints sort by rank when the view loads.

&nbsp;

### Understanding the activity timeline

The activity timeline displays sprint duration and user activity. A two-week sprint shows two weeks of work. Longer sprints display their full duration.

![](/wp-content/uploads/tij-gitcloud-backlog-view-activity-timeline.png)

&nbsp;

### Auditing sprint activity

To view sprint changes, hover over activity boxes. A popup displays issue additions, removals, and status changes. This audit window shows progress and modifications throughout the sprint.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Hover over daily activities to see work performed on each specific day.
    </div>
    </div>
</div>

&nbsp;

### Viewing sprint issues

To expand a sprint and view issue activities, click the expand icon (**\>**).

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

#### Understanding the status column

To view progress status and completion percentage, hover over the status column.

<img src='/wp-content/uploads/tij-gitcloud-backlog-view-show-status-detail.png' style='margin:25px auto;max-width:100%;display:block;' />

&nbsp;

#### Interpreting alert symbols

To compare calculated versus expected progress, hover over <img src='/wp-content/uploads/bbb-alert-20.png' style='margin:0 3px 0 3px;display:inline-block;' /> alert icons. The popup shows remaining sprint time and completed issue count.

<img src='/wp-content/uploads/tij-gitcloud-backlog-view-show-calc-progress-detail.png' style='margin:25px auto;max-width:100%;display:block;' />

In this example, the sprint has two days remaining with 18% calculated progress, indicating few completed issues.

This view helps you determine whether the sprint is on track or at risk of missing deadlines.

&nbsp;

#### Showing code differences

To display issues with code changes, click **Show diff**. To hide code differences, click **Hide diff**.

![](/wp-content/uploads/tij-gitcloud-backlog-view-show-diff.png)

&nbsp;

#### Using the actions menu

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

To access sprint actions, click the menu icon **\[...\]**.

| Action | Description |
|:-------|:------------|
| **Edit** | Opens the dialog to modify sprint settings. |
| **Start** | Begins the sprint. Status changes to: <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>IN PROGRESS</b>. |
| **Finish** | Completes the sprint. Status changes to: <b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>DONE</b>. |
| **Move up** | Increases the sprint's priority ranking. |
| **Move down** | Decreases the sprint's priority ranking. |
| **Delete** | Removes the sprint. |

&nbsp;

### Editing a sprint

To edit sprint properties:

1.  Click **\[...\]** to open the actions menu.
2.  Select **Edit** to open the sprint properties dialog.

<img src='/wp-content/uploads/tij-gitcloud-backlog-view-actions-edit-dlg.png' style='margin:25px auto 35px auto;max-width:100%;display:block;' />

The dialog contains the following fields:

| Field | Description |
|:------|:------------|
| **Name** | The sprint name. |
| **Goal** | The completion goal for planning purposes. |
| **Start Date** | The sprint start date for resource planning. |
| **End Date** | The sprint deadline for accountability. |
| **Timeline** | A slider to adjust the sprint period. Dragging changes only the end date. |

&nbsp;

### Adjusting the timeline

To adjust sprint duration using the timeline slider:

1.  Click and drag the slider to change the period.
2.  Release to set the new end date.

<img src='/wp-content/uploads/tij-gitcloud-backlog-view-timeline-drag-sel.png' style='margin:25px auto;max-width:100%;display:block;' />

Note that dragging the slider changes only the end date, not the start date.

&nbsp;

### Searching and filtering

Use the search and sort filters at the top to refine the displayed data.

![](/wp-content/uploads/tij-gitcloud-backlog-view-search-panel.png)

Enter text to search for issues. Apply filters to narrow results.

&nbsp;

#### Filtering by sprint type

![](/wp-content/uploads/tij-gitcloud-backlog-view-search-pane-typel.png)

Select sprint types to display: active, future, or backlog. The counter shows the number of matches per type.

Click **Apply selection** to apply your choices. Click **Clear** to reset.

&nbsp;

#### Filtering by activity

![](/wp-content/uploads/tij-gitcloud-backlog-view-search-pane-activity.png)

Select an activity date interval. Default: **All**.

Choose **Custom** to specify exact dates. Click **Clear** to reset.

&nbsp;

#### Filtering by project

![](/wp-content/uploads/tij-gitcloud-backlog-view-search-pane-project.png)

Select a project to search within. Use the search box when filtering across multiple projects.

&nbsp;

#### Filtering by assignee

Select users to filter by assignee. Default: **All**.

&nbsp;

#### Resetting filters

To reset all filters, click **Clear All**.

To apply your filter selections and display results, click **Search**.

&nbsp;

### Sorting columns

To change the sort order, click a column header. Click again to toggle between ascending and descending order.

Sortable columns include:

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

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
