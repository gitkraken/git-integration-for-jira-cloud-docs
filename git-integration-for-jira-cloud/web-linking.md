---

title: Web linking
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

OPTIONAL

The web linking feature adds links to your git hosting provider directly into the _**Git Commits**_ tab. Configure web linking options while editing **repository settings** (![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ _Edit integration_ | ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) _Actions_ ➜ _Edit repository_) so that commits can include links to the git host pages.

The Git Integration for Jira Cloud app automatically configures web links for most git hosts via Git service integration panel.

For single git repository integration, web link setup is optional. However, git links will become available in Git Commits tab when configured.

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/qmumdo048n) _to open this video in a new browser tab for more viewing options._
_(Updated video coming soon)_


The following providers are supported:

*   **cgit**

*   **Fisheye**

*   **GitHub**

*   **Gitorious**

*   **gitweb**

*   **Beanstalk**

*   **CloudForge**

*   **Atlassian Stash**

*   **GitLab**

*   **TFS (starting v2013)**

*   **Azure Server**

*   **VSTS**

*   **Azure DevOps**

*   **Gerrit**

*   **Bonobo**

*   **AWS CodeCommit**

*   **Bitbucket**

*   **Bitbucket Server**

*   **Gitblit**

*   **Gitolite**


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025184/gitcloud-edit-repo-cfg-web-linking-sel.png?version=2&modificationDate=1648637786816&cacheVersion=1&api=v2&width=680&height=675)

Select a git host from the **Web Link** list. The web linking format fields are automatically filled out with corresponding variables for the selected git host service. Change the variables according to the actual URL settings of the git host.

Only configure the variables enclosed in `<>` (tags) and leave variables enclosed in `{}` (brackets) as is.


You can create several custom configuration to support other git hosting providers. The following five URLs should be configured for setup:

|     |     |
| --- | --- |
| **Option** | **Description** |
| _**View Format**_ | _String._ Optional. <br><br>This URL is unused and not being configured for the newly added integration types. |
| _**Changeset Format**_ | This is the URL used to display revision.  <br>Use the following variable: `${rev}`  – git revision |
| _**File Added Format,**_  <br>_**File Modified Format,**_  <br>_**File Deleted Format**_ | This is the URL to display content of added, modified or deleted files. Use the following variables:<br><br>*   `${num}` –  number of change (0, 1, …)<br>    <br>*   `${rev}`  –  git revision<br>    <br>*   `${path}`  –  path of the file being changed<br>    <br>*   `${parent}`  –  parent git revision<br>    <br>*   `${blob}`  –  ID of blob object<br>    <br>*   `${parent_blob}`  –  ID of parent blob object<br>    <br>*   `$convert(${branch},"subStr","newSubStr")`  –  this inline function returns branch name with `subStr` replaced by a `newSubStr`. As of **v2.11.0+** of the Git Integration app, the `${branch}` code has been changed to cope up with the character requirements on some hosting services. |
| _**Branch Format**_ | This is the URL to display content of branches. |
| _**Tag Format**_ | This is the URL to display content for tag information_._ |

The **Git Integration for Jira** app supports an unlimited number of repositories.

Some git hosts require web linking to be configured via the Git Integration app ➜ ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Edit repository** screen (_mostly single git repository integrations_).

The Bonobo git server requires a branch name to construct URL.  Use `$convert(${branch},"/","~2")` for web linking since bonobo requires substitution of "/" with "~2" in the branch name.

**For example:**
`http://<host>/Bonobo.Git.Server/Repository/<project>/$convert(${branch},"/","~2")/Commit/${rev}`


Any Git host that is accessible via SSH, HTTP, HTTPS and git protocol is supported.

Once properly configured, the **Git Commits** tab on the Jira **Issues** page will display as follows:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025184/gitcloud-jira-issue-commits-tab-weblink-sample-sel.png?version=1&modificationDate=1634298669637&cacheVersion=1&api=v2&width=680&height=355)

[« General settings](/git-integration-for-jira-cloud/general-settings-for-administrators/)

[Linking git commits to Jira issues »](/git-integration-for-jira-cloud/smart-commits-gij-cloud/)