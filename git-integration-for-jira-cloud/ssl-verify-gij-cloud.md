---

title: SSL Verify
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This feature can be accessed at the following locations on the Manage Git repositories page:

<ul style='line-height:2;'>
    <li>
        <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 0 0 5px; font-size: small;'>EXISTING INTEGRATION</b> <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ <b>Edit integration</b>.
    </li>
    <li>
        <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>EXISTING REPOSITORY</b> <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ <b>Edit repository</b>.
    </li>
    <li><b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 0 0 5px; font-size: small;'>EXISTING INTEGRATION</b> <b style='background-color:#DEE0E5; padding:1px 5px; color:#44516C; border-radius:3px; margin: 0 5px; font-size: small;'>EXISTING REPOSITORY</b> Under <b>Integration/Repository</b> _column_ ➜ click an integration or repository URL name.
    </li>
</ul>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If this setting is not displayed, it means that the git host service does not support this feature.
    </div>
    </div>
</div>

The **SSL Verify** option is set to `Enabled` by default. If set to `Disabled`, the Git Integration for Jira Cloud app will ignore verification of SSL certificates when connecting to a git server. This is useful for private Git servers that has custom SSL certificates.

<img src='/wp-content/uploads/gij-gitcloud-edit-repo-cfg-ssl-verify.png' style='margin:25px auto;max-width:100%;dispay:block;' />

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <b>SSL Verify</b> setting is available in Jira Server, Data Center and Jira Cloud. This option is not available for non-fetched repositories.
    </div>
    </div>
</div>

&nbsp;
* * *

[**Prev:** Edit repository](/git-integration-for-jira-cloud/edit-repository-gij-cloud)

[**Next:** View repository indexing logs](/git-integratin-for-jira-cloud/view-repository-indexing-logs-gij-cloud)

