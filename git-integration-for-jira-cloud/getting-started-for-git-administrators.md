---

title: Getting started for Git administrators
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923023183/bbb-overview.png?version=1&modificationDate=1630063544665&cacheVersion=1&api=v2)

# Welcome Git Admin!

You are probably reading this page because a Jira administrator has requested access to the Git server. The Jira administrator has installed the Git Integration for Jira app.

**What’s on this page:**

* * *

## What is the Git Integration for Jira app?

The Git Integration for Jira app pulls data from a Git source code control repository. Jira users will be able to see code in Git in context with Jira projects and issues. Even non-technical users will be able to see Git in the familiar Jira interface.

Jira users will be able to securely browse content in Git without requiring you to create IDs for every user.

## How does Jira interact with the Git server?

The Git Integration for Jira app acts as a regular Git client. It performs a scheduled pull from the repository.

## What does the Jira administrator need?

The Jira administrator needs the ability to clone the repository and pull from it just like a regular developer workstation would do.

We recommend that you create a new user identity specifically for this Jira server.

|     |
| --- |
| ### For Git repositories with HTTP/HTTPS access |
| Please do the following:<br><br>1.  Create a new user for the Jira server.<br>    <br>2.  Send the Jira administrator:<br>    <br><br>*   The URL to the Git server<br>    <br>*   _For example:_  `https://gitserver/repo/timetrackingproject.git`<br>    <br>*   The username and password for the user you created |

|     |
| --- |
| ### For Git repositories with SSH access |
| Please do the following:<br><br>1.  Define a new SSH public/private key pair for the Jira server<br>    <br>2.  Install the public key on the Git server<br>    <br>3.  Send the Jira administrator:<br>    <br><br>*   The URL to the Git server<br>    <br>*   _For example:_  `git@gitserver:repo/timetrackingproject.git`<br>    <br>*   The private key you created |

|     |
| --- |
| ### For Git repositories with Git protocol access |
| Send the Jira administrator the URL to the Git server.<br><br>For example:  `git://gitserver/repo/timetrackingproject.git` |

## Troubleshooting issues

For information on troubleshooting known errors and issues, see [Git Integration for Jira - Knowledge Base/FAQ](https://bigbrassband.com/faqs-sel.html) and [Troubleshooting guides](/wiki/spaces/GITSERVER/pages/128221244/Troubleshooting+articles).

## Classic and webhook indexing

Classic indexing refers to an internal process which runs in a set amount of time to review repositories eligible to be checked for changes. For more information on how this works, see [Classic indexing explainer](/wiki/spaces/GITCLOUD/pages/183369754/Classic+Indexing+Explainer).

Webhook indexing refers to automatic indexing designed to record changes in a timely manner for all types of repositories resulting in immediate reindex times. For more information on how this works, see [Webhook indexing explainer](/wiki/spaces/GITCLOUD/pages/1422819484/Webhook+Indexing+Explainer).

[« Installation](/wiki/spaces/GITCLOUD/pages/1923023014/Installation)

[Setup GitLab Server to respond to incoming network API calls »](/wiki/spaces/GITCLOUD/pages/1923023297/Setup+GitLab+Server+to+respond+to+incoming+network+API+calls)

## More related topics about getting started for Jira admins

*   Page:

    [New GitLab v10+ authentication](/wiki/spaces/GITCLOUD/pages/1923023311) (Git Integration for Jira Cloud)

*   Page:

    [Setup GitLab Server to respond to incoming network API calls](/wiki/spaces/GITCLOUD/pages/1923023297/Setup+GitLab+Server+to+respond+to+incoming+network+API+calls) (Git Integration for Jira Cloud)

*   Page:

    [Setting up web linking](/wiki/spaces/GITCLOUD/pages/1923023467/Setting+up+web+linking) (Git Integration for Jira Cloud)

*   Page:

    [Setting up indexing triggers](/wiki/spaces/GITCLOUD/pages/1923023481/Setting+up+indexing+triggers) (Git Integration for Jira Cloud)


* * *

|     |
| --- |
| **Get new product notifications and feature updates from BigBrassBand LLC.** |
| [Click here to subscribe to our mailing list](http://eepurl.com/hhfbwz) |

Need to know more features?  Read next:  [Helpful Tips for Jira Administrators](https://bigbrassband.com/tips-for-jira-admins.html)