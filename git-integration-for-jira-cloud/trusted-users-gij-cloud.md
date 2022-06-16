---

title: Trusted Users - Administration
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

**What's on this page:**
- [Introduction](#introduction)
- [Inviting a User and Assigning a Role](#inviting-a-user-and-assigning-a-role)
- [Changing the Role of a User](#changing-the-role-of-a-user)

* * *

## Introduction

Trusted users are users that are able to invite other users and have administrative permissions. They can see all pages of the Git Integration app. Once a user is assigned the **Trusted** role, adding this user to the `jira-administrators` group will not change the access to the [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app because the **Trusted** role is considered to be a Jira administrator.

Jira administrators can grant certain users the **Trusted** role via invite and then later on can change the role according to your organization rules.

## Inviting a User and Assigning a Role

On your Jira dashboard, go to ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Jira Administration** ➜ **User Management**.

![Jira Cloud menu Administration accessing User Management](https://bigbrassband.atlassian.net/wiki/download/attachments/792002572/gitcloud-jira-admin-user-mgr-menu-access.png?version=1&modificationDate=1601548276316&cacheVersion=1&api=v2)

On the following screen, click **Invite Users**.

![Jira user management screen](https://bigbrassband.atlassian.net/wiki/download/attachments/792002572/gitcloud-jira-admin-user-mgr-invite.png?version=1&modificationDate=1601549065688&cacheVersion=1&api=v2)

The next screen is displayed.

![Invite users screen selecting the Trusted role](https://bigbrassband.atlassian.net/wiki/download/thumbnails/792002572/gitcloud-jira-admin-invite-users.png?version=1&modificationDate=1601549598293&cacheVersion=1&api=v2&width=507&height=710)

Enter a user’s email address or several email addresses of the users to be assigned with the role.

Under the **Role** dropdown, choose **Trusted**.

Click **Invite # user(s)** to complete this setup.

## Changing the Role of a User

Go to **Jira Administration** ➜ **User Management**.

Scroll to the bottom of the page to find the list of users.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/792002572/gitcloud-user-mgr-userlist.png?version=1&modificationDate=1601550877546&cacheVersion=1&api=v2)

Click **Show details** or click **…** then **Show details**. The next screen is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/792002572/gitcloud-user-show-details-roles.png?version=1&modificationDate=1601551488708&cacheVersion=1&api=v2&width=476&height=518)

Click the Role dropdown then select **Trusted**. The role is automatically applied once granted.

