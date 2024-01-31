---

title: Fix for empty JSON files
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Investigation and work on this issue is expected to continue through Monday, Feb. 5 before it's fully complete.
    </div>
    </div>
</div>

&nbsp;

### Problem(s)

Our technical team discovered corrupted files in a number of customer integrations. These files are limited to information about integrations and repositories. Rest assured that no customer data was lost.

While our team is still investigating the root cause behind the corrupted files, they have also identified a path for recovering files from backups.

&nbsp;

### Diagnosis

There are two cases that can lead to the following:

    Integration configuration disappears completely.

    Integration configuration still exists but there are indexing errors related to JSON parsing.

&nbsp;

### Cause

Unexpected file corruption of the JSON file which holds information about connected integrations and repositories configuration such as integration name, commits/pull/merge counter, etc.

&nbsp;

### Solution

#### Case 1: If integration(s) disappears completely…

1.  Connect and setup the required integration again. If the integration is large, do note that the indexing of all repositories may take some time, even several hours.

2.  If the Jira Development Info feature is used, please do the following to prevent data duplication:

    *   Disable all integrations.

    *   Click on the Clear Development Information button in the advanced section of the GIJ ‘General settings’ page:

        ![](/wp-content/uploads/gij-gitcloud-gencfg-advanced-clear-dev-info.png)

    *   Enable all integrations.

3.  After performing the above steps, notify the [GIJ support team](/git-integration-for-jira-cloud/gij-cloud-contact-support/) that data restoration is not required for the install. Otherwise, data duplication will occur if we restore the data on our side.

&nbsp;

#### Case 2: If integration(s) exists but there are indexing errors like "Error of converting a string to java.util.HashMap\<java.lang.String, java.util.Collection\<org.json.JSONObject\>\>"

1.  Remove or disconnect the affected integration.

2.  Connect and setup the affected integration again. If the integration is large, do note that the indexing of all repositories may take some time, even several hours.

3.  After performing the above steps, notify the GIJ support team that data restoration is not required for the install. Otherwise, data duplication will occur if we restore the on from our side.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If you still have a question – reach out to our <a href='/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

