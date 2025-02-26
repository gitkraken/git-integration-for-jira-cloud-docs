---

title: Risk View Settings (TIJ Cloud)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Risks play a critical role in highlighting sprints or issues that may not be progressing as anticipated. It draws attention to potential problems or delays in the project timeline. These risks can be individually tracked, which enables project managers to either activate or deactivate them based on the project's evolving status. Furthermore, each risk can be assigned a severity level. This allows for a more distinct understanding of the impact each risk may have on the overall project.

When an issue or sprint reaches a predefined risk threshold, a visual alert is automatically triggered on the project timeline. This indicator marks the presence of a risk and its severity. Thus, team managers can assess, classify and prioritize the urgency of the potential impact and the severity of the risk.

Overall, the Risk View Settings helps prioritize which risks require immediate attention and resources to mitigate, ensuring the project stays on track.

&nbsp;

### Sprint Risk Settings

![](/wp-content/uploads/tij-gitcloud-risk-settings-sprint-cfg.png)

Get notified about potential sprint risks, including approaching deadlines with unresolved issues, progress that are behind the schedule, scope changes, overdue sprints, and pending sprints past their start date. Help and improve your team to stay on track and address potential challenges.

To set the severity level for each setting, use the provided dropdown control.

#### Sprint end date is less than # days away and more than #% of issues are not Done

<p style='padding-left:30px;'>Get visual notifications if the end date of the sprint is less than the defined <b>number of days</b>; and <b>how much percentage</b> (max 100%) of the issues that are still in an incomplete state.</p>

#### Sprint progress is # percentage points lower than expected

<p style='padding-left:30px;'>See visual cues if the sprint progress<sup>1</sup> is lower than the defined <b>number of percentage points</b>.</p>

<p style='padding-left:30px;'><sup>1</sup> <i>The expected progress calculation is based on completed issues, total number of issues and the sprint duration. For example, for a two-week sprint (14 days) with 14 issues -- the expected progress would be 1 issue in the Done status per day.</i></p>

#### Sprint scope has been changed

<p style='padding-left:30px;'>Get visual alerts if the sprint scope has changed<sup>2</sup> at any point from when it started.</p>

<p style='padding-left:30px;'><sup>2</sup> <i>Indicates an issue was added or removed from the sprint at any point after it was started.</i></p>

#### Sprint is completed, but contains issues that are in progress

<p style='padding-left:30px;'>See visual warnings for completed sprints which contains issues that are still in progress.</p>

#### Sprint is active beyond its end date

<p style='padding-left:30px;'>Get visual notifications if a sprint is still active past its due date.</p>

#### Sprint has not been started and its start date is in the past

<p style='padding-left:30px;'>See visual alerts if a sprint has not been started for a long time.</p>

&nbsp;

### Issues Risk Settings

![](/wp-content/uploads/tij-gitcloud-risk-settings-issues-cfg.png)

Get notified when issues remain inactive for a set period, lack an assignee, or exceed expected work hours, helping maintain workflow efficiency and accountability.

To set the severity level for each setting, use the provided dropdown control.

#### Issue is stagnant (no activity) for # days from last activity

<p style='padding-left:30px;'>See visual notifications when an issue is inactive for the defined <b>number of days</b>.</p>

#### Issue is stagnant (no activity) for # days from the last status change

<p style='padding-left:30px;'>Get visual cues when an issue is inactive for the defined <b>number of days</b> from the last time its status was changed.</p>

#### No assignee for # days

<p style='padding-left:30px;'>See visual alerts if an issue has no assigned user for a defined <b>number of days</b>.</p>

#### More than # hours work of time logged

<p style='padding-left:30px;'>Get visual notifications if an issue has exceeded the defined <b>number of time logged</b> for work in hours.</p>

&nbsp;

### Pull Request Risk Settings

![](/wp-content/uploads/tij-gitcloud-risk-settings-pull-request-cfg.png)

#### No activity on PR # days since last activity

<p style='padding-left:30px;'>See visual representation alerts for pull requests that have been inactive for a defined <b>number of days</b> since the last activity.</p>

&nbsp;

### More on Team Insights for Jira Cloud

[Team Insights for Jira main](/git-integration-for-jira-cloud/team-insights-for-jira-gij-cloud)

[General View](/git-integration-for-jira-cloud/team-insights-for-jira-general-view-gij-cloud/)

[Teams View](/git-integration-for-jira-cloud/team-insights-for-jira-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/team-insights-for-jira-backlog-view-gij-cloud/)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-tij-gij-cloud/)

**Risk View Settings** (this page)

