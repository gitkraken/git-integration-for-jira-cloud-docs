---

title: Deep Linking
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>NEW FEATURE</b>
<br>

Deep linking allows you to quickly move between Jira and your Git source code.

We've added the ability to deep link from repositories, commits, branches, and tags throughout the Git Integration for Jira app into the [GitKraken Git client](https://www.gitkraken.com) and [GitLens VS Code extension](https://www.gitkraken.com/gitlens).

![](/wp-content/uploads/gij-gitcloud-deeplinking-feature-example.png)

GitKraken supports deep linking into Git Integration for Jira as well. To learn more about this feature, see [GitKraken Integrations: Git Integration for Jira](https://support.gitkraken.com/integrations/git-integration-for-jira/).

GitLens 13.3 introduced deep linking support and Git Integration for Jira allows users to open commit, tags and repository links into GitLens. To learn more about this feature, see [GitLens Deep Linking support](https://help.gitkraken.com/gitlens/gitlens-release-notes-current/#deep-linking-support).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>On this page:</b><br>
        <ul style='margin-bottom:0px;'>
            <li><a href='#deep-linking-to-the-gitkraken-client'>Deep Linking to the GitKraken Client</a></li>
            <li><a href='#deep-linking-to-gitlens'>Deep Linking to GitLens</a></li>
        </ul>
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Deep Linking to the GitKraken Client

<img src='https://www.gitkraken.com/wp-content/uploads/2023/01/Group-812.svg' style='margin:30px auto 35px auto;' />

[GitKraken Git Client](https://www.gitkraken.com/git-client/features) is a multi-platform application which allows integration of Git repositories such as GitHub, GitLab, Bitbucket, Azure DevOps, Jira, and more. It provides a seamless approach to visualize Git, helping thousands of developers save time with their development workflow. It grants flexibility with switching between a GUI or a terminal. It also possesses robust team features which affords a seamless experience with Git -- whether you work on Windows, Mac or Linux.

### Video

<div class='embed-container' style='padding-bottom: 69.58%'>
    <iframe width='709' height='493' src='https://fast.wistia.com/embed/iframe/qhlf1natdt?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px;margin-bottom:40px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/qhlf1natdt'><b>here</b></a> and open this video in a new browser tab for more viewing options.</i>
</div>
<br>

### GitKraken deep link access locations

The GitKraken deep links are accessible on the following locations:

#### Jira issue – Git commits tab

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-issue-git-commits.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitKraken in the Commits panel in the Git Commits tab' />

#### Jira issue Git developer panel – branches and tags lists

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-issue-branches.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitKraken in the Branches list on the Jira issue Git development panel' />

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-issue-tags.png' style='margin:0 auto 25px auto;display:block;' alt='Shows the deeplink for GitKraken in the Tags list on the Jira issue Git development panel' />

#### Repository browser – All repository table

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-repo-browser-actions.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitKraken in the Repository browser -- Repositories list' />

#### Repository browser – Commits page

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-repo-browser-commit.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitKraken in the Repository browser -- Commits page' />

#### Repository browser – Compare page (commit view)

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-repo-browser-compare.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitKraken in the Repository browser -- Compare page' />

#### Jira issue Git Commits tab deeplinking panel

Use the deeplinking panel on the Jira issue Git Commits tab to download the GitKraken Git client.

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-download-git-commits-issue-tab.png' style='margin:25px auto;display:block;' alt='Use the deeplinking panel on the Jira issue Git Commits tab to download the GitKraken Git client app' />

#### Jira issue Git development sidebar deeplinking panel

Use the deeplinking panel on the Jira issue Git development sidebar to download the GitKraken Git client.

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-download-dev-panel.png' style='margin:25px auto;display:block;' alt='Use the deeplinking panel on the Jira issue Git development sidebar to download the GitKraken Git client app' />


### GitKraken user settings

Individual Jira Cloud users can enable or disable the GitKraken integration with Git Integration for Jira Cloud by visiting the Git Integration: User settings page.

1.  Go to **Jira Profile** menu.

2.  Click **Git Integration: User settings**.

3.  Enable/disable the setting under the **Connected apps** section.

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-user-settings.png'  style='margin:25px auto;display:block;' alt='Access the GitKraken integration option to enable/disable the feature in the User settings (sidebar) of the Git Integration for Jira app' />

<br>

### GitKraken administrator settings

The GitKraken deeplinking feature is enabled by default in the General settings of Git Integration for Jira app.

Jira Data Center administrators can enable/disable this feature for all Jira users. All Jira Server users can enable the GitKraken integration separately (see [User settings](/git-integration-for-jira-cloud/user-settings-gij-cloud) above).

1.  Go to the Git Integration for Jira – **General settings** tab (sidebar).

2.  Enable/disable this setting under **Jira Issue View Options**

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitkraken-general-settings.png'  style='margin:25px auto;display:block;' alt='Access the GitKraken integration option to enable/disable the feature in the General settings of the Git Integration for Jira app' />

&nbsp;

* * *

&nbsp;

## Deep Linking to GitLens

<img src='https://www.gitkraken.com/wp-content/uploads/2023/01/Group-17491.svg' style='margin:30px auto 35px auto;' />

[GitLens](https://www.gitkraken.com/gitlens) is a Visual Studio Code extension and supercharges Git inside VS Code while helping users visualize code, explore Git repositories, use powerful compare commands and so much more.

Support for GitLens deep linking is now available in Git Integration for Jira app. Open repositories, commits, tags, and branches into GitLens using the relevant access locations in Jira.

### GitLens deep link access locations

The GitLens deep links are accessible on the following locations:

#### Jira issue – Git commits tab

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-issue-git-commits.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitLens in the Commits panel in the Git Commits tab' />

#### Jira issue Git developer panel – branches and tags lists

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-issue-branches.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitLens in the Branches list on the Jira issue Git development panel' />

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-issue-tags.png' style='margin:0 auto 25px auto;display:block;' alt='Shows the deeplink for GitLens in the Tags list on the Jira issue Git development panel' />

#### Repository browser – All repository table

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-repo-browser-actions.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitLens in the Repository browser -- Repositories list' />

#### Repository browser – Commits page

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-repo-browser-commit.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitLens in the Repository browser -- Commits page' />

#### Repository browser – Compare page (commit view)

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-repo-browser-compare.png' style='margin:25px auto;display:block;' alt='Shows the deeplink for GitLens in the Repository browser -- Compare page' />


#### Jira issue Git Commits tab deeplinking panel

Use the deeplinking panel on the Jira issue Git Commits tab to download the GitLens extension.

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-download-git-commits-issue-tab.png' style='margin:25px auto;display:block;' alt='Use the deeplinking panel on the Jira issue Git Commits tab to download the GitLens extension' />

#### Jira issue Git development sidebar deeplinking panel

Use the deeplinking panel on the Jira issue Git development sidebar to download the GitLens extension.

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-download-dev-panel.png' style='margin:25px auto;display:block;' alt='Use the deeplinking panel on the Jira issue Git development sidebar to download the GitLens extension' />

### GitLens user settings

Individual Jira Cloud users can enable or disable the GitLens integration with Git Integration for Jira Cloud by visiting the Git Integration: User settings page.

1.  Go to **Jira Profile** menu.

2.  Click **Git Integration: User settings**.

3.  Enable/disable the setting under the **Connected apps** section.

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-user-settings.png'  style='margin:25px auto;display:block;' alt='Access the GitLens integration option to enable/disable the feature in the User settings (sidebar) of the Git Integration for Jira app' />

<br>

### GitLens administrator settings

The GitLens deeplinking feature is enabled by default in the General settings of Git Integration for Jira app.

Jira Data Center administrators can enable/disable this feature for all Jira users. All Jira Server users can enable the GitLens integration separately (see Profile settings)

Go to the Git Integration for Jira – **General settings** tab (sidebar).

Enable/disable this setting under **GitLens integration** section.

<img src='/wp-content/uploads/gij-gitcloud-deeplink-gitlens-general-settings.png'  style='margin:25px auto;display:block;' alt='Access the GitLens integration option to enable/disable the feature in the General settings of the Git Integration for Jira app' />

