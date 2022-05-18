---

title: Comparing branches or tags in Repository browser
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
On the Repository browser (_Jira dashboard ➜ Apps menu ➜ **Git Integration: Repository browser**_), click the **Compare** page tab.

On this page, two branches from the current repository can be compared.

A diff between the _**base**_ branch and the _**compare**_ branch is displayed:

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025590/gitcloud-repo-browser-page-compare-view.png?version=1&modificationDate=1650263701274&cacheVersion=1&api=v2)

To view desired results, use the following selection scenarios:

*   select **master** as compare; select the most recent branch as base.

*   select **master** as compare; select a tag with a version release.

*   select different branches as base and compare. (Example: `TYT-212` against `TYT-316`)


Click **…** to swap the base and the compare selection.

The **Summary** page displays the _**Commits**_, _**Aggregated Lines by Developers**_ and _**Files**_. Click on a file to view its code diff.

Click **Commits** on the sidebar to view the list of commits resulting from this compare. The adjacent figure indicates the number of commits associated to this compare.

Click **Diff** on the sidebar to view code diffs of the selected range of commits with the path and name of the affected files.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025590/gitcloud-repo-browser-page-compare-isues-view.png?version=1&modificationDate=1650263827433&cacheVersion=1&api=v2&width=680&height=249)

Click **Issues** on the sidebar to view list of unique Jira issues related to commits.

On the **Issues** page, clicking the **View in issue navigator** label will open the search page with passed query of a list of Jira issues found based from the compare criteria.

[« Viewing list of commits in Repository browser](/wiki/spaces/GITCLOUD/pages/1923025571/Viewing+list+of+commits+in+Repository+browser)

[Enable/disable Repository browser via git repository configuration page »](/wiki/spaces/GITCLOUD/pages/1923025615/Repository+browser+general+settings)

### More related topics about repository browser

*   Page:

    [Repository browser](/wiki/spaces/GITCLOUD/pages/1923025500/Repository+browser) (Git Integration for Jira Cloud)

*   Page:

    [Viewing list of commits in Repository browser](/wiki/spaces/GITCLOUD/pages/1923025571/Viewing+list+of+commits+in+Repository+browser) (Git Integration for Jira Cloud)

*   Page:

    [Comparing branches or tags in Repository browser](/wiki/spaces/GITCLOUD/pages/1923025590/Comparing+branches+or+tags+in+Repository+browser) (Git Integration for Jira Cloud)

*   Page:

    [Repository browser general settings](/wiki/spaces/GITCLOUD/pages/1923025615/Repository+browser+general+settings) (Git Integration for Jira Cloud)