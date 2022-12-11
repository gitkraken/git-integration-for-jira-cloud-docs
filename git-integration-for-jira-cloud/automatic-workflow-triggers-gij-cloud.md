---

title: Automatic Workflow Triggers
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<!-- FEATURES -->

Use your development activity to make automatic changes in your Jira project workflows. For example:

*   you can configure your Jira workflow to automatically send a Jira issue to <b style='background-color:#FFF1B6; padding:1px 5px; color:#172A4C; border-radius:3px; margin: 0 5px; font-size: small;'>IN REVIEW</b> status when a pull request is pushed and associated with the issue, or

*   you can send a Jira issue to <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>IN PROGRESS</b> when a commit is pushed and associated with a Jira issue.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Available triggers through the <a href='https://marketplace.atlassian.com/4984'  target='_blank'><b>Git Integration for Jira</b></a> and <a href='https://marketplace.atlassian.com/1219270' target='_blank'><b>Dev Info for Jira</b></a> apps:
        <ul>
            <li>Commit created</li>
            <li>Branch created</li>
            <li>Pull request created</li>
            <li>Pull request merged</li>
            <li>Pull request declined (closed)</li>
            <li>Pull request reopened</li>
        </ul>
    </div>
    </div>
</div>
<br>

To configure automatic workflow triggers for your project:

1.  Go to <img src='/wp-content/uploads/actions-icon.png' /> **Project settings**.

2.  Select **Workflow** on the sidebar.

3.  Click <img src='/wp-content/uploads/gij-edit-icon-dark.png' /> **Edit** on the _**Actions**_ column.

4.  Click **Text** to display the Diagram in text mode.

5.  Under _**Transitions**_ column, click a transition item.

6.  Click **Add trigger**. The Add trigger dialog is displayed.

    ![](/wp-content/uploads/gij-gitcloud-automatic-workflow-trigger-add-trigger-c.png)

7.  Click **Commit created**.

8.  Click **Add trigger**. This trigger will automatically transition the issue when a related commit is made in a connected repository.

9.  Click **Publish Draft**. This action will publish the currently edited workflow. Create a backup or set it to _**No**_ then click **Publish**.


The automatic workflow trigger is now configured. You can also view this entire process by watching the demo video below.

## Demo video: Configuring Automatic Workflow Trigger

<div class='embed-container' style='padding-bottom:65%'>
    <iframe width='709' height='461' src='https://fast.wistia.com/embed/iframe/r8fm0tbrcs?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/r8fm0tbrcs'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <a href='https://confluence.atlassian.com/jirasoftwarecloud/configuring-development-tools-764478056.html#Configuringdevelopmenttools-Workflowtriggers'><b>More information from Atlassian</b></a>
    </div>
    </div>
</div>
<br>
<br>

## More related topics about Jira Cloud smart commits and workflow triggers

[Enable Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers](/git-integration-for-jira-cloud/enable-jira-cloud-smart-commits-automation-for-jira-and-workflow-triggers-gij-cloud)

[How can a Jira administrator enable or disable the Jira Cloud Smart Commits, Automation for Jira and Workflow Triggers?](/git-integration-for-jira-cloud/jira-cloud-smart-commits-and-workflow-triggers-gij-cloud/#how-can-a-jira-administrator-enable-or-disable-the-jira-cloud-smart-commits-automation-for-jira-and-workflow-triggers)

**Automatic Workflow Triggers** (this page)

<br>
<br>
<hr>
<br>
<br>

## More related topics on Jira Development Information

[Development Information Views](/git-integration-for-jira-cloud/development-information-views-gij-cloud)

[JQL searching for commits and pull requests](/git-integration-for-jira-cloud/jql-searching-for-commits-and-pull-requests-gij-cloud)

[Jira Cloud Smart Commits and Workflow Triggers](/git-integration-for-jira-cloud/jira-cloud-smart-commits-and-workflow-triggers-gij-cloud/)

[Jira Development Information general settings](/git-integration-for-jira-cloud/jira-development-information-settings-gij-cloud)


