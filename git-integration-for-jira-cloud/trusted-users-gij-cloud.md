---

title: Trusted Users
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

### Introduction

Trusted users are users that are able to invite other users and have administrative permissions. They can see all pages of the Git Integration app. Once a user is assigned the **Trusted** role, adding this user to the `jira-administrators` group will not change the access to the [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app because the **Trusted** role is considered to be a Jira administrator.

Jira administrators can grant certain users the **Trusted** role via invite and then later on can change the role according to your organization rules.

### Inviting a User and Assigning a Role

On your Jira dashboard, go to ![](/wp-content/uploads/actions-icon.png) Jira Administration ➜ **User Management**.

<img src='/wp-content/uploads/gij-gitcloud-jira-admin-user-mgr-menu-access-2025.png' style='display:block;margin:25px auto 35px auto;max-width:100%' alt='Jira Cloud menu Administration accessing User Management' />

On the following screen, click **Invite Users**.

<img src='/wp-content/uploads/gij-gitcloud-jira-admin-user-mgr-invite-2025.png' style='display:block;margin:25px auto 35px auto;max-width:100%' alt='Jira user management screen' />

The next screen is displayed.

<img src='/wp-content/uploads/gij-gitcloud-jira-admin-invite-users-2025.png' style='display:block;margin:25px auto 25px auto;max-width:100%' alt='Invite users screen selecting the Trusted role' />

*   Enter a user’s email address or several email addresses of the users to be assigned with the role.

*   Under the **Role** dropdown, choose **Trusted**.

*   Click **Invite # user(s)** to complete this setup.

### Changing the Role of a User

Go to ![](/wp-content/uploads/actions-icon.png) Jira Administration ➜ **User Management**.

Scroll to the bottom of the page to find the list of users.

<img src='/wp-content/uploads/gij-gitcloud-user-mgr-userlist-2025.png' style='display:block;margin:25px auto 25px auto;max-width:100%' />
