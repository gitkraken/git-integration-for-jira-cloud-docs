---

title: Git Integration for Jira Cloud - Release Notes
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
We publish new features, bug fixes, security updates/patches, and Jira compatibility regularly. Below are highlights of the changes.

**Important links**

*   [Roadmap for Git Integration for Jira Cloud](https://trello.com/b/Af64QYkE/git-integration-jira-cloud-roadmap)

*   [Atlassian Marketplace listing](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview)

*   [Git Integration for Jira Cloud Status](https://status.bigbrassband.com)

*   [Git Integration for Jira Cloud Security](https://www.gitkraken.com/git-integration-for-jira/security-and-trust)


If you have any questions, please contact us through our [Support Portal](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

* * *

## GitLens for Visual Studio Code Integration
'29 Mar 2023' <b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>NEW FEATURE</b> <b style='background-color:#EAE5FE; padding:1px 5px; color:#412C92; border-radius:3px; margin: 0 5px; font-size: small;'>ALL USERS</b>

This workflow improvement is a great addition for developers that are using Visual Studio Code to edit source code. [GitLens](https://www.gitkraken.com/gitlens) is a Visual Studio Code extension that helps users visualize code, explore Git repositories, use powerful compare commands and so much more. From within Jira, clicking on the GitLens icon next to repositories, commits, tags, and branches will open them in VS Code.

![](https://help.gitkraken.com/wp-content/uploads/gij-gitcloud-deeplink-gitlens-issue-git-commits.png)

This enables team members to quickly transition between Jira and their code editor without losing context. GitLens deep links are located within Jira issues and the Repository Browser. [View the help article](https://help.gitkraken.com/git-integration-for-jira-cloud/deep-linking-into-gitlens-gij-cloud/) for more information.

## GitHub OAuth: Deep link admins into their GitHub account to the correct app settings

25 Mar 2022 NEW FEATURE ADMINS

Adds a link to GitHub to quickly view which GitHub organizations are authorized for use with Git Integration for Jira.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/gitcloud-github-oauth-permissions.png?version=1&modificationDate=1648202553405&cacheVersion=1&api=v2)

## Manage repositories: Ability to reindex or disable individual repositories

25 Mar 2022 NEW FEATURE ADMINS

This is a new feature that allows you to reindex individual repositories or disable them without having to remove them.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr-reindex-selected.png?version=2&modificationDate=1645034345288&cacheVersion=1&api=v2&width=510&height=282)

## Manage repositories: New settings are now visible

25 Mar 2022 IMPROVEMENT ADMINS

Some new features have been brought to the Manage repositories screen such as:

*   permissions

*   smart commits

*   the state of indexing triggers for webhooks

*   Last indexed (shows dates for the last time it was indexed)


The status field has been upgraded to be much more accurate as well as show a symbol to let you know the state of progress.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr-settings.png?version=1&modificationDate=1645121982620&cacheVersion=1&api=v2&width=510&height=282)

## Manage repositories: Commits/branches/PR count added

25 Mar 2022 NEW FEATURE ADMINS

New column headers to view the number of branches, commits and pull requests.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr-counts.png?version=1&modificationDate=1645034225511&cacheVersion=1&api=v2&width=510&height=282)

## Manage repositories: Improved access to indexing logs

25 Mar 2022 IMPROVEMENT ADMINS

The Repository Indexing Log has been greatly improved by now showing just the most-recent 15 lines of the log, and providing the ability to copy it to the clipboard or download the full log.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr-logs.png?version=1&modificationDate=1645034180112&cacheVersion=1&api=v2&width=510&height=323)

## Manage repositories: Refresh data

25 Mar 2022 NEW FEATURE ADMINS

You will get nice clean pagination when you refresh the data using this handy new feature.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr-refresh-data.png?version=1&modificationDate=1645034149880&cacheVersion=1&api=v2&width=510&height=282)

## Manage repositories: Multi-select

25 Mar 2022 NEW FEATURE ADMINS

This new features lets you select all repositories in your list or pick and choose repositories, then apply the function “Reindex selected”, “Enable selected”, or “Disable selected”.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr-multiselect.png?version=1&modificationDate=1645034117757&cacheVersion=1&api=v2&width=510&height=282)

## Manage repositories: Option to reindex individual repositories manually

25 Mar 2022 NEW FEATURE ADMINS

Reindex any selected repository.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr-reindex-selected.png?version=2&modificationDate=1645034345288&cacheVersion=1&api=v2&width=510&height=282)

