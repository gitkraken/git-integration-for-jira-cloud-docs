---

title: Require Personal Access Tokens for user actions (create branch/pull request)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

**What's on this page:**
- [Background](#background)
- [Objective](#objective)
- [Instructions](#instructions)
- [What will Jira users see?](#what-will-jira-users-see)


## Background

The Git Integration for Jira app allows users of integrations (_such as GitLab, GitHub and etc._) to create branches and pull requests from within the Jira issue. By default, the operation will be performed by the integration user that is used for indexing.

![](/wp-content/uploads/gij-jira-server-create-branch-example-01.png)

## Objective

For teams looking to maintain user attribution, Jira administrators can require that individual Jira users provide personal access tokens to perform actions such as creating a branch or pull request in Jira. This can be done by using their git service account rather than the integration account.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Supported integrations:</b><br>
        User attribution is supported in the following special integrations in Git Integration for Jira Cloud:
        <ul style='margin-bottom:0px !important'>
            <li>GitHub.com</li>
            <li>GitHub Enterprise</li>
            <li>GitLab.com</li>
            <li>GitLab self-managed</li>
            <li>Microsoft Azure DevOps</li>
            <li>Microsoft Visual Studio Team Services (VSTS)</li>
            <li>Microsoft Team Foundation Server (TFS)</li>
            <li>AWS CodeCommit</li>
        </ul>
    </div>
    </div>
</div>
<br>

## Instructions

To enable/disable the _**Require User PAT**_ setting for all repositories within an integration:

1.  Navigate to **Manage Git repositories**.

2.  Add a new integration or edit existing integration's feature settings.

    ![](/wp-content/uploads/gij-req-pat-gitmgr-actions-edit-git-settings.png)

3.  Locate the **Require User PAT** setting.

    ![](/wp-content/uploads/gij-req-pat-gitmgr-page-actions-control-cfg.png)

4.  Tick the box to enable the requiring of user PAT.

5.  Click **Update** at the bottom of the page to save the setting.


## What will Jira users see?

1.  Once the Jira administrator requires Personal Access Tokens, your Jira users will be presented with a message that setup is required.

    ![](/wp-content/uploads/gij-req-pat-create-branch-dlg-setup-your-pat.png)

2.  Following that link - the user is taken to a prompt on the **User settings** screen to enter Personal Access Token (PAT) for the service (GitHub, GitLab, etc).
    See [Instructions: Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud).

    ![](/wp-content/uploads/gij-req-pat-seruo-pat-dlg.png)

    If you don't have a token or your existing PAT has expired, click the **New token** label link to start generating a new PAT.

3.  With the Personal Access Token saved - the user will now see the following:

    ![](/wp-content/uploads/gij-req-pat-create-branch-dlg-after-pat-is-setup.png)

PATs were introduced with TFS 2017 and newer.  TFS 2013 and TFS 2015 do not support PATs.  If the repository setting **Require User PAT** property is set to `ON`, the users will not be able to create/delete branches and pull requests.

Personal Access Tokens are saved per integration by individual Jira users app. Examples shown above are for the Create branch action; Create pull request is the same. The same token is used for Create branch and Create pull request.

Jira users must have the **View Development Tools** permission in the context of a Jira project to view content from the Git Integration for Jira app.

<p>&nbsp;</p>
&nbsp;

<!-- FOOTNOTE -->
<br>
<br>
<div style='border-top: 1px solid #456; width: 40%; padding-bottom: 12px'></div>
<div style='font-size: 12px;'>
    <sup>1</sup> <i>Logo owned by <a href='https://gitlab.com/'>GitLab Inc</a> used under <a href='https://creativecommons.org/licenses/by-nc-sa/4.0/'>license</a>.
    <p>&nbsp;&nbsp;All product names, logos, and brands are property of their respective owners.<p><i>
</div>

