---
title: Fix for empty JSON files
description: Troubleshooting guide for corrupted JSON configuration files in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

This page provides solutions for recovering from corrupted integration configuration files.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Note:</b> Investigation and work on this issue is expected to continue through Monday, Feb. 5 before fully complete.
    </div>
    </div>
</div>

&nbsp;

## Problem

Our technical team discovered corrupted files in some customer integrations. These files contain information about integrations and repositories only. No customer data was lost.

While investigating the root cause, the team identified a recovery path using backups.

&nbsp;

## Diagnosis

Two cases can occur:

1. Integration configuration disappears completely.
2. Integration configuration exists but indexing errors appear related to JSON parsing.

&nbsp;

## Cause

Unexpected file corruption of the JSON file that stores integration and repository configuration (integration name, commit/pull/merge counter, etc.).

&nbsp;

## Solutions

### Case 1: Integration disappears completely

1. Connect and set up the required integration again. Large integrations may take several hours to index all repositories.

2. If you use the Jira Development Info feature, prevent data duplication:

   a. Disable all integrations.
   
   b. Go to GIJ **General settings** ➜ **Advanced** section.
   
   c. Click **Clear Development Information**.
   
   ![](/wp-content/uploads/gij-gitcloud-gencfg-advanced-clear-dev-info.png)
   
   d. Enable all integrations.

3. After completing these steps, notify the [GIJ support team](/git-integration-for-jira-cloud/gij-cloud-contact-support/) that data restoration is not required. Otherwise, data duplication will occur if we restore data on our side.

&nbsp;

### Case 2: Integration exists but indexing errors appear

**Error message:** "Error of converting a string to java.util.HashMap<java.lang.String, java.util.Collection<org.json.JSONObject>>"

1. Remove or disconnect the affected integration.

2. Connect and set up the affected integration again. Large integrations may take several hours to index all repositories.

3. After completing these steps, notify the [GIJ support team](/git-integration-for-jira-cloud/gij-cloud-contact-support/) that data restoration is not required. Otherwise, data duplication will occur if we restore data on our side.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        Reach out to our <a href='/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

<kbd>Last updated: December 2025</kbd>
