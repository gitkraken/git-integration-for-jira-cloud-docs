---

title: Known Performance Limitations
description: Soft limits and performance guidelines for Git Integration for Jira Cloud
taxonomy:
    category: git-integration-for-jira-cloud

---

The Cloud version of Git Integration for Jira runs on AWS instances and has fewer configuration options compared to a self-hosted Jira/GIJ instance. This document details soft limits beyond which some customers experience performance issues.

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The thresholds below are guidelines rather than hard limits. In most cases, you can exceed these limits, but depending on severity, this could lead to degraded performance or halted operation. If you experience issues due to exceeding these limits, our support team will suggest alternative configurations, but we cannot guarantee performance or operation when limits are breached.
    </div>
    </div>
</div>

&nbsp;

## Git Tags

| Limit | Possible Issues |
| :--- | :--- |
| >2,000 | Slow indexing |

&nbsp;

## Total Repositories in an Integration

| Limit | Possible Issues |
| :--- | :--- |
| >2,000 | Slow indexing |
| | Rate limit errors when getting PR/Builds/Deployments data during indexing |
| | Long loading times or timeout errors when loading development data |

&nbsp;

## Individual Repository Size

| Limit | Possible Issues |
| :--- | :--- |
| >2 GB | Extended indexing time |
| | Rate limit errors when getting PR/Builds/Deployments data during indexing |
| | Long loading times or timeout errors when loading development data |

&nbsp;

## Individual File Size in a Repository

This is a hard limit due to a restriction in an internal component used by Git Integration for Jira. If the file size limit is exceeded, the repository cannot be indexed.

See [Max Object Error](/git-integration-for-jira-cloud/error-while-reindexing-java-heap-space-object-too-large-rejecting-the-pack-gij-cloud) for further details.

| Limit | Possible Issues |
| :--- | :--- |
| >2 GB | Repository will not clone or index |

&nbsp;

## Number of Branches in a Repository

| Limit | Possible Issues |
| :--- | :--- |
| >2,000 | Slow indexing |
| | Rate limit errors when getting PR/Builds/Deployments data during indexing |
| | Long loading times or timeout errors when loading development data |

&nbsp;

## Number of Pull/Merge Requests

| Limit | Possible Issues |
| :--- | :--- |
| >2,000 | Slow indexing |
| | Rate limit errors when getting PR/Builds/Deployments data during indexing |
| | Long loading times or timeout errors when loading development data |

&nbsp;

## Number of Builds and/or Deployments

| Limit | Possible Issues |
| :--- | :--- |
| >2,000 | Slow indexing |
| | Rate limit errors when getting PR/Builds/Deployments data during indexing |
| | Long loading times or timeout errors when loading development data |

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
