---

title: Managing integrations via Actions (Jira Cloud)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
After integrating your repository or git host service, a set of Actions can be performed by clicking the ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) icon under the **Actions** column on the integration/repository configuration list.

## Action commands (integration)

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024517/gitcloud-manage-integration-actions-menu.png?version=3&modificationDate=1648984361910&cacheVersion=1&api=v2)

Utilize the following actions to manage integrations in Jira Cloud:

|     |     |
| --- | --- |
| **Action** | **Description** |
| _**Reindex integration**_ | Immediately starts the synchronization with the selected integration and its repositories. |
| _**Edit integration**_ | Opens the page to manage connection and feature settings for the selected integration. |
| _**Disable integration**_ | Disable specific integrations if you are not using them with Jira. Enable them again if you are going to use them later on. |
| _**View log**_**s** | Opens a dialog showing the indexing log of the selected integration. |
| _**Disconnect integration**_ | Disconnects the selected integration and removes its settings from the Git Integration for Jira Cloud app integration configuration page. |

The **Show integration repositories** command is deprecated and the displayed integration repositories are moved to the Manage repositories page.

Jump to [Edit integration](/wiki/spaces/GITCLOUD/pages/1923024559/Edit+integration) settings page documentation.

## Action commands (repositories)

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923024517/gitcloud-manage-repositories-actions-menu.png?version=1&modificationDate=1648984477536&cacheVersion=1&api=v2)

Utilize the following actions to manage repositories in Jira Cloud:

|     |     |
| --- | --- |
| **Action** | **Description** |
| _**Reindex repository**_ | Immediately starts the synchronization with the selected repository. |
| _**Edit repository**_ | Opens the page to manage connection and feature settings for the selected repository. |
| _**View log**_ | Opens a dialog showing the indexing log of the selected integration. |
| _**Disable repository**_ | Disable specific repositories if you are not using them with Jira. Enable them again if you are going to use them later on. |

**Disconnecting unused repositories**
Disconnect or disable selected repositories if they are not used for faster integration reindex.

To disconnect a repository integration (plain git), use the relative action command from the Manage integrations page instead to remove its settings and clone data from the Git Integration for Jira Cloud app integration configuration page.

Jump to [Edit repository](/wiki/spaces/GITCLOUD/pages/1977384961/Edit+repository) settings page documentation.

## Action commands (Group selection)

Group action becomes available when selecting multiple integrations and repositories. Thus, providing ease of use and streamlined processing of the selected items.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923024517/gitcloud-actions-group-selection-feature.png?version=1&modificationDate=1649145056712&cacheVersion=1&api=v2&width=680&height=349)

[« Managing repository or integration configuration](/wiki/spaces/GITCLOUD/pages/1923024455/Managing+integration+or+repository+configuration)

[Edit integration »](/wiki/spaces/GITSERVER/pages/1923028309/Edit+integration+feature+settings)

### More related topics about managing repository/integration configuration

*   Page:

    [Managing integration or repository configuration](/wiki/spaces/GITCLOUD/pages/1923024455/Managing+integration+or+repository+configuration) (Git Integration for Jira Cloud)

*   Page:

    [Managing integrations via Actions (Jira Cloud)](/wiki/spaces/GITCLOUD/pages/1923024517) (Git Integration for Jira Cloud)

*   Page:

    [Edit integration](/wiki/spaces/GITCLOUD/pages/1923024559/Edit+integration) (Git Integration for Jira Cloud)

*   Page:

    [SSL Verify](/wiki/spaces/GITCLOUD/pages/1923024654/SSL+Verify) (Git Integration for Jira Cloud)

*   Page:

    [Viewing indexing properties (Jira Cloud)](/wiki/spaces/GITCLOUD/pages/1923024741) (Git Integration for Jira Cloud)

*   Page:

    [Removing integration or repository configuration](/wiki/spaces/GITCLOUD/pages/1923024762/Removing+integration+or+repository+configuration) (Git Integration for Jira Cloud)

*   Page:

    [Associating project permissions](/wiki/spaces/GITCLOUD/pages/1923024786/Associating+project+permissions) (Git Integration for Jira Cloud)

*   Page:

    [Edit repository](/wiki/spaces/GITCLOUD/pages/1977384961/Edit+repository) (Git Integration for Jira Cloud)

*   Page:

    [View repository indexing logs](/wiki/spaces/GITCLOUD/pages/2013626625/View+repository+indexing+logs) (Git Integration for Jira Cloud)