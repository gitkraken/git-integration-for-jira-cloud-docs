---

title: Permissions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/21vd3arsj6?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/21vd3arsj6'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>
<br>

## Permissions requirement to display commit information

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Users must have '<b><i>View Development Tools</i></b>' permission in order to view commit information on the issue page.<p style='margin-bottom: 0px'>Administrators must grant themselves the '<b><i>View Development Tools</i></b>' permission in order to view commit information on the issue pages.</p>
    </div>
    </div>
</div>
<br>

The user needs to be in the developers group to view code diffs when default permission scheme is used.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/405962836/view-dev-tools-project-acl(c).png?version=1&modificationDate=1585811271845&cacheVersion=1&api=v2&width=680&height=361)


Consider the following criteria when setting permissions:

*   Permission name may be different depending on your version of Jira.

*   Project permissions are configured on the project administration page. Different projects may have different permissions.

*   Default permission scheme grants access to add-on to all members of _**administrators**_ and _**developers**_ groups. No additional configuration is required in this case.

