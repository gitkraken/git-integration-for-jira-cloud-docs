---

title: Permissions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---


&nbsp;

### Permissions requirement to display commit information

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Users must have '<b><i>View Development Tools</i></b>' permission in order to view commit information on the issue page.
        <p style='margin-bottom:-10px'>Administrators must grant themselves the '<b><i>View Development Tools</i></b>' permission in order to view commit information on the issue pages.</p>
    </div>
    </div>
</div>

The user needs to be in the developers group to view code diffs when default permission scheme is used.

![](/wp-content/uploads/gij-gitcloud-jira-view-dev-tools-project-acl.png)


Consider the following criteria when setting permissions:

*   Permission name may be different depending on your version of Jira.

*   Project permissions are configured on the project administration page. Different projects may have different permissions.

*   Default permission scheme grants access to add-on to all members of _**administrators**_ and _**developers**_ groups. No additional configuration is required in this case.

