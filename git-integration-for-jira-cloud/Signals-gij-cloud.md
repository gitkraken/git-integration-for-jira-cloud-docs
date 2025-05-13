---

title: Signals - GIJ Advanced
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class='embed-container embed-container--16-9'>
    <iframe width='709' height='382' src='https://www.youtube.com/embed/ctzCdY9CXOg' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:12px;margin-bottom:40px;'>
    <i>Right click <a href='https://www.youtube.com/watch?v=ctzCdY9CXOg'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

This extension provides team managers the ability to monitor specific git history and Jira team activity at the project, epic and sprint level. This enables managers to prioritize work, identify risks, reveal trends and make better decisions of managing Jira team workflows and activities.

![](/wp-content/uploads/tij-gitcloud-main-default-view-general-tab.png)

Team Insights for Jira (TIJ) grants managers a complete view of what your team is working on and its progress. Managers can easily identify items at-risk based on team activity and progress.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If you have Git Integration for Jira Cloud installed, it can enhance your planning workflow and provide more information by integrating Git data into your views.
    </div>
    </div>
</div>

&nbsp;

### Installation

Starting February 11, 2025, the Team Insights for Jra Cloud app extension is merged with Git Integration for Jira Cloud app.

Go to the Atlassian Marketplace then search for "[Git Integration for Jira by GitKraken" (GIJ) app](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud).

![](/wp-content/uploads/gij-gitcloud-new-installation-trial-buy-c.png)

Click **Try it free** and start the free trial for 30 days.

![](/wp-content/uploads/gij-gitcloud-try-new-git-for-jira-cloud-app-c.png)

Login to your Jira account, if required, to proceed installation of the app. See [Git Integration for Jira Cloud pricing and subscription tiers](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=pricing) for more information. The license key is automatically configured into the app configuration for free trial licenses.

After the installation is complete, you will see the following message box:

![](/wp-content/uploads/gij-gitcloud-installation-success-msg-balloon-c.png)

*   Click **Get started** to take you to the Manage integrations page where you can configure and integrate your git repositories.

*   Click **Manage app** to take you to the Manage apps page where you can manage your installed Jira apps and view the Git Integration for Jira app properties, version and license information.

This completes the installation for Git Integration for Jira app with Team Insights for Jira extension.

&nbsp;

### Migration of Standalone TIJ Cloud data to GIJ\+TIJ Cloud

#### Are there any special steps to migrate TIJ Cloud standalone to the merged GIJ+TIJ Cloud app? Any installation requirements?

No, there are no additional steps or installation requirements needed. The TIJ standalone data migration is automatic.

#### Does the TIJ extension becomes inaccessible when the GIJ app expires?

No. The TIJ extension acts as a separate module and your TIJ data is not affected and remains accessible.

&nbsp;

### Feature matrix

With Team Insights for Jira app, team managers will be able to see team activity across projects, epics and sprints.

| Feature   | TIJ Only  | GIJ + TIJ |
|:----------|:----------|:----------|
| Identify stale issues or issues that revert in status | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| See activities for sprint planning, stand ups, and retrospectives<sup>1</sup> | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Helpful insights for executives, managers, and individual contributors<sup>1</sup> | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Enables all team members to identify and contribute improvements | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Valuable for all departments that use Jira in your organization | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Easily see issues status progress over time, where it changed and how long it remained in that state | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Identify pull requests that remain open for too long<sup>2</sup> | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| View commits and other git related data for your team. | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Create branches and pull/merge requests in Jira issues for your team | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Link webhooks to your Git and Jira for faster display of git data | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Manage git integrations and repository connections | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| Assign other users to manage integrations and repository connections | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |

<b><sup>1</sup></b> With Git Integration for Jira app also installed, git data is displayed in a more detailed manner

<b><sup>2</sup></b> Requires Git Integration for Jira app installed if you want to see pull request status and information.

&nbsp;

### Permissions

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IMPORTANT!</b>

Viewing Team Insights for Jira data is derived from the Jira user permissions they are assigned with. Thus, if users have access to Jira issues, they will also be able to view TIJ data.

&nbsp;

### Extension access location

![](/wp-content/uploads/tij-gitcloud-menu-access-location.png)

Once you have successfully installed the application, you will be able to access the Team Insights for Jira extension via the Jira dashboard menu. Simply navigate to Apps ➜ **Git Integration: Team Insights**.

&nbsp;

### Feature highlights

Team Insights for Jira provides you with the ability to view Git activity across all of your projects and issues. These features allow you to gain valuable insights into the collaboration and development process within your team. And best of all, it's completely free!

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        By analyzing the Git activity, you can identify trends, track progress, and make data-driven decisions to improve productivity and efficiency.
    </div>
    </div>
</div>

&nbsp;

#### Customize Your View Across Projects, Epics, and Sprints

Team Insights for Jira aims to improve your workflows and provide you with the data you need to put you on the right track. View the timeline by Epics, Issues and Sub-tasks and filter by project, sprint, team members, issue status, and more. When managing your tasks, it's important to have the ability to sort them based on different criteria. For example, you can sort tasks by the number of days since the last status update or by the number of commits made.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        By utilizing these sorting options, you can gain valuable insights into your workflow. This can help you prioritize and stay organized.
    </div>
    </div>
</div>

&nbsp;

#### Manage Jira Workflows Efficiently

Focus on the Jira issues that demand immediate attention. Gain insight into actions performed by users and their timing across multiple Jira issues. Easily determine tasks that are at risk of missing upcoming deadlines, identify team members that have an excessive workload in a more detailed view. Pinpoint stagnant problems, reverted closed issues, and pull requests that remain open for an extended period of time.

&nbsp;

#### Enhance Team Collaboration with TIJ Views

Enable every team member and all departments to enhance their understanding by utilizing TIJ views during sprint, epic, and backlog planning. When analyzing data, individuals can identify recurring patterns, detect trends, and uncover potential areas for improvement. This process helps them understand the whole situation beforehand.

&nbsp;

#### Track and Improve Team Productivity

Team Insights for Jira provides a comprehensive view of your team's Jira and Git activity over time. It allows you to easily track what tasks your team is currently working on and monitor their progress, thus impacting on productivity and efficiency.

TIJ displays Jira activity for all Jira users. Git data such as branches, commits, pull requests, and tags are automatically included in the views if you have the [Git Integration for Jira](https://www.gitkraken.com/git-integration-for-jira) app installed.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This combination is ideal for team workflows and git integration without requiring any additional setup or configuration.
    </div>
    </div>
</div>

&nbsp;

### More on Team Insights for Jira features

**Team Insights for Jira Cloud** (this page)

[General View](/git-integration-for-jira-cloud/team-insights-for-jira-general-view-gij-cloud/)

[Teams View](/git-integration-for-jira-cloud/team-insights-for-jira-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/team-insights-for-jira-backlog-view-gij-cloud/)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-tij-gij-cloud/)


