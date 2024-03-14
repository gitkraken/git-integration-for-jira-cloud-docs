---

title: General View (TIJ Cloud)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

![](/wp-content/uploads/tij-gitcloud-general-view-tab-access.png)

The default view for the Team Insights for Jira app is the General View.

You can switch to another view such as General, Teams or Backlog by clicking their specific tabs. In General View, the epics issue list can be enabled by clicking the **Show epics** checkbox on the Issues column header.

Use the search bar together with available search options to filter the list view.

&nbsp;

### Column Information

The list view displays Jira issues showing priority, user activity, and other information:

| Column | Description |
|:-------|:------------|
| **_Issue_** | The Issue column shows the Jira issues that contain user and progress activities.<br><br>Click the **Show epics checkbox** to display the Epics issue types instead. |
| **_Priority_** | Displays the degree of priority of a Jira issue. |
| **_Status_** | Shows the progress status of a Jira issue. |
| **_Assignee_** | Shows the user the Jira issue is currently assigned to. |
| **_Contributors_** | Shows the contributor users actively worked on the Jira issue. |
| **_Sprint_** | Shows the sprint name a Jira issue is included in. |
| **_Days_** | Shows the number of days a Jira issue has been worked on. |
| **_Comments_** | Shows the number of comments a Jira issue has. |
| **_Commits_** | Shows how many commits this task has.<br><div class="bbb-callout bbb--alert"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">If your organization or team requires information be displayed in this column, install the Git Integration for Jira app.</div></div></div> |
| **_Pull requests_** | Shows how many pull requests this task has.<br><div class="bbb-callout bbb--alert"><div class="irow"><div class="ilogobox"><span class="logoimg"></span></div><div class="imsgbox">If your organization or team requires information be displayed in this column, install the Git Integration for Jira app.</div></div></div> |

&nbsp;

### Showing Issue Details

To view more details about a specific Jira issue or Epics, click on the twisty icon (**\>**) to expand it.

![](/wp-content/uploads/tij-gitcloud-general-view-item-details.png)

Click on the Issue details icon to display the detailed dialog of the Jira issue.

<img src='/wp-content/uploads/tij-gitcloud-issue-view-issue-details-dialog.png' style='margin:25px auto;max-width:100%;display:block;' />

The issue details shows the following information on:

*   who the Jira issue is assigned to
*   which Jira issues the current ticket is waiting on
*   which Jira issues is causing the current ticket to stall
*   what is the current status of the Jira issue

&nbsp;

### Sprints view

On the right section of the Issue list is the sprints view which displays the timeline of the sprint. This gives team managers the full picture of the progress of the Jira issues and what’s the next step to do. They will also be able to see which Jira issues that needed attention and identify which team members are overloaded with tasks or which work is at risk for an upcoming due date.

![](/wp-content/uploads/tij-gitcloud-general-view-timeline-labels.png)

The red line indicates today's date. If you drag the timeline scrubber, it changes the Activity date range filter. Hence, it will only show issues that have activity in that time frame. For example, dragging the slider to left lets you take a peek on what was worked on in the past few days or yesterday.

Hover the mouse pointer over the activity bar and it will show details about status changes, and statistics on development changes – for that day. This will display what type of work the team performed on that day.

<img src='/wp-content/uploads/tij-gitcloud-general-view-sprints-section-details.png' style='margin:25px auto;max-width:100%;display:block;' />

Click on the **Go to issue** shortcut to take you directly to that Jira issue.

Scroll the timeline horizontally by using the scrollbar at the bottom. The timeline shows a list of issues based on your selected Issue and Activity filters.

![](/wp-content/uploads/tij-gitcloud-general-view-bottom-scroll-bar-loc.png)

Click on an Issue row to expand child issues and view additional information by moving the mouse pointer over the revealed icons.

![](/wp-content/uploads/tij-gitcloud-issue-view-timeline-row-details.png)

Finally, on the bottom part of the page, you will see the following shortcut controls:

| Control | Description |
|:--------|:------------|
| **_Displayed items_** | Set how many items per page will be displayed in the list view. |
| **_Page navigation_** | Shows the page controls to switch across several pages of information views. |
| **_Today_** | Clicking this button will automatically adjust the slider to today's date. |
| <img src='/wp-content/uploads/gij-question-mark-icon-32.png' style='height:16px;width:auto;' /> |Clicking this button will show quick helpful tips on how to navigate and use the General, Epics, or Teams view. |

&nbsp;

### Epics view mode

Tick the **Show epics** checkbox on the Issue column header to display the list view in Epics mode.

<img src='/wp-content/uploads/tij-gitcloud-general-view-epics-mode.png' style='margin:25px auto;max-width:100%;display:block;' />

The Epics view contains information that helps to organize the rows by epics. This allows team/product managers to easily expand and view the issues within each epic. While it functions closely similar to the General View, it also provides an additional level of organization based on epics.

&nbsp;

### Search Functions and Filters

On the search panel, team/project managers can set the criteria and apply some filters to the search.

![](/wp-content/uploads/tij-gitcloud-teams-view-search-panel.png)

To find and display items in the list that contain a specific word or text, simply enter the desired search term into the search box. This will allow you to easily locate and view relevant items from the list.

&nbsp;

#### Activity filter

![](/wp-content/uploads/tij-gitcloud-teams-view-search-activity-filter.png)

Set **Activity Dates** by choosing the desired interval. Click on the drop-down list to see available intervals which include:

*   All Activity - Last 8 weeks
*   Last 4 weeks
*   Last 2 weeks
*   Last 1 week
*   Custom - Select start date and end date for this filter.

For **Filters**, select if you want to:

*   Show Issues with Jira Activity, and/or
*   Show Issues with Git Activity (requires Git Integration for Jira app installed)

You can select one or both. Click **Apply selection** to accept the selected filters.

For **Contributors**, click on the drop-down list to select one or more members for this filter. The default filter is **All**. Utilize the search box to quickly find the team member that you want to select for this filter. Finally, click **Apply selection** to accept the selected members for the contributors filter.

To reset selection and filter settings click **Clear** on each filter group.

&nbsp;

#### Issue filter

The Issue Filters allows team/project managers to assign available issue filters to the search. Utilize the search box on each filter to quickly find and select one or more categories. If available, click **Apply selection** to accept the selected filters.

| Category filter | Description |
|:----------------|:------------|
| Project | Select one or more projects for the issue filter. |
| Sprints | Click on the sprints filter to view and select one or more sprints.<br><br>Choose No Sprint if you want to see projects that does not have sprints. |
| Statuses | Select one or more statuses for the issue filter. |
| Assignees | Select one or more team members for the issue filter. |
| Labels | Select one or more labels for the issue filter. |
| Issue Types | Select one or more issue type for the issue filter. |
| Versions | Select one or more versions for the issue filter. Displays nothing if no versions are detected. |
| Priorities | Select one or more priority state for the issue filter. |
| Components | Select one or more components for the issue filter. Displays nothing if no components are detected. |

&nbsp;

#### Clear All

To clear all the selected filters and search settings, click **Clear All**. Some selections and search filters are also reset to default.

With all the selection of filters and search options in place, click **Search** to see the results in the list view according to your preference.

&nbsp;

### More on Team Insights for Jira

[Team Insights for Jira main](/git-integration-for-jira-cloud/team-insights-for-jira-gij-cloud)

**General View** (this page)

[Teams View](/git-integration-for-jira-cloud/team-insights-for-jira-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/team-insights-for-jira-backlog-view-gij-cloud/)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-tij-gij-cloud/)

