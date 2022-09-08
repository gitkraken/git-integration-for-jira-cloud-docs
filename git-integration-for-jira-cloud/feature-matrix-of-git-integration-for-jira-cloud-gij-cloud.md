---

title: Feature matrix of Git Integration for Jira Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
See also [Feature Comparison](/git-integration-for-jira-cloud/git-integration-server-data-center-vs-jira-cloud-feature-comparison-gij-cloud) for information on features and differences between Git Integration for Server/Data Center versus Git Integration for Jira Cloud.

The [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app offers a variety of integration options and features. The below matrix explains which features are offered when using a specific type of integration. For any questions, contact [BigBrassBand Support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

|     | Git service integrations<br><br>\[Classic full feature integrations\] | Single git repository integrations<br><br>\[Limited feature connect\] | Webhook indexing integrations<br><br>\[Limited feature connect\] |
| :--- | :--- | :--- | :--- |
| **Works with git servers behind firewall** | ![](/wp-content/uploads/gij-matrix-open-warn-blue.png) | ![](/wp-content/uploads/gij-matrix-open-warn-blue.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| **View commits, branches, pull/merge requests in Jira** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) Commits and branches<br><br>![](/wp-content/uploads/gij-matrix-open-not-red.png) Pull/merge requests | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| **Pull / Merge Request Reviewers and Approvals Shown in Jira** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-not-red.png) Pull/merge requests | ![](/wp-content/uploads/gij-matrix-open-check-green.png) GitHub<br><br>![](/wp-content/uploads/gij-matrix-open-check-green.png) Azure DevOps, VSTS, TFS<br><br>![](/wp-content/uploads/gij-matrix-open-not-red.png) GitLab |
| **View git tags in Jira** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b> |
| **Support for Automation for Jira + Smart Commits** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| **Repository Browser** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| **Create branches and pull requests in Jira** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-not-red.png) | ![](/wp-content/uploads/gij-matrix-open-not-red.png) |
| **Support for large # of commits in git pushes** |  ▼  |  ▼   |  ▼  |
| **GitHub** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) |
| **GitLab** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-warn-blue.png) Max of 20 commits per push |
| **Azure DevOps, VSTS, TFS** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-warn-blue.png) Max of 25 commits per push |
| **AWS CodeCommit** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b> |
| **BitBucket** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b> |
| **Gerrit** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>COMING SOON</b> |
| **Indexing full repository history** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-not-red.png) |
| **View source code in Jira** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-not-red.png) |
| **Easily connect many repositories** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-not-red.png) Each repository must be configured by a Jira administrator | ![](/wp-content/uploads/gij-matrix-open-check-green.png) Webhook indexing can be configured at organization / server / group level. |
| **Authentication** | HTTPS, HTTP, OAuth (GitHub.com, Azure DevOps and VSTS) | HTTPS, HTTP, SSH | Secret protected URL |
| **Connect any git repository** | ![](/wp-content/uploads/gij-matrix-open-warn-blue.png) Classic integrations currently include: GitHub, GitLab, Bitbucket, AWS CodeCommit, Azure DevOps, VSTS, TFS and Gerrit. | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-warn-blue.png) Webhook indexing currently supports: GitHub, GitLab, Azure DevOps, VSTS, and TFS. |
| **Indexing triggers** | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) | ![](/wp-content/uploads/gij-matrix-open-check-green.png) Indexing triggers are not necessary. |


<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For more information about the different types of integrations:
        <ul>
            <li><a href='/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud'>Classic Indexing Explainer</a></li>
            <li><a href='/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud'>Webhook Indexing Explainer</a></li>
            <li><a href='/git-integration-for-jira-cloud/setting-up-integrations-gij-cloud'>Setting up integrations</a></li>
        </ul>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        
    </div>
    </div>
</div>

If you have questions or need additional support - contact [BigBrassBand Support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

