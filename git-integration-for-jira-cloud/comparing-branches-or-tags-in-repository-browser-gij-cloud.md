---

title: Comparing branches or tags in Repository browser
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

On the Repository browser (_Jira dashboard ➜ Apps menu ➜ **Git Integration: Repository browser**_), click the **Compare** page tab.

On this page, two branches from the current repository can be compared.

A diff between the _**base**_ branch and the _**compare**_ branch is displayed:

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-compare-view.png)

To view desired results, use the following selection scenarios:

*   select **master** as compare; select the most recent branch as base.

*   select **master** as compare; select a tag with a version release.

*   select different branches as base and compare. (Example: `TYT-212` against `TYT-316`)

![](/wp-content/uploads/gij-gitcloud-repo-browser-compare-view-swap.png)

Click **…** to swap the base and the compare selection.

The **Summary** page displays the _**Commits**_, _**Aggregated Lines by Developers**_ and _**Files**_. Click on a file to view its code diff.

Click **Commits** on the sidebar to view the list of commits resulting from this compare. The adjacent figure indicates the number of commits associated to this compare.

Click **Diff** on the sidebar to view code diffs of the selected range of commits with the path and name of the affected files.

![](/wp-content/uploads/gij-gitcloud-repo-browser-page-compare-isues-view.png)

Click **Issues** on the sidebar to view list of unique Jira issues related to commits.

On the **Issues** page, clicking the **View in issue navigator** label will open the search page with passed query of a list of Jira issues found based from the compare criteria.

&nbsp;
* * *

[**Prev:** Viewing list of commits in Repository browser](/git-integration-for-jira-cloud/viewing-list-of-commits-in-repository-browser-gij-cloud/)

[**Next:** Repository browser general settings](/git-integration-for-jira-cloud/repository-browser-general-settings-gij-cloud/)

