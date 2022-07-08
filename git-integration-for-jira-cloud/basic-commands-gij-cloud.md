---

title: Smart commits - Basic Commands
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
There are smart commits commands that you can use in your commit messages. Read on for more details on each smart commit command.

## \#comment

This command works both in Jira Server/Cloud.

The `#comment` command will add a comment to a Jira issue.

**Syntax: ISSUE\_KEY** **\#comment** `[your comment text]`

**Examples:**<br>
**GIT-264** **\#comment** `Resolved conflicts.`<br>
**GIT-1720** **\#comment** `Plugin version change from 2.8.2 to 2.8.3. Build number change from 69 to 70.`

The above examples will add the specified comment text against the Jira issues.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The committers’ email address in the git configuration must match with the email address of the corresponding Jira user (or vice versa) to comment on issues.
    </div>
    </div>
</div>
<br>

## \#time

This command works both in Jira Server/Cloud.

The `#time` command will record time tracking information against a Jira issue.

**Syntax:** **ISSUE\_KEY** **\#time** \[Some amount in Jira time syntax\] `[Your worklog comment text]`

**Examples:**<br>
**GIT-264** **\#time** 1w 6d 13h 52m `Total work logged.`<br>
**GIT-1720** **\#time** 1h 20m `Merged to master. Released to marketplace.`

The above examples will add the respective time and worklog comment text against the Jira issues.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Jira time tracking feature allows users to log the length of time spent working on issues. Jira administrators must have enabled this feature for this smart commit to work.
    </div>
    </div>
</div>
<br>

## \#\<transition-name\>

This command works both in Jira Server/Cloud.

The `#<transition-name>` command will move the Jira issue to a particular workflow state.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The Jira user must have the appropriate project permissions to be able to transition issues.
    </div>
    </div>
</div>
<br>

**Syntax:** **ISSUE\_KEY** **\#\<transition-name\>** `[Your commit comment text]`

**Examples:**<br>
**GIT-264** **\#code-review** `For review.`<br>
**GIT-1720** **\#close** `Closing ticket.` **\#comment** `Tasks completed.`
The first example will transition the Jira issue to the specified workflow state and adds the comment message to the commit.

The second example will transition the Jira issue to the specified workflow state, adds the comment "_**Closing ticket**_" to the Comment tab and adds the specified comment, "_**Task completed**_" to the mentioned Jira issue.

For more information on transitions and workflow names and how they work, see [Workflow Transitions](/git-integration-for-jira-cloud/workflow-transitions-gij-cloud/).

<br>

## \#assign

This command works both in Jira Server/Cloud.

The `#assign` command will assign the particular issue to the specified Jira user. This command works in Jira Server/Cloud.

**Syntax:** **ISSUE\_KEY** **\#assign** `[Jira username or email of Jira user]`

**Examples:**<br>
**GIT-1925** **\#assign** `johnsmith`<br>
**GIT-1961** **\#assign** `johnsmith@example.com`

<br>

## \#label

This command works both in Jira Server/Cloud.

The `#label` command will add a new label to a Jira issue. If more than one Jira issue is referenced, the labels are added to all mentioned Jira issues. Multiple labels can be created by putting spaces between words.

**Syntax: ISSUE\_KEY(S) \#label** `[label1] .. [labeln]`

**Examples:**<br>
**GITCL-443** **\#label** `bucketbreakfix` `bucketenhancement`<br>
**GITCL-443 GITCL-247 GITCL-214** **\#label** _admin@example.com_ _user1@example.com_ requested-feature new-feature **\#comment** `Return email when implemented`