## Manage repositories: Filtering (status, name, integration)

25 Mar 2022 NEW FEATURE ADMINS

You can use this new dropdown menu to filter all integrations, status, and perform text searches for the names of repositories (very helpful if you have a high number of repositories).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr-filtering.png?version=1&modificationDate=1645034023629&cacheVersion=1&api=v2&width=510&height=282)

## Manage repositories: Sorting (repo, integration, last indexed, # of commits/branches/PRs)

25 Mar 2022 NEW FEATURE ADMINS

With this new feature you can now sort your list of repositories by repo name, integration name, last indexed time, or number of branches, commits, or PRs.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr-sorting.png?version=1&modificationDate=1645033976431&cacheVersion=1&api=v2&width=510&height=282)

## New section: Manage repositories

25 Mar 2022 NEW FEATURE ADMINS

There are many new and improved features in this section including: Sorting (repo, integration, last indexed, # of commits/branches/PRs), filtering (status, name, integration), a new option to reindex individual repositories manually, multi-select feature for repositories, ability to refresh data, improved access to indexing logs, commits/branches/PR count added, and the new ability to reindex or disable individual repositories.

There are also an array of new settings now visible from this screen such as: permissions, smart commits, the state of indexing triggers for webhooks, status, and last indexed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mr.png?version=1&modificationDate=1645033607560&cacheVersion=1&api=v2&width=510&height=282)

## Manage integrations: Implement filtering by name and status

25 Mar 2022 NEW FEATURE ADMINS

Using the new status dropdown selector you can now filter by which state you’re in – useful if you have a large number of integrations. Filtering by name is also made possible.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mi-filtering.png?version=1&modificationDate=1644949149031&cacheVersion=1&api=v2&width=510&height=282)

## Manage integrations: Disabling/Enabling feature

25 Mar 2022 NEW FEATURE ADMINS

Using this new feature, you can now stop or pause the integration without having to remove it.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mi-select-status.png?version=1&modificationDate=1644949108427&cacheVersion=1&api=v2&width=510&height=282)

## Manage integrations: New settings are now visible

25 Mar 2022 IMPROVEMENT ADMINS

Some new features have been brought to the Manage integrations screen such as:

*   permissions

*   smart commits

*   the state of indexing triggers for webhooks

*   Last indexed (shows dates for the last time it was indexed)


The status field has been upgraded to be much more accurate as well as show a symbol to let you know the state of progress.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mi-settings.png?version=1&modificationDate=1645033548105&cacheVersion=1&api=v2&width=510&height=282)

## Manage integrations: Select orgs/repositories feature

25 Mar 2022 IMPROVEMENT ADMINS

This new features allows you to pick and choose which repositories to connect, without having to add them all.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/select-repositories.png?version=1&modificationDate=1644948845755&cacheVersion=1&api=v2&width=510&height=282)

## Manage integrations: improved access to indexing logs

25 Mar 2022 IMPROVEMENT ADMINS

The Repository Indexing Log can be accessed from the gear icon located under Actions, and has been greatly improved by now showing just the most-recent 15 lines of the log, and providing the ability to copy it to the clipboard or download the full log.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mi-logs.png?version=1&modificationDate=1644948761571&cacheVersion=1&api=v2&width=510&height=323)

## Manage integrations: Repo count

25 Mar 2022 NEW FEATURE ADMINS

This handy new feature we’ve included on the Manage integrations page shows the number of connected repositories for each instance.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mi-repo-count.png?version=1&modificationDate=1644948728961&cacheVersion=1&api=v2&width=510&height=282)

## Manage integrations: Integrations list with wizard for adding to list

25 Mar 2022 IMPROVEMENT ADMINS

*   Admins will be able to take advantage of a new wizard to add integrations in a streamlined fashion. The wizard features an easy 3-step setup process:

    *   Select integration type

    *   Select Git service

    *   Select repositories

    *   The wizard makes it clear to admins where they are in the process and guides them through each step to completion.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/add-integration.png?version=1&modificationDate=1644948694935&cacheVersion=1&api=v2&width=510&height=282)

## Manage integrations: Welcome message showing details of your integrations

25 Mar 2022 NEW FEATURE ADMINS

When you access the new “Manage integrations” menu item, you will now get a welcome message that includes details about your integrations. For example, upon getting started you will see the message “You have no integrations yet.” along with an accompanying button to “Add integrations”. This new improvement makes it easier to understand right from the start where you stand and what needs to be done upfront, while providing a handy button to proceed to get your integrations added.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/mi-welcome-message.png?version=1&modificationDate=1644948622922&cacheVersion=1&api=v2&width=510&height=282)

