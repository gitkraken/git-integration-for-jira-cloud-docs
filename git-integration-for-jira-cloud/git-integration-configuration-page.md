---

title: Git integration configuration page
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/m1k2sol0a5) _to open this video in a new browser tab for more viewing options._


On this page, you will be able to setup your git repositories and connect them to Jira. Click **Add integration** to get started.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024023/gitcloud-managed-ui-getting-started.png?version=1&modificationDate=1647866199013&cacheVersion=1&api=v2)

* * *

|     |
| --- |
| ### Git service integration (Recommended) |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024023/gitcloud-managed-ui-git-service-sel.png?version=1&modificationDate=1647930706531&cacheVersion=1&api=v2) |
| Formerly known as Full feature auto-connect integration.<br><br>Use this type of integration to connect specific git host services to Jira. This integration supports multiple connected repositories and automates most git integration settings.<br><br>**We highly recommend this type of integration for multiple repository configuration.**<br><br>For more details on supported git host services, see the full feature integration section in our Integration Guides.<br><br>**GitLab**  <br>Support for Gitlab API v3 is deprecated. We recommend to use **GitLab API v4** when adding new integrations for increased security. |

|     |
| --- |
| ### Webhook indexing integration |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024023/gitcloud-managed-ui-webhook-idx-sel.png?version=1&modificationDate=1647930808726&cacheVersion=1&api=v2) |
| Connect directly to a Git service by configuring webhooks to push commit, branch, pull request, and tag data to Jira Cloud.<br><br>Webhook indexing integration allows your connected git servers to work behind a firewall. However, the downside is that your integration will have limited features. For now, the supported git servers are GitHub.com, GitLab and Microsoft. More will be coming in the future. |

|     |
| --- |
| ### Single git repository integration |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024023/gitcloud-managed-ui-single-repo-sel.png?version=1&modificationDate=1647930891191&cacheVersion=1&api=v2) |
| Manually connect single git repositories using this setup such as git protocol, SSH, HTTP/HTTPS, etc. or simply connect one specific repository. |


Connected git service integrations appear in the Manage integration configuration list.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024023/gitcloud-managed-ui-integration-list.png?version=1&modificationDate=1647933667463&cacheVersion=1&api=v2)

*   Use the search option and filter to control integration list display.

*   Use the checkbox to specifically select integration/repositories from the list. Pair this with actions to perform multiple configuration for selected items.

*   Use the column headers to sort the list in ascending or descending order.

*   Use ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Actions** to manage integration/repository settings.


The above UI descriptions also apply to the Manage repositories page since it has a similar layout.

|     |
| --- |
| ### Reindex selected (formerly Reindex All) |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024023/gitcloud-managed-ui-reindex-all.png?version=1&modificationDate=1647934041821&cacheVersion=1&api=v2) |
| UPDATE  <br>In the new managed user interface, the Reindex all function is further improved and superseded by selecting one or more integration/repositories using the checkboxes and then ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Reindex selected**.<br><br>This function will perform a reindex queue of all the selected integration/repository from the list.<br><br>**Note**  <br>Reindex will ignore disabled integrations. Enable them first to run reindex on these integrations.<br><br>  <br>For more information on this topic, see [Reindexing](/wiki/spaces/GITCLOUD/pages/1923026060/Reindexing). |

|     |
| --- |
| ### Other features |
| Click the **…** to see other features such as Repository browser and General settings. |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024023/gitcloud-managed-ui-other-features.png?version=1&modificationDate=1647935460986&cacheVersion=1&api=v2) |
| The rest of the features can also be accessed on the left sidebar. |
| ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923024023/gitcloud-managed-ui-other-features-sidebar.png?version=1&modificationDate=1647935812707&cacheVersion=1&api=v2&width=680&height=413) |


Click on the next » topic below (recommended) to learn about adding a new full feature integration in Jira.

[« Setting up repositories (topic index)](/wiki/spaces/GITCLOUD/pages/1923023982/Setting+up+integrations)

[Using the Git service integration wizard »](/wiki/spaces/GITCLOUD/pages/1923024112/Using+the+Git+service+integration+wizard)

### More topics about setting up integration

*   Page:

    [Git integration configuration page](/wiki/spaces/GITCLOUD/pages/1923024023/Git+integration+configuration+page) (Git Integration for Jira Cloud)

*   Page:

    [Using the Git service integration wizard](/wiki/spaces/GITCLOUD/pages/1923024112/Using+the+Git+service+integration+wizard) (Git Integration for Jira Cloud)

*   Page:

    [Using the Single git integration wizard](/wiki/spaces/GITCLOUD/pages/1923024154/Using+the+Single+git+integration+wizard) (Git Integration for Jira Cloud)

*   Page:

    [Managing integration or repository configuration](/wiki/spaces/GITCLOUD/pages/1923024455/Managing+integration+or+repository+configuration) (Git Integration for Jira Cloud)