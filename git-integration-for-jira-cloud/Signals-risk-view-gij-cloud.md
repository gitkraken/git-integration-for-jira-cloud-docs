---

title: Signals Risk View Settings
description: Configure risk thresholds and severity levels for sprints, issues, and pull requests in Signals to identify potential project risks.
taxonomy:
    category: git-integration-for-jira-cloud

---

Risks highlight sprints or issues not progressing as expected, drawing attention to potential delays. Managers can activate or deactivate risks based on project status. Each risk has a severity level indicating project impact.

When issues or sprints reach predefined thresholds, visual alerts appear on the timeline showing risk severity. Use these alerts to assess, classify, and prioritize potential impacts.

Configure Risk View Settings to highlight risks requiring immediate attention.

&nbsp;

### Sprint risks

![](/wp-content/uploads/tij-gitcloud-risk-settings-sprint-cfg.png)

Monitor sprint risks: approaching deadlines, behind-schedule progress, scope changes, overdue sprints, and pending sprints past start date.

Set severity levels using the dropdown.

#### Sprint end date approaching with incomplete issues

<p style='padding-left:30px;'>Alert when sprint ends in fewer than <b># days</b> with more than <b>#%</b> issues incomplete.</p>

#### Sprint progress behind schedule

<p style='padding-left:30px;'>Alert when progress<sup>1</sup> falls <b># percentage points</b> below expected.</p>

<p style='padding-left:30px;'><sup>1</sup> <i>Expected progress = completed issues ÷ total issues ÷ sprint duration. A 14-day sprint with 14 issues expects 1 completed issue per day.</i></p>

#### Sprint scope changed

<p style='padding-left:30px;'>Alert when issues are added or removed<sup>2</sup> after sprint start.</p>

<p style='padding-left:30px;'><sup>2</sup> <i>Triggers when sprint scope changes post-start.</i></p>

#### Completed sprint with in-progress issues

<p style='padding-left:30px;'>Alert when completed sprints contain in-progress issues.</p>

#### Sprint active past end date

<p style='padding-left:30px;'>Alert when sprints remain active past due date.</p>

#### Sprint not started past start date

<p style='padding-left:30px;'>Alert when sprints have not started and start date has passed.</p>

&nbsp;

### Issue risks

![](/wp-content/uploads/tij-gitcloud-risk-settings-issues-cfg.png)

Monitor issue risks: inactivity, missing assignees, or excessive logged hours.

Set severity levels using the dropdown.

#### Stagnant issue (no activity)

<p style='padding-left:30px;'>Alert when issues have no activity for <b># days</b>.</p>

#### Stagnant issue (no status change)

<p style='padding-left:30px;'>Alert when issues have no status change for <b># days</b>.</p>

#### Unassigned issue

<p style='padding-left:30px;'>Alert when issues have no assignee for <b># days</b>.</p>

#### Excessive logged time

<p style='padding-left:30px;'>Alert when logged time exceeds <b># hours</b>.</p>

&nbsp;

### Pull request risks

![](/wp-content/uploads/tij-gitcloud-risk-settings-pull-request-cfg.png)

#### Inactive pull request

<p style='padding-left:30px;'>Alert when pull requests have no activity for <b># days</b>.</p>

&nbsp;

### More on Signals

[Signals](/git-integration-for-jira-cloud/Signals-gij-cloud)

[General View](/git-integration-for-jira-cloud/Signals-general-view-gij-cloud)

[Teams View](/git-integration-for-jira-cloud/Signals-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/Signals-backlog-view-gij-cloud)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-Signals-gij-cloud)

<kbd>Last updated: December 2025</kbd>
