---

title: Associating project permissions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Integrations and/or repositories can be associated with one or more Jira projects to restrict which users can view development information. All newly-connected repositories or integrations are associated with all Jira projects by default.

This feature is displayed on the following locations:

*   REPOSITORY Manage repositories page ➜ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ Edit repository ➜ **Feature settings**.

*   INTEGRATION Manage integration page ➜ ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ Edit integration ➜ **Feature settings**.


![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923024786/gitcloud-project-permissions-setting.png?version=1&modificationDate=1633705526768&cacheVersion=1&api=v2&width=674&height=176)

**Restrict to projects**  –  One or more projects can be mapped to this repository or integration to make Git Commits tabs available in the Issue pages of the associated projects. Disable _**Associate with all projects**_ option to gain access to this field.

**Associate with all projects**  –  Enable this option to associate this repository or integration to all projects. Disable this option if you want to use the existing mapped projects from the **Restrict to projects** field. The default setting is enabled _(checked)_.

## Project permissions level

There are several types of project permission levels, namely:

### Repository level

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/xvzj32nxou) _to open this video in a new browser tab for more viewing options._
(_Updated video coming soon_)


You can configure the project permissions for single connection repositories:

1.  On the Manage repositories page, click ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Edit repository**.

2.  On the page that appears, scroll down to **Project Permissions**.

3.  Uncheck (turn off) the **Associate with all projects** setting.

4.  Click on the **Restrict to projects** field then select one or more projects from the list.

5.  Click **Update** to save the settings.


The same process can also be applied for other single repository connections in Jira Cloud.

### Integration level

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/rnm5t639cz) _to open this video in a new browser tab for more viewing options._
(_Updated video coming soon_)


You can configure the project permissions for integration (multiple repository connection):

1.  On the Manage integrations page, click ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Edit integration**.

2.  On the page that appears, click **Feature settings** on the sidebar then scroll down to the **Project Permissions** section.

3.  Uncheck (turn off) the **Associate with all projects** setting.

4.  Click on the **Restrict to projects** field then select one or more projects from the list.

5.  Click **Update** to save the settings.


### Repository level within integration

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/fder2qnpgw) _to open this video in a new browser tab for more viewing options._
(_Updated video coming soon_)


You can configure the project permissions for repositories within integration:

1.  On the Manage repositories page, click ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Actions ➜ **Edit integration** for a repository that is part of the integration (which can be identified with the Integration column).

    *   For easy access, use the integration dropdown selector.

        ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024786/gitcloud-manage-integrations-actions-selector(c).png?version=1&modificationDate=1650280023564&cacheVersion=1&api=v2)
2.  Click a repository name (under the Repository column) to directly open its repository settings.

3.  On the page that appears, scroll down to **Project Permissions**.

4.  Uncheck (turn off) the **Associate with all projects** setting.

5.  Click on the **Restrict to projects** field then select one or more projects from the list.

6.  Click **Update** to save the settings.


## Setting project permissions in Jira Cloud

Project permissions are now available in Git Integration for Jira Cloud. The default setting for new repository/integration connections is **Associated with all Jira projects**.

Whenever the **integration** settings for project permissions are updated, the repository settings will be overwritten.


Watch the video below to learn different settings for each project permissions level.

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/nnao2x4ses) _to open this video in a new browser tab for more viewing options._
(_Updated video coming soon_)

[« Viewing indexing properties](/wiki/spaces/GITCLOUD/pages/1923024741)

[View repository indexing logs »](/wiki/spaces/GITCLOUD/pages/2013626625/View+repository+indexing+logs)

### More topics about setting up repositories

*   Page:

    [Git integration configuration page](/wiki/spaces/GITCLOUD/pages/1923024023/Git+integration+configuration+page) (Git Integration for Jira Cloud)

*   Page:

    [Using the Git service integration wizard](/wiki/spaces/GITCLOUD/pages/1923024112/Using+the+Git+service+integration+wizard) (Git Integration for Jira Cloud)

*   Page:

    [Using the Single git integration wizard](/wiki/spaces/GITCLOUD/pages/1923024154/Using+the+Single+git+integration+wizard) (Git Integration for Jira Cloud)

*   Page:

    [Managing integration or repository configuration](/wiki/spaces/GITCLOUD/pages/1923024455/Managing+integration+or+repository+configuration) (Git Integration for Jira Cloud)