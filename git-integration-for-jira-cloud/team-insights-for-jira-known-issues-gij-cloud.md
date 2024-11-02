---

title: Known Issues TIJ Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

he Team Insights for Jira app extension is equipped with a wide range of features designed to elevate the work of team leaders and project leads, making their tasks significantly more manageable. However, due to the wide array of hardware configurations, these excellent features can sometimes be encumbered by various issues.

Below are the known issues and workarounds related to Team Insights for Jira app extension:

- [Users are removed from search list as you type in the search text box](#users-are-removed-from-search-list-as-you-type-in-the-search-text-box)
- [Text search for issue key in backlog page not returning the desired Jira issue](#text-search-for-issue-key-in-backlog-page-not-returning-the-desired-jira-issue)
- [More on Team Insights for Jira features](#more-on-team-insights-for-jira-features)

<div id="users-are-removed-from-search-list">

### Users are removed from search list as you type in the search text box

When doing a search query for a user through a search filter (contributor or assignee), typing a search text past a certain number of characters will cause the search result items to disappear.

For example, if the search text is two characters or less, a user’s name is displayed correctly and appears in the recommended list and search results. However, when you type more than 3 characters of that name, it is no longer shown in the list.

On the other hand, searching by last name appears to work as expected and shows the correct search result.

Please expect that this issue will be fixed in the future version of the extension.

### Text search for issue key in backlog page not returning the desired Jira issue

Sometimes, the Backlog view does not display the desired Jira issue. This is because of the known slow performance of loading data into the view. However, as a tradeoff, this allowed users to see all Jira issues on the Backlog view.

For example, you can use the search field to find Jira issues by summary. This approach supports wildcards. See below:

![](/wp-content/uploads/tij-gitcloud-search-list-example.png)

You can also do a search by issue key. Make sure to specify a valid Jira issue key or you'll get errors. Take note that this approach does not support wildcards. See example below:

![](/wp-content/uploads/tij-gitcloud-search-supports-jql-example.png)

![](/wp-content/uploads/tij-gitcloud-search-error-example-01.png)

&nbsp;

### More on Team Insights for Jira features

**Team Insights for Jira Cloud** (this page)

[General View](/git-integration-for-jira-cloud/team-insights-for-jira-general-view-gij-cloud/)

[Teams View](/git-integration-for-jira-cloud/team-insights-for-jira-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/team-insights-for-jira-backlog-view-gij-cloud/)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-tij-gij-cloud/)