## New section: Manage integrations

25 Mar 2022 NEW FEATURE ADMINS

There are many new and improved features in this section including: An improved integrations list, repo count, improved access to indexing logs, a new select orgs/repos feature, disable/enable feature for integrations, and you can now implement filtering by name and status.

There are also an array of new settings now visible from this screen such as: permissions, smart commits, the state of indexing triggers for webhooks, status, and last indexed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/manage-integrations.png?version=2&modificationDate=1644948566792&cacheVersion=1&api=v2&width=510&height=282)

## “Manage Git repositories” menu item has now been split into two new menu items

25 Mar 2022 NEW FEATURE ADMINS

The “Manage Git repositories” menu item (from previous versions) has now been split into two new menu items named “Manage integrations” and “Manage repositories”.
Take a look at what each of these new sections entail in the following entries.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/New-menu-items.png?version=2&modificationDate=1644948507935&cacheVersion=1&api=v2&width=510&height=282)

## New User Interface for admins

25 Mar 2022 IMPROVEMENT ADMINS

We’ve launched an all-new management user interface, supporting the goal of making the UI more self-serving for admins. The new UI contains improved functions from new sorting features to viewing the number of repos connected on each instance. More specific details are provided in the other Release Notes entries on this page. The new UI also features an improvement which now allows you to configure your repositories visually.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/manage-integrations.png?version=2&modificationDate=1644948566792&cacheVersion=1&api=v2&width=510&height=282)

* * *

## Deep Linking to GitKraken

21 Sep 2021 NEW FEATURE ALL USERS

With the [acquisition](https://www.gitkraken.com/blog/gitkraken-acquires-git-integration-jira-bigbrassband) of BigBrassBand's Git Integration for Jira app (GIJ) by GitKraken, we have introduced deep linking between GIJ and GitKraken so users can now have a stronger integration between the two. You can now click to open commits, branches, tags and repositories directly in GitKraken from the Jira issue view giving you a seamless transition from your Jira issues to GitKraken.

[Learn more](/git-integration-for-jira-cloud/deep-linking-to-the-gitkraken-client-gij-cloud)

You will see the added ability to open the GitKraken client from our app in various locations. See an example of what this looks like below.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/screenshot%201.png?version=2&modificationDate=1636484053576&cacheVersion=1&api=v2&width=544&height=300)

## Default branch for a repository + project + user

13 Jun 2021 IMPROVEMENT ALL USERS

Now you can configure a Default branch for a repository when creating new branches. When using this feature, you will no longer have to select the branch each time you pick the repository.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/gitcloud-user-settings-default-branches-sel.png?version=1&modificationDate=1632647800328&cacheVersion=1&api=v2&width=544&height=209)

You may immediately set the selected branch as default for the current repository when using the create branch dialog.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/gitcloud-user-settings-create-def-branch-dlg.png?version=2&modificationDate=1632899635182&cacheVersion=1&api=v2&width=340&height=188)

For more information on this feature, see article [Default branch feature](/git-integration-for-jira-cloud/default-branch-feature-gij-cloud).

## Webhook indexing integration

13 May 2021 NEW FEATURE ADMINS

Webhook indexing integration allows your connected git servers to work behind a firewall but will have limited features which are stated under the Connect the your Git server features comparison table. For detailed information on this new feature, see [Git Integration for Jira Cloud: Webhook indexing integration](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud).

![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/gitcloud-release-notes-whook-idx-01.png?version=1&modificationDate=1621314159632&cacheVersion=1&api=v2)
![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/gitcloud-release-notes-whook-idx-02.png?version=1&modificationDate=1621314164638&cacheVersion=1&api=v2)

## User PATs have been moved to a new page

07 Mar 2021 NEW FEATURE ALL USERS

We've created a new Jira user settings screen to allow individual Jira users to manage their Personal Access Tokens (PATs) for use in creating/deleting branches and pull requests from Jira.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/CleanShot2021-03-08_at_13.26.54@2x.png?version=1&modificationDate=1615237434880&cacheVersion=1&api=v2&width=544&height=283)

* * *

## Support for Dark Mode in Jira Cloud Mobile

25 Jan 2021 NEW FEATURE ALL USERS

