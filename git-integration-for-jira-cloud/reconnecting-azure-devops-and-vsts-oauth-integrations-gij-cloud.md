---

title: Reconnecting Azure DevOps and VSTS OAuth integrations
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
On March 2, 2022, all OAuth integrations between Git Integration for Jira and Azure DevOps and VSTS were interrupted. Our investigation found that Microsoft OAuth apps' client secrets expire after 5 years. This limitation has a single workaround and that is for all customers to reconnect. We apologize for this inconvenience and interruption in service. Below are steps to reconnect.

## Workaround: Reconnecting Azure DevOps and VSTS OAuth

Requirements:

1.  Jira administrator permissions

2.  Azure DevOps / VSTS account or service account.


Steps:

1.  Visit the **Manage Git repositories** screen in the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app

2.  Click on the integration name

3.  Click on Reconnect

4.  Login to Azure DevOps / VSTS with the account you wish to associate with Git Integration for Jira.


Videos:

[CleanShot2022-03-03 at 01.24.59.mp4](https://bigbrassband.atlassian.net/wiki/download/attachments/2079686657/CleanShot2022-03-03%20at%2001.24.59.mp4?version=1&modificationDate=1646288892990&cacheVersion=1&api=v2&width=210)

[CleanShot2022-03-03 at 01.26.20.mp4](https://bigbrassband.atlassian.net/wiki/download/attachments/2079686657/CleanShot2022-03-03%20at%2001.26.20.mp4?version=1&modificationDate=1646288879632&cacheVersion=1&api=v2&width=210)