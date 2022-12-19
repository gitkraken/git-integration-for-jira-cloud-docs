---

title: Link git commits to Jira issue
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/cs229y2gzj?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:15px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/cs229y2gzj'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

&nbsp;

Open a Jira issue then go to the Git Commits tab.  In this tab, you will see commits, files changed, links to external repository, commit author and more.

<img srr='/wp-content/uploads/gij-gitcloud-git-commits-example.png' style='display:block;margin:25px auto 15px auto;max-width:100%'/>

<div align=center style='margin-bottom:30px'><i>In the above example, the issue key **TEST-1** text is inserted into a git commit message <br>to link the commit to this Jira issue.</i></div>

The git commit will get associated with the Jira issue if the commit message includes the exact issue ID. The Git Integration for Jira app will automatically index new commits and associate the referenced issue. For better readability, place the issue key text at the start of the commit message.

### Git administrator »

If you want to enforce the commit with a hook, please install this Git commit hook script - [Commit-msg Hook](/git-integration-for-jira-cloud/commit-msg-hook-gij-cloud).


