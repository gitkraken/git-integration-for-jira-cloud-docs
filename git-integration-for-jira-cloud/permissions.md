---

title: Permissions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Permissions

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/405962836/Permissions>

* * *

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/21vd3arsj6) _to open this video in a new browser tab for more viewing options._  

## Permissions requirement to display commit information

Users must have ‘_**View Development Tools**_’ permission in order to view commit information on the issue page.

Administrators must grant themselves the ‘_**View Development Tools**_’ permission in order to view commit information on the issue pages.

  
The user needs to be in the developers group to view code diffs when default permission scheme is used.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/405962836/view-dev-tools-project-acl(c).png?version=1&modificationDate=1585811271845&cacheVersion=1&api=v2&width=680&height=361)

  
Consider the following criteria when setting permissions:

*   Permission name may be different depending on your version of Jira.
    
*   Project permissions are configured on the project administration page. Different projects may have different permissions.
    
*   Default permission scheme grants access to add-on to all members of _**administrators**_ and _**developers**_ groups. No additional configuration is required in this case.