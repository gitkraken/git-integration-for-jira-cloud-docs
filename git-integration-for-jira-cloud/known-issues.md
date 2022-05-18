---

title: Known Issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The Git Integration for Jira app is packed with features that makes Jira administrators and developers happy. However, with different hardware configurations out there, these great features can also become burdened by issues.

Below are the Git Integration app known issues and workarounds:

|     |
| --- |
| #### **Number of connected repositories per integration** |
| GIT INTEGRATION: JIRA CLOUD<br><br>The Git Integration for Jira app have per integration limitation for number of connected repositories:<br><br>*   GitHub - 5000<br>    <br>*   GitLab - 5000<br>    <br>*   All others - 5000<br>    <br><br>_Reference: GITCL-1395, GITCL-1846_ |

|     |
| --- |
| #### **2GB object Git repositories storage limit** |
| GIT INTEGRATION: JIRA CLOUD<br><br>The Git Integration for Jira application uses the JGit library which does not support objects over 2GB in size stored in git repositories.<br><br>*   2GB object limit<br>    <br><br>Reference: … |

|     |
| --- |
| #### **Smart commits failing user search by email** |
| GIT INTEGRATION: JIRA CLOUD<br><br>It was reported that some users have their smart commits attributed to the app user rather than specific users. It is found that the user search via email is failing. Some Jira Cloud instances are failing to return users based on email.<br><br>**Workaround:**  <br>Use `/rest/api/2/user/assignable/search?issueKey=ABC-123` to return a list of assignable users for an issue - if the user search by email fails.<br><br>_Reference: GITCL-800_ |

|     |
| --- |
| #### **Microsoft pull request requirement for status updates** |
| GIT INTEGRATION: JIRA CLOUD<br><br>Microsoft integrations require all pull requests for the configured repositories to be requested each time for status updates. Microsoft's Pull Request APIs do not currently provide any information allowing for filtering by last changed date/time.<br><br>_Reference:_ GIT-3889 |
|     |

|     |
| --- |
| #### **Why Microsoft PAT integrations require “All accessible organizations” permission** |
| GIT INTEGRATION: JIRA CLOUD  <br>IMPORTANT!<br><br>It is highly required that administrators must select the “All accessible organizations” option when creating personal access tokens (PAT). Otherwise, the integration will not work.<br><br>Please follow the instructions for creating MS/Azure PATs outlined in our Confluence how-tos [here](/wiki/spaces/BBBSUPPORT/pages/136904881/Creating+Personal+Access+Tokens).<br><br>For more information, see the [**official reference for Azure DevOps PAT integration**](https://developercommunity.visualstudio.com/content/problem/902833/azure-devops-personal-access-token-does-).<br><br>_Reference:_ GIT-3978 |

|     |
| --- |
| #### **SSH single Git repository integration is not generating the trigger for Jira Automation** |
| GIT INTEGRATION FOR JIRA CLOUD<br><br>In Automation for Jira, a user can create a rule or set of rules to start a trigger. These triggers will run the rules while listening to events; such as when a commit or branch is created.<br><br>This feature works well for auto-connected integrations and [single HTTPS authenticated git repositories](/wiki/spaces/GITCLOUD/pages/923238448), but single repositories authenticated via [SSH connection](/wiki/spaces/GITCLOUD/pages/923238489) are not supported by Atlassian Jira Cloud (Atlassian bug issue: [JSWCLOUD-20935](https://jira.atlassian.com/browse/JSWCLOUD-20935)).<br><br>If you use Jira automation triggers, we strongly recommend to use HTTP/HTTPS connections for single repository git URL. _(See below)_ |
| Using this git URL will make triggers to ignore commit event:<br><br>```java<br>git@github.com:admin/admin-test-repo-one.git<br>```<br><br>Using the HTTPS git URL works:<br><br>```java<br>https://github.com/admin/admin-test-repo-one.git<br>```<br><br>_Reference: GITCL-1624_ |

|     |
| --- |
| #### **Tags taking longer than 10s to load on an issue will timeout** |
| GIT INTEGRATION: JIRA CLOUD<br><br>Loading tags in Jira is a very resource-intensive operation and usually occurs on integrations with repositories with large git history – which can take a very long time to process/load.<br><br>Currently, the GIt Integration for Jira Cloud app limits loading of tags to **10 seconds** before timing out. |

|     |
| --- |
| #### **Left Git Integration options panel takes up to 10 seconds to load** |
| The left sidebar for the Git Integration for Jira app panel takes up to 10 seconds to load.<br><br>![](https://bigbrassband.atlassian.net/wiki/download/attachments/591986707/left-sidebar-loading-delay-bug-example.png?version=1&modificationDate=1622733576577&cacheVersion=1&api=v2)<br><br>Atlassian has opened a public [bug ticket](https://ecosystem.atlassian.net/browse/ACJIRA-2415) for this issue. |

|     |
| --- |
| #### **Duplicate SC commands #comment and #time with both BBB and Atlassian SC enabled** |
| GIT INTEGRATION: JIRA CLOUD<br><br>In Jira Cloud, there are two possible Smart Commit processors: Jira Cloud and BigBrassBand.<br><br>In the Git Integration for Jira Cloud: General settings, there are two options for processing Smart commits:<br><br>*   Atlassian – which supports `#comment`, `#time`, and `#<transition>`<br>    <br>*   BigBrassBand – which supports `#comment`, `#time`, and `#<transition>`, `#assign` and `#label`.<br>    <br><br>If both are enabled, the user will see duplicate `#comment` and `#time`.<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/591986707/gitcloud-gencfg-dup-smart-commits-sel.png?version=1&modificationDate=1634440501925&cacheVersion=1&api=v2&width=680&height=212)<br><br>We set the default to the Atlassian smart commit processor to enabled because it is bundled with the workflow triggers (a valuable feature). In addition, the Atlassian processor does most of the SC features plus the workflow triggers.<br><br>If the admin decides to use the BigBrassBand processing, users will be able to use the additional smart commit commands (`#assign` and `#label`). However, choosing this path drops support for workflow triggers.<br><br>_Reference: GITCL-1334_ |