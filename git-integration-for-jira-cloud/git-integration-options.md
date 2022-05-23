---

title: Git integration options
description:
taxonomy:
    category: git-integration-for-jira-cloud

---


# Git integration options

<https://bigbrassband.atlassian.net/spaces/GITCLOUD/pages/1207829137/Git+integration+options>

* * *

This setting is part of the [**General Settings**](/git-integration-for-jira-cloud/General-Settings) configuration page for Git Integration for Jira Cloud.


These settings will take effect at integration level for projects with connected GitLab/GitHub git hosts. The default state for each setting is _enabled_.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1207829137/gitcloud-gencfg-git-integration-options.png?version=1&modificationDate=1645097188275&cacheVersion=1&api=v2&width=566&height=368)


**What’s on this page:**

## Git integration settings

|     |
| --- |
| ### Enable create \| delete branch |
| This setting shows or hides the function for creating/deleting of branches. The ability to create/delete selected branches from the Jira developer panel is dependent on this setting.<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1207829137/gitcloud-dev-panel-create-branch-sel.png?version=1&modificationDate=1643340514593&cacheVersion=1&api=v2&width=296&height=208) |
| ### Enable create pull \| merge request |
| This setting shows or hides the function for creating pull/merge requests from the Jira developer panel.<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1207829137/gitcloud-dev-panel-create-PRMR-sel.png?version=1&modificationDate=1643340576227&cacheVersion=1&api=v2&width=296&height=208) |

## Branch name template

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1207829137/gitcloud-gencfg-branch-name-template.png?version=1&modificationDate=1645097379618&cacheVersion=1&api=v2&width=566&height=119)

Set the **Branch Name Template** using the supported variables. Use the template to generate a default name for newly-created branches with the Create Branch dialog via the development panel of the Jira issue. Click/expand **Examples** to view template structure examples.

Use the following template variables:

|     |
| --- |
| `${issuetype}` – Issue Type. The Issue type is used to map a custom issue type as part of the template. The mapping pattern should look like this:<br><br>```java<br>${issuetype:type0,subsitute0[,type1,substitute1,...,typeN,substituteN][,defaultsubstitute]}<br>```<br><br>*   `typeN` - is the _**nth**_ issue type string to match.<br>    <br>*   `substituteN` - is the substitution string to use for _**typeN**_.<br>    <br>*   `defaultsubstitute` - is the substitution string to use if _**typeN**_'s match is not found. If _**defaultsubstitute**_ is blank, the lowercase version of the defined issue type is used. |
| `${issuekey}` – Issue Key. The Issue key is used in upper case. |
| `${summary}` – Issue Summary. The Summary is used from the current Jira issue your are on and will be in lowercase; spaces are substituted by "-" (dash). |
| **The Git Integration for Jira app default is:**  <br>`${issuekey}-${summary}`<br><br>This generates the string format like "**PRJ-123-add-more-logging**" as a default value for the Create Branch and Pull/Merge Request dialogs. Where `PRJ-123` is the issue key followed by a hyphen then the summary text of the active issue page (in hyphenated lowercase form). |
| `${sourcebranch}` – Source branch. The source branch from the Create Branch dialog is used and will be in lowercase; spaces are substituted by “-” (dash). |
| `${projectkey}` – Project Key. The Project key is used and will be in uppercase. |
| `${displayname}` -- This is the displayed name of the current user. |

## Branch name templates inner separator

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1207829137/gitcloud-gencfg-branch-name-temp-inner-sep.png?version=1&modificationDate=1645097573430&cacheVersion=1&api=v2&width=512&height=97)

This setting applies which inner word separator to use for the branch name template. The default setting is `"-" (dash)`.

## Max branch name length

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1207829137/gitcloud-gencfg-branch-name-length.png?version=1&modificationDate=1645097669336&cacheVersion=1&api=v2&width=511&height=73)

This setting allows administrators to specify the maximum character length for branch names. The default value is **250** chars.

* * *

## Some examples

|     |
| --- |
| **Example 1:** |
| `${issuetype}/${issuekey}-${summary}` |
| This generates the string format like "**newfeature/PRJ-123-add-more-logging**" as a default value for the branch names. Where `newfeature` is the actual issue type of the active Jira issue; in lowercase and trimmed of whitespaces, `PRJ-123` is the issue key followed by a hyphen then the summary text of the active issue page (in hyphenated lowercase form). |

|     |
| --- |
| **Example 2:** |
| `${issuetype:New Feature,feature,Bug Fix,bug}/${issuekey}-${summary}` |
| This generates the string format like "**feature/PRJ-123-add-more-logging**" as a default value for the branch names. This example uses a Jira issue which has the _**New Feature**_ issue type -- where `feature` is the substituted to _issuetype_ since _type0_ matches the active Jira issue type; `PRJ-123` is the issue key followed by a hyphen then the summary text of the active issue page (in hyphenated lowercase form). |

|     |
| --- |
| **Example 3:** |
| `${issuetype:Old Issue,old,Bug Fix,bug,branch}/${issuekey}-${summary}` |
| This generates the string format like "**branch/PRJ-123-add-more-logging**" as a default value for the branch names. This example uses a Jira issue which has the _**New Feature**_ issue type -- where `branch` is substituted to _issuetype_ since _type0..typeN_ does not match the active Jira issue type; `PRJ-123` is the issue key followed by a hyphen then the summary text of the active issue page (in hyphenated lowercase form). |

After all the settings have been configured according to your requirements, click **Update** to apply the changes.

