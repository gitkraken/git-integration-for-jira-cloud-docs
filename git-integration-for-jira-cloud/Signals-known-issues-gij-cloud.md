---

title: Known Issues for Signals
description: Review known issues and workarounds for the Signals feature in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud

---

Signals provides features for team leaders and project leads. However, some known issues may occur.

Known issues and workarounds:

- [Users are removed from search list as you type in the search text box](#users-are-removed-from-search-list-as-you-type-in-the-search-text-box)
- [Text search for issue key in backlog page not returning the desired Jira issue](#text-search-for-issue-key-in-backlog-page-not-returning-the-desired-jira-issue)
- [More on Signals features](#more-on-Signals-features)

<div id="users-are-removed-from-search-list"></div>

### Users are removed from search list as you type in the search text box

When searching for a user through a filter (contributor or assignee), typing more than a few characters may cause search results to disappear.

For example, if the search text is two characters or less, a user’s name is displayed correctly and appears in the recommended list and search results. However, when you type more than 3 characters of that name, it is no longer shown in the list.

On the other hand, searching by last name appears to work as expected and shows the correct search result.

This issue will be fixed in a future version.

### Text search for issue key in backlog page not returning the desired Jira issue

The Backlog view may not display the desired Jira issue due to slow data loading. This tradeoff allows users to see all Jira issues in the Backlog view.

**Workaround:** Search by issue summary using wildcards:

![](/wp-content/uploads/tij-gitcloud-search-list-example.png)

You can also search by issue key. Specify a valid Jira issue key to avoid errors. This approach does not support wildcards:

![](/wp-content/uploads/tij-gitcloud-search-supports-jql-example.png)

![](/wp-content/uploads/tij-gitcloud-search-error-example-01.png)

&nbsp;

### More on Signals features

[General View](/git-integration-for-jira-cloud/Signals-general-view-gij-cloud)

[Teams View](/git-integration-for-jira-cloud/Signals-teams-view-gij-cloud)

[Backlog View](/git-integration-for-jira-cloud/Signals-backlog-view-gij-cloud)

[Pull request timeline reindex](/git-integration-for-jira-cloud/pull-request-timeline-for-Signals-gij-cloud)

<kbd>Last updated: December 2025</kbd>
