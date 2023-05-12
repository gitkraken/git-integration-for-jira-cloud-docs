---

title: Jira issue page
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

If the Git Integration for Jira app is configured and licensed successfully, new tabs are added to each Jira issue.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Some features can be switched on and off via <a href='/git-integration-for-jira-cloud/general-settings-gij-cloud'>General settings</a>):<br>
        <ul style='margin-bottom:0px;'>
            <li>Jira dashboard menu Apps ➜ Git Integration: Repository browser/Git Integration: Manage Git repositories ➜ <b>General settings</b> (sidebar).</li>
        </ul>
    </div>
    </div>
</div>

Also, users should be able to see available features in the Jira issue page, namely:

*   Git Commits tab
*   Git Roll Up tab
*   Git Development panel
*   Git Integration panel

![](/wp-content/uploads/gij-gitcloud-jira-issue-page-view-sel.png)

<img src='/wp-content/uploads/gij-gitcloud-jira-issue-git-idev-panel-view-new.png' style='margin:25px auto;max-width:100%;display:block;' />

**1\. Git Commits**<br>
In this tab, service users will be able to see commit information such as commit author, changes to source files, as well as viewing the full commit that are associated to the current issue.

**2\. Git Roll Up**<br>
In this tab, service users will be able to see commit statistics, diff and referenced Jira issues.

**3\. Jira Development panel**<br>
The Jira Development Panel is located on the right panel of the Jira issue page. In most cases, this panel is intended for developers. This is also a shortcut to viewing list of branches, commits and pull/merge requests.

**4\. Git Integration panel**  <br>Click to open the Git integration panel and allows service users to create branches and pull/merge requests for selected repositories inside Jira.

**5\. Commit counter**<br>
This section contains git commits counter and shortcuts to Git Commits and Git Roll Up tabs.

**6\. Branches**<br>
This feature allows service users to create git branches against the specified repository from inside Jira. The created branches are also displayed as a list. 

**7\. Ahead and Behind**<br>
Represents the number of commits that are ahead/behind the main branch.

**8\.Deep links**<br>
These are the deep link shortcuts to view the selected branch in your git host service or in GitKraken git client app.

**9\. Pull/Merge Requests**<br>
This feature allows service users to create pull/merge request against the specified repository from inside Jira. The created pull/merge requests are also displayed as a list.

**10\. Git tags**<br>
This section lists available git tags from the connected git repositories. Use the git shortcut icons on the right to open git tags in your git host service, GitKraken git client app or GitLens VSCode extension.

&nbsp;
* * *

[**Prev:** Jira user information card](/git-integration-for-jira-cloud/jira-user-information-card-gij-cloud)

[**Next:** Git Roll Up tab](/git-integration-for-jira-cloud/git-roll-up-tab-gij-cloud/)