Enabled dark mode support for iOS, MacOS and Android for the Jira Cloud mobile apps.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/1632-aui-problem-example.PNG?version=1&modificationDate=1611594397643&cacheVersion=1&api=v2&width=204&height=362)

* * *

## Expand to see more code in diff screens

23 Nov 2020 NEW FEATURE ALL USERS

Expand to see more of a file when doing quick code reviews in Jira Cloud.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/CleanShot2020-11-23%20at%2010.28.39@2x-20201123-153004.png?version=1&modificationDate=1606145421958&cacheVersion=1&api=v2&width=442&height=213)

Video (0:09):

[CleanShot2020-11-23 at 10.27.04-2.mp4](/wiki/download/attachments/871792645/CleanShot2020-11-23%20at%2010.27.04-2.mp4?version=1&modificationDate=1606145270685&cacheVersion=1&api=v2&width=442)

* * *

## Support for iOS, Android, and Mac Apps

05 Nov 2020 NEW FEATURE ALL USERS

Development Information (branches, commits, and pull requests) are now visible in:

*   [Jira Cloud iOS app](https://www.atlassian.com/software/jira/mobile-app)

*   [Jira Cloud Android app](https://www.atlassian.com/software/jira/mobile-app)

*   [Jira Cloud MacOS app](https://www.atlassian.com/software/jira/mac)


This information is visible in the native Jira Cloud development information area + the Git Integration glance where you can view branches, commits, pull requests and tags.  You can create branches and pull requests all from the above applications.


**Mobile apps**

| Examples | Examples | Examples |
| --- | --- | --- |
| **Jira iOS/Android app: View development information**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/IMG_DCB9B343D5C3-1.jpeg?version=1&modificationDate=1605127361553&cacheVersion=1&api=v2&width=102&height=220) | **Jira iOS/Android app: Branches detail**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/IMG_017E0B3B5371-1.jpeg?version=2&modificationDate=1605127402971&cacheVersion=1&api=v2&width=102&height=220) | **Jira iOS/Android app: Commits detail**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/IMG_80F7BE242631-1.jpeg?version=1&modificationDate=1605127426174&cacheVersion=1&api=v2&width=102&height=220) |
| **Jira iOS/Android app: Pull / merge requests detail**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/IMG_2BD0A76A4891-1.jpeg?version=1&modificationDate=1605127449033&cacheVersion=1&api=v2&width=102&height=220) | **Jira iOS/Android app: Git Integration “glance” view**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/IMG_655428BABEEB-1.jpeg?version=1&modificationDate=1605127539872&cacheVersion=1&api=v2&width=102&height=220) | **Jira iOS/Android app: Glance: Create branch**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/IMG_03572F208F3B-1.jpeg?version=1&modificationDate=1605127586708&cacheVersion=1&api=v2&width=102&height=220) |
| **Jira iOS/Android app: Glance: Create branch**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/IMG_50095B8D776F-1.jpeg?version=1&modificationDate=1605127638241&cacheVersion=1&api=v2&width=102&height=220) |     |     |

**MacOS app**

| Examples | Examples | Examples |
| --- | --- | --- |
| **Jira MacOS app: Issue sidebar**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2015.33.16@2x-20201111-203318.png?version=1&modificationDate=1605126815417&cacheVersion=1&api=v2) | **Jira MacOS app: Branches detail**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/CleanShot%202020-11-11%20at%2015.34.00@2x-20201111-203401.png?version=1&modificationDate=1605126850897&cacheVersion=1&api=v2&width=204&height=162) | **Jira MacOS app: Commits detail**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2015.34.20@2x-20201111-203421.png?version=1&modificationDate=1605126872113&cacheVersion=1&api=v2) |
| **Jira MacOS app: Pull / merge requests detail**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2015.34.56@2x-20201111-203457.png?version=1&modificationDate=1605126909706&cacheVersion=1&api=v2) | **Jira MacOS app: Git Integration: “glance” view**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2015.36.12@2x-20201111-203613.png?version=1&modificationDate=1605126983163&cacheVersion=1&api=v2) | **Jira MacOS app: Git Integration: Glance: Create branch**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2015.37.41@2x-20201111-203743.png?version=1&modificationDate=1605127079983&cacheVersion=1&api=v2) |
| **Jira MacOS app: Git Integration: Glance: Create pull request**<br><br>![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2015.38.58@2x-20201111-203859.png?version=1&modificationDate=1605127149677&cacheVersion=1&api=v2) |     |     |

* * *

## Default repository for projects

