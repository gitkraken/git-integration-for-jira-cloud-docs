---

title: Permissions
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<p><a href="https://bigbrassband.wistia.com/medias/21vd3arsj6?wvideo=21vd3arsj6"><img src="https://embed-ssl.wistia.com/deliveries/e02752d1bb406d091a57caf57e0f2a9103bc20bd.jpg?image_play_button_size=2x&amp;image_crop_resized=960x600&amp;image_play_button=1&amp;image_play_button_color=54bbffe0" width="400" height="250" style="width: 400px; height: 250px;"></a></p><p><a href="https://bigbrassband.wistia.com/medias/21vd3arsj6?wvideo=21vd3arsj6">Git Integration for Jira Cloud - Permissions - BigBrassBand</a></p>


_Click_ [_**here**_](https://bigbrassband.wistia.com/medias/21vd3arsj6) _ to view the video._

## Permissions requirement to display commit information

Users must have ‘_**View Development Tools**_’ permission in order to view commit information on the issue page.

Administrators must grant themselves the ‘_**View Development Tools**_’ permission in order to view commit information on the issue pages.


The user needs to be in the developers group to view code diffs when default permission scheme is used.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/405962836/view-dev-tools-project-acl(c).png?version=1&modificationDate=1585811271845&cacheVersion=1&api=v2&width=680&height=361)


Consider the following criteria when setting permissions:

*   Permission name may be different depending on your version of Jira.

*   Project permissions are configured on the project administration page. Different projects may have different permissions.

*   Default permission scheme grants access to add-on to all members of _**administrators**_ and _**developers**_ groups. No additional configuration is required in this case.