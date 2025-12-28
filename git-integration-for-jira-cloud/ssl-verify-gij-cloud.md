---

title: SSL verify
description: How to configure SSL verification for Git integrations
taxonomy:
    category: git-integration-for-jira-cloud

---

Access this feature at the following locations on the Manage Git repositories page:

<ul style='line-height:2;'>
    <li>
        <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 0 0 5px; font-size: small;'>EXISTING INTEGRATION</b> <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ <b>Edit integration</b>.
    </li>
    <li>
        <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>EXISTING REPOSITORY</b> <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ <b>Edit repository</b>.
    </li>
    <li><b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 0 0 5px; font-size: small;'>EXISTING INTEGRATION</b> <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>EXISTING REPOSITORY</b> Under the <b>Integration/Repository</b> column ➜ click an integration or repository URL name.
    </li>
</ul>

If this setting is not displayed, the git host service does not support this feature. For example, SSL Verify is not available for git services such as:

*   GitHub.com
*   GitLab.com
*   Azure/VSTS
*   AWS CodeCommit
*   Bitbucket.org

SSL Verify is available for the following integrations:

*   GitHub Enterprise
*   GitLab CE/EE
*   Azure DevOps Server/TFS
*   Gerrit
*   Plain git repository

The **SSL Verify** option is set to `Enabled` by default. If set to `Disabled`, Git Integration for Jira Cloud ignores verification of SSL certificates when connecting to a git server. This is useful for private Git servers that have custom SSL certificates.

<img src='/wp-content/uploads/gij-gitcloud-edit-repo-cfg-ssl-verify.png' style='margin:25px auto;max-width:100%;display:block;' />

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <b>SSL Verify</b> setting is available in Jira Server, Data Center, and Jira Cloud. This option is not available for non-fetched repositories.
    </div>
    </div>
</div>

&nbsp;
* * *

[**Prev:** Edit nested repository settings](/git-integration-for-jira-cloud/edit-nested-repository-settings-gij-cloud/)

[**Next:** View repository indexing logs](/git-integration-for-jira-cloud/view-repository-indexing-logs-gij-cloud)

&nbsp;

### More Related Topics About Managing Repository/Integration Configuration

[Managing integration or repository configuration](/git-integration-for-jira-cloud/managing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Managing integrations via Actions (Jira Cloud)](/git-integration-for-jira-cloud/managing-integrations-via-actions-jira-cloud-gij-cloud/) (Git Integration for Jira Cloud)

[Edit integration settings](/git-integration-for-jira-cloud/edit-integration-gij-cloud/) (Git Integration for Jira Cloud)

[Edit repository settings](/git-integration-for-jira-cloud/edit-repository-gij-cloud/) (Git Integration for Jira Cloud)

[Edit nested repository settings](/git-integration-for-jira-cloud/edit-nested-repository-settings-gij-cloud/) (Git Integration for Jira Cloud)

**SSL verify** (this page)

[View repository indexing logs](/git-integration-for-jira-cloud/view-repository-indexing-logs-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect an integration or repository configuration](/git-integration-for-jira-cloud/removing-integration-or-repository-configuration-gij-cloud/) (Git Integration for Jira Cloud)

[Disconnect a nested repository configuration](/git-integration-for-cloud/remove-a-nested-repository-gij-cloud/) (Git Integration for Jira Cloud)

[Associating project permissions](/git-integration-for-jira-cloud/associating-project-permissions-gij-cloud/) (Git Integration for Jira Cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