05 Sep 2020 NEW FEATURE ALL USERS

Developers will often work in a single repository in a given Jira project. Each Jira user can now set their own default repository for a Jira project.

[default-repo-feature.mov](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/default-repo-feature.mov?version=1&modificationDate=1605046934883&cacheVersion=1&api=v2&width=612)

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/create-pull-request-annotated.png?version=1&modificationDate=1605045753159&cacheVersion=1&api=v2&width=510&height=190)

Default repository selection for Jira projects is available in the [Create branch](/git-integration-for-jira-cloud/create-branch-gij-cloud) and [Create pull / merge request](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud) features of the app.

All default selections can be reviewed and updated in [User Settings](/git-integration-for-jira-cloud/user-settings-gij-cloud):

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/user-settings-default.png?version=1&modificationDate=1605564848523&cacheVersion=1&api=v2&width=510&height=246)

* * *

## Pagination for Repository Browser screen

06 Jun 2020 NEW FEATURE ALL USERS

All Jira users with the `View development tools` permission have access to the **Repository browser** screen (_formerly View all repositories_) in Jira Cloud. We have added pagination to this screen to better support large numbers of repositories and the ability to filter the list by search term.

**Note:** Permissions to specific repositories can be limited using Project Permissions (see [Permissions](/git-integration-for-jira-cloud/permissions-gij-cloud) for more information).

[view-all-repos-pagination-feature.mov](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/view-all-repos-pagination-feature.mov?version=1&modificationDate=1605048187186&cacheVersion=1&api=v2&width=612)

* * *

## Webhook Log Viewer

02 May 2020 NEW FEATURE ADMINS

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/CleanShot%202020-11-05%20at%2013.21.15@2x-20201105-182120.png?version=1&modificationDate=1604600486980&cacheVersion=1&api=v2&width=612&height=428)

The **Webhooks** page now includes logs of inbound webhooks sent to the Git Integration for Jira Cloud app. Status, reindex status, type, and related repository are shown in the table to assist Jira administrators in troubleshooting and identifying which webhooks are triggered for reindexing.

Webhook logs are retained for 7 days.

* * *

## Add Jira issue link to Pull / Merge Request description

28 Feb 2020 NEW FEATURE ALL USERS

When a Jira user creates a pull request or merge request (GitLab) using the Git Integration for Jira app ([Create pull / merge request](/git-integration-for-jira-cloud/create-pull-or-merge-request-gij-cloud), a link to the Jira issue is included in the pull request / merge request description.

| **GitLab** | **GitHub** | **Bitbucket** |
| --- | --- | --- |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2014.41.17@2x-20201111-194133.png?version=1&modificationDate=1605123706591&cacheVersion=1&api=v2) | ![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2014.48.52@2x-20201111-194908.png?version=1&modificationDate=1605124157746&cacheVersion=1&api=v2) | ![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2014.52.22@2x-20201111-195238.png?version=1&modificationDate=1605124390642&cacheVersion=1&api=v2) |

| **Azure DevOps** | **AWS Code Commit** |
| --- | --- |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2014.41.56@2x-20201111-194208.png?version=1&modificationDate=1605123738388&cacheVersion=1&api=v2) | ![](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/CleanShot%202020-11-11%20at%2014.46.04@2x-20201111-194620.png?version=1&modificationDate=1605123984893&cacheVersion=1&api=v2) |

* * *

## Show integration type + org/owner name + repo name in lists of repositories

05 Feb 2020 NEW FEATURE ALL USERS

Integration type icons and org/group names have been added to user facing repository selectors to help distinguish between similarly named repositories across different git servers and orgs/groups.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/CleanShot%202020-11-11%20at%2015.06.42@2x-20201111-200706.png?version=1&modificationDate=1605125230566&cacheVersion=1&api=v2&width=510&height=210)

* * *

## Display name for integrations and repositories

02 Feb 2020 IMPROVEMENT ADMINS

Jira administrators can now edit the names of integrations and repositories that are shown in Jira Cloud.

[display-name-feature.mov](https://bigbrassband.atlassian.net/wiki/download/attachments/871792645/display-name-feature.mov?version=1&modificationDate=1605047598752&cacheVersion=1&api=v2&width=578)

**Tip:** Use the Display Name feature to record information about the git server account.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/871792645/CleanShot%202020-11-10%20at%2017.36.53@2x-20201110-223701.png?version=3&modificationDate=1605047881789&cacheVersion=1&api=v2&width=204&height=110)

* * *
