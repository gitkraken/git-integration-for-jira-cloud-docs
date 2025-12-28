---

title: Web linking
description: Configuring web links to your git hosting provider in Git Integration for Jira Cloud
taxonomy:
    category: git-integration-for-jira-cloud

---

<b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>OPTIONAL</b>

The web linking feature adds links to your git hosting provider directly into the **Git Commits** tab. Configure web linking options while editing **repository settings** (![](/wp-content/uploads/actions-icon.png) _Actions ➜ Edit integration_ \| ![](/wp-content/uploads/actions-icon.png) _Actions_ ➜ _Edit repository_) so that commits can include links to the git host pages.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Git Integration for Jira Cloud automatically configures web links for most git hosts via Git service integration panel.
    </div>
    </div>
</div>

For single git repository integration, web link setup is optional. However, git links become available in Git Commits tab when configured.

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

<img src='/wp-content/uploads/gij-gitcloud-edit-repo-cfg-web-linking-sel.png' style='max-width:100%;margin:35px auto 25px auto;display:block;' />

Select a git host from the **Web Link** list. The web linking format fields are automatically filled out with corresponding variables for the selected git host service. Change the variables according to the actual URL settings of the git host.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Only configure the variables enclosed in <code>&lt;&gt;</code> (tags) and leave variables enclosed in <code>{}</code> (brackets) as is.
    </div>
    </div>
</div>

You can create several custom configurations to support other git hosting providers. Configure the following five URLs for setup:

| Option | Description |
| :--- | :--- |
| _**View Format**_ | _String._ Optional. <br><br>This URL is unused and not configured for newly added integration types. |
| _**Changeset Format**_ | This is the URL used to display revision.<br>Use the following variable: `${rev}` – git revision |
| _**File Added Format,**_ <br>_**File Modified Format,**_<br>_**File Deleted Format**_ | This is the URL to display content of added, modified, or deleted files. Use the following variables:<br><ul><li><code>${num}</code> – number of change (0, 1, …)</li><li><code>${rev}</code> – git revision</li><li><code>${path}</code> – path of the file being changed</li><li><code>${parent}</code> – parent git revision</li><li><code>${blob}</code> – ID of blob object</li><li><code>${parent_blob}</code> – ID of parent blob object</li><li><code>$convert(${branch},"subStr","newSubStr")</code> – this inline function returns branch name with <code>subStr</code> replaced by a <code>newSubStr</code>. As of <b>v2.11.0+</b> of the Git Integration app, the <code>${branch}</code> code has been changed to cope with the character requirements on some hosting services.</li></ul> |
| _**Branch Format**_ | This is the URL to display content of branches. |
| _**Tag Format**_ | This is the URL to display content for tag information. |

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Git Integration for Jira</b> supports an unlimited number of repositories.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Some git hosts require web linking to be configured via Git Integration for Jira ➜ Actions ➜ <b>Edit repository</b> screen (<i>mostly single git repository integrations</i>).
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Bonobo git server requires a branch name to construct URL. Use <code>$convert(${branch},"/","~2")</code> for web linking since Bonobo requires substitution of <code>/</code> with <code>~2</code> in the branch name.
        <p style='margin-bottom:-10px'>
            <b>For example:</b><br>
            <code>http://&lt;host&gt;/Bonobo.Git.Server/Repository/&lt;project&gt;/$convert(${branch},"/","~2")/Commit/${rev}</code>
        </p>
    </div>
    </div>
</div>

Any git host that is accessible via SSH, HTTP, HTTPS, and git protocol is supported.

Once properly configured, the **Git Commits** tab on the Jira **Issues** page displays as follows:

<img src='/wp-content/uploads/gij-gitcloud-jira-issue-commits-tab-weblink-sample-sel.png' style='max-width:100%;margin:25px auto 10px auto;display:block;' />

<div align=center style='margin-top:12px'><i>Git Integration for Jira supports custom web linking. The commit information appears <br>
in the Git Commits issue tab if the git host server URL is provided in the <br>
Web Linking section when editing repository settings.</i></div>

&nbsp;
* * *

[**Prev:** General settings for Administrators](/git-integration-for-jira-cloud/general-settings-for-administrators-gij-cloud)

[**Next:** Linking git commits to Jira issues](/git-integration-for-jira-cloud/smart-commits-gij-cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
