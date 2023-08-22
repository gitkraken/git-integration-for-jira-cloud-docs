---

title: Linking git commits to Jira issues
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

To create a link between your Git commit and a Jira issue, developers must include the issue key into the commit comment.

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/cs229y2gzj?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;margin-bottom:30px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/cs229y2gzj'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

Commits are selected by issue key. Developers should add them to comments every time the commits are made.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        For example, the <b>"PRJ-50 fixed issue"</b> comment – this assumes that you have configured a Jira project with the key <b>'PRJ'</b> and someone has created the issue <b>#50</b> within this project.
    </div>
    </div>
</div>

<img src='/wp-content/uploads/gij-gitcloud-git-commits-commits-info.png' style='margin-top:25px auto;max-width:100%;display:block;' />

<div style='margin-top:10px'><i>Example Git commit message: <b>"TEST-1 Update..."</b><br>
In this case, <b>"TEST-1"</b> is the issue key linking the commit message to the Jira issue.</i></div>

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Commits that are part of non-master branches will be included only if the master branch doesn't have them.
    </div>
    </div>
</div>

As a best practice to work with sub-task — put the parent and sub-task Jira issue keys in the commit message so that the commit shows in both places. This way, the commit for the sub-task does not get lost in the many commits of the parent issue.

<img src='/wp-content/uploads/gij-gitcloud-git-commit-commit-sel-subtask.png' style='margin:25px auto' />

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The maximum commit message length limit is <b>8,000 characters</b>.
    </div>
    </div>
</div>

The Git Integration for Jira app supports commits that used the old Jira key in the commit message after a project rename to a new key name (Example: `TEST-16` to `PROJ-16`).

There are two scenarios related to the rename/move:

*   The Jira project key was renamed and the commit message contains the old key prior to the installation of the Git Integration for Jira app.

*   The Jira issue was moved from one project to another project and the message contains the old key prior to the installation of the Git Integration for Jira app.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Jira Activity Stream</b><br>
        Only the commits that are linked to Jira issues will show on the Jira Activity Stream (not all commits in repositories).
    </div>
    </div>
</div>

&nbsp;
* * *

[**Prev:** Web linking](/git-integration-for-jira-cloud/web-linking-gij-cloud)

[**Next:** Associating git commits manually to Jira issues](/git-integration-for-jira-cloud/associating-git-commits-manually-to-jira-issues-gij-cloud)

