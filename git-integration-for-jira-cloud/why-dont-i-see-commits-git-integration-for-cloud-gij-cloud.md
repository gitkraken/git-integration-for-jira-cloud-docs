---

title: Why don't I see commits? (Git Integration for Cloud)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
![](/wp-content/uploads/gij-troubleshoot-how-do-i-see-commits-top.png)

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center><b>Check if Git Integration for Jira app is installed, licensed and active</b> <b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b></p>

1.  Follow the [link](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) to install from the Atlassian Marketplace. You can verify that the Git Integration for Jira Cloud app is installed by visiting

    Jira Settings ➜ Apps ➜ **Manage apps**.

2.  Verify that the license is valid and that the application is active (installed, subscription is active).

<img src='/wp-content/uploads/gij-troubleshoot-manage-apps.png' style='max-width:100%;margin:25px auto;display:block' />

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center>Git Integration for Jira Cloud is installed, licensed and active</p>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center><b>Check if user has "Development Tools" permission</b> <b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b></p>

Using the **Permission Helper** within Jira Cloud - verify that the user in question has the **Development Tools** permission.

The Permission Helper is available to Jira admins: Jira settings ➜ System ➜ Permission Helper.

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/21vd3arsj6?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/21vd3arsj6'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center>Permissions are correct</p>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center><b>Check if repository with commit is connected to Jira</b> <b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b></p>

A couple ways to do this:

*   Via integration in Manage Git Repositories

    ![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-via-repo-1.png)

    ![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-via-repo-2.png)

*   Via Repository Browser (shows the list of all the repositories that are connected in one list

    ![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-reindex-since-commit.png)

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center>The repository with the missing commit is connected</p>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center><b>Check if repository has been reindexed since commit</b> <b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b></p>

Reindexing integrations (or repositories) manually. Note: all repositories are updated regularly without any manual updating required.

Approximately every 8-15 minutes.

![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-reindex-manually.png)

Admins can setup webhooks to index commits immediately

![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-webhooks.png)

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center>The repository has indexed since the commit was pushed</p>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center><b>Check if repository is associated with Jira project</b> <b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b></p>

It allows an admin to associate an integration (and all the repositories) or just a single repository to a set of Jira projects (one, many, or all).

Go to Manage Git Repositories ➜ Project Permissions.

Check "Associate all projects" if you want the repository to be associated with all Jira projects.

![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-associate-projects.png)

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center>The Jira project is associated with the repository</p>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center><b>Check if commit has a valid Jira issue key</b></p>

The association between Jira issues and commits is created by adding the Jira issue key (ABC-123 or MAIN-345) in the commit message.

Example commit messages:

**```ABC-123 added a bug fix```**

**```MAIN-345 adding important new feature.```**

Valid Jira issue key examples are shown in the following screenshot:

![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-valid-key.png)

GitLab showing an actual commit and the commit message:

![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-gitlab.png)

Check the video for more instructions:

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/cs229y2gzj?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin:10px 0 30px 0'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/cs229y2gzj'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center>Commit has a valid Jira issue key</p>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center><b>Try to find indexed commit in Jira Cloud</b></p>

The commit may be indexed by Jira Cloud - but not associated with any Jira issues. You can verify this with the following steps:

1.  Navigate to **View All Repositories** 

2. Find the repository and then the indexed commit (may need to select the branch)

If you find the commit - you can then fix commit association by clicking on **Change**.

![](/wp-content/uploads/gij-troubleshoot-try-to-find-indexed-commits-in-jira.gif)

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center>Commit is indexed</p>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center><b>Try to find indexed commit in Jira Cloud</b></p>

Check if commit is showing now

Where you can see commits:

*   New Jira issue view

    ![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-new-jira.png)

*   Old Jira issue view

    ![](/wp-content/uploads/gij-troubleshoot-idontsee-commits-old-jira.png)

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center>I still do not see my commits</p>

<p style='font-size:26px;text-align:center;'>&#8681;</p>

<p align=center>Contact <a href='mailto:support@bigbrassband.com'>support@bigbrassband.com</a> by email or via the <a href='https://bigbrassband.atlassian.net/servicedesk/customer/portals'>BigBrassBand Support Portal</a>.

