---

title: Smart commits general settings
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
Navigate to Git integration for Jira (sidebar) ➜ **General settings** to access this setting.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/1923025462/image-20210324-081135.png?version=1&modificationDate=1630063662176&cacheVersion=1&api=v2)

<br>

<b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>JIRA CLOUD</b> <b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>DEV INFO</b>

**Max commit age**  –  This setting is a hidden feature in Git Integration for Jira Cloud and Dev Info for Jira Cloud. All commits which are older than this setting (in seconds) shall be ignored for smart commits processing. The default value is **1209600** seconds (14 days). |

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        In case <a href="/git-integration-for-jira-cloud/jira-development-information-gij-cloud/">when DevInfo for Jira Cloud is enabled</a>, commits shall be sent with <b><i>disabledTransition</i></b> flag.
    </div>
    </div>
</div>
<br>

