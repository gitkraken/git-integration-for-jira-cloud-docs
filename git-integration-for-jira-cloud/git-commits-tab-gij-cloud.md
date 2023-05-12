---

title: Git Commits tab
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

The Git Commits tab shows commit information such as commit authors, date of commit, commit messages, access to view code diffs, commit id and view full commit.

![](/wp-content/uploads/gij-gitcloud-jira-issue-git-commits-tab-chart.png)


Open an issue then go to the _**Git Commits**_ tab to view commit information:

| Pointer | Information | Description |
| :---: | :--- | :--- |
| **1** | **Repository/Indexed** | Name of the repository _(as in app config)_ and date of last synchronization with remote repository. |
| **2** | **Author/Committer** | User who performed the commit. Hover the mouse pointer on the name to view user card. |
| **3** | **Issue key/Commit message** | This is the Jira issue with the corresponding commit message. |
| **4** | **Repository name/Branch** | This is the name of the repository and the branch where the commit has been made. |
| **5** | **Commit UID** | UID of the commit and git host link. Click the UID to view the code diffs for this commit. Click the git host link to view this commit via the git host server. |
| **6** | **Commit counter indicators** | ![Git commit traffic light example](/wp-content/uploads/gij-traffic-light-example.png)<br><br>The traffic light indicator shows the added/modified/deleted lines from the file code diffs. |
| **7** | **Click the commit ID to view the commit code diff. Click the copy icon to copy the commit code diff to the system clipboard. |
| **8** | **Open in GitKraken** | Opens this commit in the GitKraken git client app. |
| **9** | **Open in GitLens** | Opens this commit in the GitLens extension via VSCode app. |
| **10** | **Files changed** | List of files affected by the commit. Click the file or git host link to view code diff of this commit. |
| **11** | **Web links** | These are clickable web links that will open the selected file code diff directly to git host service portal in a new browser window/tab. |

&nbsp;

View the whole commit code diff information by clicking the **View full commit** button to the right of the commit message.

View code diff information of the particular file by clicking the filename for each file adjacent to the rollup counter markers.

&nbsp;
* * *

[**Prev:** Git roll up tab](/git-integration-for-jira-cloud/git-roll-up-tab-gij-cloud)

[**Next:** Jira Git integration development panel](/git-integration-for-jira-cloud/jira-git-integration-development-panel-gij-cloud/)

