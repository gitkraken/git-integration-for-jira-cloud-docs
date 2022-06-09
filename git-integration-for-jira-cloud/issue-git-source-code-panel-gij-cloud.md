---

title: Issue Git Source Code Panel
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Note

*   By default, [Git Integration for Jira](https://marketplace.atlassian.com/4984) has the Git Source Code Panel enabled. ([How to disable](/git-integration-for-jira-cloud/issue-git-source-code-panel/))
*   By default, [Dev Info for Jira](https://marketplace.atlassian.com/1219270) has the Git Source Code Panel disabled. ([How to enable](/git-integration-for-jira-cloud/issue-git-source-code-panel/))



The **View developer tools** _permission_ is required to view the Git Source Code Panel. Jira users must also have the **Browse Project** _permissions_ to a project associated with a repository to view.


* * *



## **Introduction**

The Issue Git Source Code Panel displays:

*   Git Commits: # of commits and link to [Git Commits Issue Tab](/git-integration-for-jira-cloud/git-commits-issue-tab-and-project-page/), link to [Git Roll Up Issue Tab](/git-integration-for-jira-cloud/git-roll-up-issue-tab/)
*   Branches: Create branch function, list of branches associated to Jira issue (Jira issue key must be in branch title)
*   Pull/Merge Requests:  Create pull/merge request function, list of pull/merge requests associated to Jira issue (Jira issue key must be in PR/MR title), status of pull/merge request
*   Tags: git tags associated to Jira issue (via associated commit). Tags are sometimes referred to as Releases in some products.



**Git Source Code Panel (old issue view)**

**![](https://bigbrassband.atlassian.net/wiki/download/attachments/138346503/git-cloud-oldview-source-code-panel.png?version=1&modificationDate=1561742276535&cacheVersion=1&api=v2)**



**Git Source Code Panel (New issue view & next-gen projects)**

The Git Commits Issue tab lists the git commits associated to the Jira issue grouped by repository and sorted by commit time. 

![](https://bigbrassband.atlassian.net/wiki/download/attachments/138346503/git-cloud-newview-source-code-panel.png?version=1&modificationDate=1561741816923&cacheVersion=1&api=v2)

## How can a Jira administrator enable or disable the Issue Git Source Code Panel?

1.  Install the [Git Integration for Jira](https://marketplace.atlassian.com/4984) or the [Dev Info for Jira](https://marketplace.atlassian.com/1219270) app
2.  Navigate to the **General settings** page of the application
3.  Enable or disable the setting: Show Git Source Code Panel
4.  Click **Update** button

![](https://bigbrassband.atlassian.net/wiki/download/attachments/138346503/gitcloud-general-settings-git-source-code-panel.png?version=1&modificationDate=1561742705018&cacheVersion=1&api=v2)

For detailed information about this feature, see [Documentation: Jira Git integration development panel](/git-integration-for-jira-cloud/jira-git-integration-development-panel-gij-cloud).

Contact Us

If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com)