---

title: General View (Signals)
description: Learn how to use the General View in Signals to monitor Jira issues, track activity timelines, and filter by projects, sprints, and team members.
taxonomy:
    category: git-integration-for-jira-cloud

---

![](/wp-content/uploads/tij-gitcloud-general-view-tab-access.png)

General View is the default Signals view.

Click tabs to switch between General, Teams, or Backlog views. Select **Show epics** on the Issues column header to display epics instead of issues.

Use the search bar to filter results.

&nbsp;

### Column information

The list view displays Jira issues with the following columns:

| Column | Description |
|:-------|:------------|
| **_Issue_** | Jira issues with user and progress activities. Select **Show epics** to display Epics instead. |
| **_Priority_** | Issue priority level. |
| **_Status_** | Issue progress status. |
| **_Assignee_** | Assigned user. |
| **_Contributors_** | Users who worked on the issue. |
| **_Sprint_** | Sprint containing this issue. |
| **_Days_** | Days worked on the issue. |
| **_Comments_** | Comment count. |
| **_Commits_** | Commit count.<br><div class="bbb-callout bbb--alert"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">Requires Git Integration for Jira.</div></div></div> |
| **_Pull requests_** | Pull request count.<br><div class="bbb-callout bbb--alert"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">Requires Git Integration for Jira.</div></div></div> |

&nbsp;

### Issue details

Click the expand icon (**\>**) to view issue or Epic details.

![](/wp-content/uploads/tij-gitcloud-general-view-item-details.png)

Click the Issue details icon to open the issue dialog.

<img src='/wp-content/uploads/tij-gitcloud-issue-view-issue-details-dialog.png' style='margin:25px auto;max-width:100%;display:block;' />

The dialog displays:

*   Assigned user
*   Blocking issues
*   Issues causing stalls
*   Current status

&nbsp;

### Sprint timeline

The right section shows the sprint timeline. This view reveals issue progress and helps identify issues needing attention, overloaded team members, and at-risk work.

![](/wp-content/uploads/tij-gitcloud-general-view-timeline-labels.png)

The red line marks today's date. Drag the timeline scrubber to change the Activity date range. Only issues with activity in that range appear.

Hover over activity bars to see status changes and development statistics for that day.

<img src='/wp-content/uploads/tij-gitcloud-general-view-sprints-section-details.png' style='margin:25px auto;max-width:100%;display:block;' />

Click **Go to issue** to open that Jira issue.

Scroll the timeline horizontally using the bottom scrollbar. Results reflect your selected filters.

![](/wp-content/uploads/tij-gitcloud-general-view-bottom-scroll-bar-loc.png)

Click an Issue row to expand child issues. Hover over icons for details.

![](/wp-content/uploads/tij-gitcloud-issue-view-timeline-row-details.png)

Controls at the page bottom:

| Control | Description |
|:--------|:------------|
| **_Displayed items_** | Items per page. |
| **_Page navigation_** | Page switching. |
| **_Today_** | Jump to today's date. |
| <img src='/wp-content/uploads/gij-question-mark-icon-32.png' style='height:16px;width:auto;' /> | Navigation tips. |

&nbsp;

### Epics view mode

Select **Show epics** on the Issue column header to switch to Epics mode.

<img src='/wp-content/uploads/tij-gticloud-general-view-epics-mode.png' style='margin:25px auto;max-width:100%;display:block;' />

Epics mode groups rows by epic. Expand each epic to view its issues. This mode works like General View but organizes content by epic.

&nbsp;

### Search and filters

Use the search panel to set criteria and filter results.

![](/wp-content/uploads/tij-gitcloud-teams-view-search-panel.png)

Enter terms in the search box to find matching items.

&nbsp;

#### Activity filter

![](/wp-content/uploads/tij-gitcloud-teams-view-search-activity-filter.png)

Set **Activity Dates** from the drop-down:

*   All Activity - Last 8 weeks
*   Last 4 weeks
*   Last 2 weeks
*   Last 1 week
*   Custom - Set specific start and end dates

For **Filters**, select options:

*   Show Issues with Jira Activity
*   Show Issues with Git Activity (requires Git Integration for Jira)

Click **Apply selection** to apply.

For **Contributors**, select members from the drop-down. Default: **All**. Use the search box to locate specific members. Click **Apply selection** to apply.

Click **Clear** to reset each filter group.

&nbsp;

#### Issue filter

Narrow results with issue filters. Use search boxes to locate categories. Click **Apply selection** to apply.

| Category filter | Description |
|:----------------|:------------|
| Project | One or more projects. |
| Sprints | One or more sprints. Select **No Sprint** for unassigned issues. |
| Statuses | One or more statuses. |
| Assignees | One or more team members. |
| Labels | One or more labels. |
| Issue Types | One or more issue types. |
| Versions | One or more versions. |
| Priorities | One or more priority levels. |
| Components | One or more components. |

&nbsp;

#### Reset filters

Click **Clear All** to reset all filters to defaults.

Click **Search** to apply filters and display results.

&nbsp;

### More on Signals

[Signals](/git-integration-for-jira-cloud/Signals-gij-cloud)

[Teams View](/git-integration-for-jira-cloud/Signals-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/Signals-teams-view-gij-cloud)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-Signals-gij-cloud)

<kbd>Last updated: December 2025</kbd>
