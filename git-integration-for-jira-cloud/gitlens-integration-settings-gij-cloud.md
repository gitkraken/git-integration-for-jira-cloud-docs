---

title: GitLens integration settings
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This setting is part of the <a href="/git-integration-for-jira-cloud/general-settings-gij-cloud">General settings</a> configuration page for Git Integration for Jira Cloud.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Default settings</b><br>
        <ul style='margin-bottom:0px;'>
            <li>
                This setting is enabled in <a href="https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?tab=overview&hosting=cloud" target="_blank"><b>Git Integration for Jira Cloud</b></a> app by default.
            </li>
            <li>
                This setting is turned off by default in <a href="https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview" target="_blank"><b>Dev Info for Jira Cloud</b></a> app.
            </li>
        </ul>
    </div>
    </div>
</div>

&nbsp;

### Enable GitLens integration

<img src='/wp-content/uploads/gij-gitcloud-gencfg-enable-gitlens-integration-417.png' style='margin:25px auto;max-width:100%;display:block;' />

Enable this setting to turn on the deep linking feature which allows you to quickly move between Jira and your Git source code with the GitLens VSCode extension. GitLens supports deep linking into Git Integration for Jira as well. To learn more about this feature, see [GitLens Integrations: Git Integration for Jira](https://www.gitkraken.com/gitlens).

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Permissions</b><br>
        The <b>View developer tools</b> <i>permission</i> is required to view the git commits. Jira users must also have the <b>Browse Project</b> <i>permissions</i> to a project associated with a repository to view.
    </div>
    </div>
</div>
<br>

For more details, see [Features: Deep Linking to the GitLens (Jira Cloud)](/git-integration-for-jira-cloud/deep-linking-into-gitlens-gij-cloud).

After all the settings have been configured according to your requirements, click **Update** to apply the changes.

