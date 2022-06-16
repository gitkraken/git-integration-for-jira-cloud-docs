---

title: Why don't I see commits? (Git Integration for Cloud)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
![](https://bigbrassband.atlassian.net/wiki/download/attachments/110755841/Asset%202@5x_1.png?version=4&modificationDate=1554913758813&cacheVersion=1&api=v2)



JIRA ADMIN

- Check if Git Integration for Jira app is installed, licensed and active

Follow the [link](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) to install from the Atlassian Marketplace. You can verify that the Git Integration for Jira Cloud app is installed by visiting

Jira Settings → Apps → Manage apps.

Verify that the license is valid and that the application is active (installed, subscription is active).   

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/manage-apps.png?version=1&modificationDate=1553619498618&cacheVersion=1&api=v2&width=800&height=388) 

Git Integration for Jira Cloud is installed, licensed and active

JIRA ADMIN

- Check if user has “Development Tools” permission

Using the **Permission Helper** within Jira Cloud - verify that the user in question has the **Development Tools** permission.

The Permission Helper is available to Jira admins: Jira settings → System → Permission Helper.

Permissions are correct

JIRA ADMIN

- Check if repository with commit is connected to Jira

A couple ways to do this:

*   Via integration in Manage Git Repositories

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/via-repo-1.png?version=3&modificationDate=1554317873812&cacheVersion=1&api=v2&width=800&height=388)

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/via-repo-2.png?version=4&modificationDate=1554318008865&cacheVersion=1&api=v2&width=800&height=388)

*   Via Repository Browser (shows the list of all the repositories that are connected in one list

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/reindex-since-commit.png?version=3&modificationDate=1554317871781&cacheVersion=1&api=v2&width=800&height=388)

The repository with the missing commit is connected

JIRA ADMIN

- Check if repository has been reindexed since commit

Reindexing integrations (or repositories) manually. Note: all repositories are updated regularly without any manual updating required.

Approximately every 8-15 minutes.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/reindex-manually.png?version=3&modificationDate=1554317862621&cacheVersion=1&api=v2&width=800&height=388)

Admins can setup webhooks to index commits immediately

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/webhooks.png?version=3&modificationDate=1554317885518&cacheVersion=1&api=v2&width=800&height=388)

The repository has indexed since the commit was pushed

JIRA ADMIN

- Check if repository is associated with Jira project

It allows an admin to associate an integration (and all the repositories) or just a single repository to a set of Jira projects (one, many, or all).

Go to Manage Git Repositories → Project Permissions. 

Check "Associate all projects" if you want the repository to be associated with all Jira projects.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/associate-projects.png?version=2&modificationDate=1554319092373&cacheVersion=1&api=v2&width=800&height=388)

The Jira project is associated with the repository

- Check if commit has a valid Jira issue key

The association between Jira issues and commits is created by adding the Jira issue key (ABC-123 or MAIN-345) in the commit message.

Example commit messages:

**```ABC-123 added a bug fix```**

**```MAIN-345 adding important new feature.```**



Valid Jira issue key examples are shown in the following screenshot:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/valid-key.png?version=1&modificationDate=1554322237274&cacheVersion=1&api=v2&width=800&height=388)

GitLab showing an actual commit and the commit message:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/gitlab.png?version=1&modificationDate=1554322268762&cacheVersion=1&api=v2&width=800&height=388)

Check the video for more instructions:

Commit has a valid Jira issue key

 - Try to find indexed commit in Jira Cloud

The commit may be indexed by Jira Cloud - but not associated with any Jira issues. You can verify this with the following steps:

1. Navigate to **View All Repositories** 

2\. Find the repository and then the indexed commit (may need to select the branch)

If you find the commit - you can then fix commit association by clicking on **Change**.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/5.gif?version=1&modificationDate=1553533096032&cacheVersion=1&api=v2&width=800&height=429)

Commit is indexed

 - Check if commit is showing now

Where you can see commits:

*   New Jira issue view

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/new-jira.png?version=1&modificationDate=1554323932219&cacheVersion=1&api=v2&width=800&height=388)

*   Old Jira issue view

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/110755841/old-jira.png?version=1&modificationDate=1554323933624&cacheVersion=1&api=v2&width=800&height=388)

I still do not see my commits

Contact [support@bigbrassband.com](mailto:support@bigbrassband.com) by email or via the [BigBrassBand Support Portal](https://bigbrassband.atlassian.net/servicedesk/customer/portals)
