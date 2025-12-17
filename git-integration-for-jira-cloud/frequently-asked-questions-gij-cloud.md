---

title: Frequently Asked Questions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Find answers to questions asked by Git Integration for Jira app users, workarounds and solutions to help you get up and running. Use the table of contents below to jump to a specific topic.

Feel free to contact our [support team](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/) if you don't see what you're looking for.

&nbsp;

## On this page

- [General](#general)
- [Developer](#developer)
- [Installation and Setup](#installation-and-setup)
- [Administration](#administration)
- [Repositories](#repositories)
- [Workspace](#workspace)
- [SSH](#ssh)
- [Reindex](#reindex)
- [Uninstall and Reinstall](#uninstall-and-reinstall)
- [Purchase and Pricing](#purchase-and-pricing)
- [Support](#support)

&nbsp;
* * *
&nbsp;

## General

Frequently asked questions by users in general.

### What is Git?

Git is a source code repository. Developers keep track of their source code using Git. Git relies heavily on branching and merging. Branching is making a temporary copy of source code for a single purpose like adding a particular feature or fixing a bug. Merging is safely moving the changes from one branch back to another.

### What is this app?

This is Git Integration for Jira Cloud – an app for Jira that mashes together data from a Git server with your Jira Cloud. It let's people see code from Git in context with Jira issues.

### Why would I want to see Git in my Jira?

Git can be complicated and daunting – especially for non-developers.  Jira users want this app so they can work with Git in the familiar Jira interface.

### How do Git and Jira work together?

In organizations with Git and Jira, it is common to have a branch for each Jira issue and branches for every version.

When developers put their work in Git, they can include a Jira issue key in the comments. With the Git Integration for Jira app installed, Jira Cloud will then show the changes in the issue.

### Is this safe? Will it cause trouble?

It is a safe and well-tested plugin.

We test this on huge Git repositories in large Jira instances. Over 5000 organizations in 70 countries use the Git Integration for Jira app.

### Which version of Jira is compatible with Git for Jira Cloud app?

For a more comprehensive view, see **[Git Integration for Jira app Version History »](https://marketplace.atlassian.com/plugins/com.xiplink.jira.git.jira_git_plugin/versions "Git add-on Version History")**.

&nbsp;
* * *
&nbsp;

## Developer

Solutions targeted for developers.

### How do Git commits get associated with a Jira issue?

On every Git commit, make sure the message includes the exact issue ID at the beginning of the text. The Git Integration for Jira Cloud app will automatically index new commits and associate the referenced issue.

To create a link between your Git commit and a Jira issue, developers must include the issue key into the commit comment.

Example git commit message:

"`PROJ-913 - Plugin version change from 2.6.7 to 2.6.8`"; where **_PROJ-913_** is the issue key that links the commit message to the Jira issue.

### How do I ensure people are following our organization's process for source code?

Open the project summary in your browser and click on the **Git Commits** tab.

All changes that developers have submitted will be listed in reverse chronologically order.  From this view, you can audit all of the changes that developers have recently submitted.

### What will happen to commit associations if a Jira issue is moved to a new Jira project?

For GIJ Cloud users, moving Jira issues to a different project is not recommended, especially for repositories with extensive git commit histories. This is because associated git commits from the old project do not automatically transfer to the new project due to the different project key.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Git Integration for Jira Cloud app allows users to manually associate git commits to a Jira issue via the Repository browser.
    </div>
    </div>
</div>

To manually associate git commits to a Jira issue in Jira Cloud:

1.  Go to Jira dashboard menu Apps ➜ **Git Integration: Repository browser**.
2.  Click a repository to work on. The list defaults to the Compare view.
3.  Click on the **Commits** tab.
4.  On the right of the list item, click on the edit ![](/wp-content/uploads/gij-edit-icon-dark.png) icon or the **Link commit** label to manage Jira issue association for the selected git commit.
5.  Add, remove or change one or more Jira issue keys to assign the selected commit.
6.  Please note that manually linking git commits in this manner can only be done one at a time.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Git Integration for Jira Cloud app also supports multiple issue keys in a commit message.
    </div>
    </div>
</div>

For Jira administrators planning to migrate from Jira Server/Data Center to Jira Cloud, please read this first - [Export project from Jira Server to Jira Cloud](https://support.atlassian.com/migration/resources/).

When transitioning from Jira self-hosted to Jira Cloud, maintaining the same project name will retain all git commit associations after the migration.

### Can the plugin be configured to handle or scan multiple keys for one project? How is this supposed to work?

Yes – the Git Integration for Jira Cloud app supports multiple Jira issue keys in a multiple-line commit message.

For more information, see **[Smart Commits »](/git-integration-for-jira-cloud/smart-commits-gij-cloud)**.

&nbsp;
* * *
&nbsp;

## Installation and Setup

Solutions related to Git Integration for Jira Cloud app installation.

### Does it take long to install?

No. With Atlassian Marketplace, you can install the app from inside of your JIRA Cloud using your browser.

### I don't know Git — what will I need to install the app?

For the most common setups, you will need the URL to your Git server and credentials to access it. Tell your Git administrator that you need access to the Git repository just like a regular developer would have.  They will provide what you need.

### What will my Jira look like after it is installed?

A new tab is added in each issue. A new tab is added in each project.

### How do I install the plugin in a development version of Jira?

Atlassian has posted the following relevant information regarding Atlassian Marketplace addons and development licenses of Jira:

[Licensing and Pricing](https://www.atlassian.com/licensing/marketplace#licensingandpricing-4)

Which points to:

[Licensing and Paid via Atlassian Listings](https://developer.atlassian.com/market/add-on-licensing-for-developers/licensing-and-paid-via-atlassian-listings)

Go to the section titled, **"Can customers use developer licenses for my add-on?"**, which has instructions on how to get a developer license for add-ons.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>In summary:</b><br>
        A developer license can be generated (free of charge) once the plugin has been purchased and can only be installed on a development licensed version of Jira.
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

## Administration

Questions and solutions targeted for administrators.

### Does Jira+GitHub integration support multiple Jira projects (many) to multiple git repositories (many)? If it does not, how about many-to-one or one-to-many?

Yes — it does support repositories supporting many projects. That said, the associations are made by the developers when they commit code to a specific issue key (which is part of a project). The permission that allows a user to see these commits in a Jira project is whether they have the "View Development Tools" permission for that project (that's a Jira setting).

&nbsp;
* * *
&nbsp;

## Repositories

Solutions to common issues encountered while connecting and configuring git repositories.

### We use GitBlit without SSH keys and use only HTTPS instead. Does Git Integration Plugin for Jira support this?

Yes. The Git Integration for Jira Cloud app definitely supports GitBlit via HTTPS authentication. Use the **[Plain git integration](/git-integration-for-jira-cloud/using-the-single-git-integration-wizard-gij-cloud/)** wizard to connect to your repositories. Towards the end of the process, a username and password will be required for connection authentication.

&nbsp;
* * *
&nbsp;

## Workspace

Questions on Git Integration for Jira add-on user experience in Jira.

### How do I see if work has really started on an issue?

Open an issue in your browser and click on the **Git Commits** tab.

If the tab says that no Git log entries have been found, then work has not yet started on the ticket.

<img src='https://bigbrassband.com/images/bbb/jira-issue-git-commits.png' style='margin:25px auto 15px auto;max-width:100%:;display:block;' />

<p align=center>
    <i>See all Git commits associated with an issue in Jira</i>
</p>

### How do I see who has worked on an issue?

Open an issue in your browser and click on the **Git Commits** tab.

Everyone listed in the "Author/Committer" column has worked on the issue.

### How do I see how long ago since someone worked on it?

Open an issue in your browser and click on the **Git Commits** tab.

All changes to source code are listed from newest to oldest. The date/time in the "Date/Revision" column on the first line is the last time changes to the issue have been submitted into Git.

### How do I see what is being changed in this ticket?

Open an issue in your browser and click on the **Git Commits** tab.

When a developer submits a change to Git, they can type a brief message that summarizes the changes. These messages show up under the Committer/Author's name.

The files that were changed by the developer appear as clickable links. column. Click on the file links to view the actual source code that was changed.

&nbsp;
* * *
&nbsp;

## SSH

Questions related to SSH connections in Jira.

### Does this app support authenticating to git repositories via SSH?

Yes.

SSH keys with and without passphrases are supported.

### Why do I need to provide a PRIVATE KEY to the Git Integration for Jira Cloud app instead of a PUBLIC KEY?

The PRIVATE KEY is needed by the SSH client, which is the Jira Cloud, to connect to the Git server via SSH.

### How do I configure/connect an SSH remote git repository to Jira?

In Jira, use the **[Plain git integration](/git-integration-for-jira-cloud/using-the-single-git-integration-wizard-gij-cloud/)** wizard to configure SSH integration with any remote git repositories.

Here's a video to guide you step-by-step as stated above:

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/qmumdo048n?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align="center" style='margin-top:10px'>
    <i>Watch the video guide by clicking <a href="https://bigbrassband.wistia.com/medias/qmumdo048n" target="_blank"><b>here</b></a> to open this video in a new browser tab<br> for more viewing options.</i>
</div>

&nbsp;
* * *
&nbsp;

## Reindex

Questions related to git notes, reindex tracking and control.

### What does re-index do?

Re-index does 2 operations:

*   Updates the cloned repo from remote
*   Updates the indexes which contain info about every commit

### Is there any way to control the reindex?

In terms of kicking off the indexing based on an event:

*   Webhook: [Configure Webhooks](/git-integration-for-jira-cloud/indexing-triggers-formerly-webhooks-gij-cloud)

What other users have done is set a high interval and then configure one of those options.

### Commits are not showing right away. Can they show up faster?

Commits won't appear immediately. Configure webhooks via **Manage integrations** page to make commits show faster.

### Is it possible to track the specified branches when reindexing?

No. The Git Integration for Jira app is designed to do a full index.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The reindex process won't start if reindex is already running.
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For more information on indexing, see [Indexing Explainer for Git Integration for Jira Cloud](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud/).
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

## Uninstall and Reinstall

Questions related to uninstall and reinstall of Git Integration for Jira app.

### How do I reinstall the app?

1.  Do an uninstall of the app as detailed in the section below.
2.  Install the Git for Jira Cloud app as outlined [**here**](/git-integration-for-jira-cloud/installation-via-atlassian-marketplace-gij-cloud).

### How do I uninstall the Git for Jira Cloud app?

The following steps will remove the Git Integration app from Jira:

**Uninstall the Git for Jira Cloud app from the Jira UPM (Universal Plugin Manager).**

1. Go to **`Jira Settings ➜ Apps ➜ Manage apps`**.

2. Under _User-installed apps_, select **Git for Jira Cloud** then click **Uninstall**.

&nbsp;
* * *
&nbsp;

## Purchase and Pricing

Questions about trial or purchase of Git Integration for Jira app and accepted payment methods.

### How do I buy this add-on?

Buy the Git Integration for Jira app on Atlassian Marketplace using your Atlassian account  —  the same place where you manage your Jira license today.

**[Click here for a 30-day trial of Jira Git Plugin](https://my.atlassian.com/addon/try/com.xiplink.jira.git.jira_git_plugin "[Try our Jira Git Plugin]")**

**[Click here to buy the Jira Git Plugin](https://my.atlassian.com/purchase/buyaddon?key=com.xiplink.jira.git.jira_git_plugin "[Buy the Jira Git Plugin]")**

### What payment methods are accepted?

Atlassian Marketplace accepts MasterCard, Visa and American Express.  You may also pay with bank transfer or mailed check.

[**30 Day Trial**](https://my.atlassian.com/addon/try/com.xiplink.jira.git.jira_git_plugin "[Try our Jira Git Plugin]")

[**Buy Now**](https://my.atlassian.com/purchase/buyaddon?key=com.xiplink.jira.git.jira_git_plugin "[Buy the Jira Git Plugin]")

### How do I determine the Git Integration for Jira app pricing after the trial?

There are four ways to determine the pricing:

1.  Install the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=pricing) app then go to:

    ```powershell
    https://[replacewithyourJiraname].atlassian.net/admin/billing/estimate
    ```

    The estimated monthly or annual price will be quoted.

2.  See pricing details on the [Atlassian Marketplace: Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=pricing).

3.  Use the [Atlassian Cloud Pricing Calculator](https://www.atlassian.com/software/pricing-calculator):

    *   Choose between **monthly/annual**.
    *   Enter the **number of seats** your Jira is licensed for.
    *   Select **Apps**.
    *   Select **Git Integration for Jira _(Top Selling)_** from the dropdown list.

4.  Create a quote on [Atlassian.com](https://www.atlassian.com/purchase/addon/com.xiplink.jira.git.jira_git_plugin).

    Select the **Quote** option then **Deployment** (Server/Cloud/DC) and follow the instructions.

All four should provide the same answer.

&nbsp;
* * *
&nbsp;

## Support

Topics related to Git Integration for Jira app support.

### Does the Git for Jira Cloud app support CJK languages or Unicode?

Unicode characters are supported and displayed properly.

### Where can I find my App Information?

You can find your App information by Navigating to the GIJ General settings

First, click on the apps menu, then click "Manage Integrations"
![](/wp-content/uploads/App-Information1.png)

Then, from the left hand menu,click the option labeled "General Settings" under the 'GIT' heading.
![](/wp-content/uploads/App-Information2.png)

Copy the information at the bottom of the page, starting from "Current Build". Include this information in your support request, or supply it to the support team if they have requested it.

