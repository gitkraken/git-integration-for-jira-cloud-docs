---

title: Known Performance limitations
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The Cloud version of our application is run on our services and there are numerous fewer options for configuration compared to a self-hosted instance of Jira/GIJ. This document details some “soft limits,” beyond which we’ve noticed some of our customers having performance issues. 

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Please note that the thresholds below are meant to be guidelines rather than hard limits. In most cases, the limits can be exceeded, but depending on the severity, could lead to degraded performance or even halted operation. In cases where you are having issues due to these limits being exceeded, our support team will do their best to make suggestions for alternative configurations that could help, but we cannot guarantee performance or operation in cases where the limits are being breached.
    </div>
    </div>
</div>

## Git Tags

| Limit | Possible issues |
| --- | --- |
|>2000 | Slow Indexing |

## Total Repositories in an Integration

| Limit | Possible issues |
| --- | --- |
|>2000 | Slow Indexing <br> Rate limit errors when getting PR/Builds/Deployments data during indexing <br> Long loading times (or even timeout errors during loading) of development data. |

## Individual Repository size

| Limit | Possible issues |
| --- | --- |
|>2gb | Extended Indexing time <br> Rate limit errors when getting PR/Builds/Deployments data during indexing <br> Long loading times (or even timeout errors during loading) of development data. |

## Individual file size in a repository
This is a hard limit due to a restriction in an internal component used in Git Integration for Jira. If the file size limit is exceeded, the Repository will not be able to be indexed. Please see [Max Object Error](https://help.gitkraken.com/git-integration-for-jira-cloud/error-while-reindexing-java-heap-space-object-too-large-rejecting-the-pack-gij-cloud/) for further details

| Limit | Possible issues |
| --- | --- |
|>2Gb | Repository will not clone/index |

## Number of branches in a repository

| Limit | Possible issues |
| --- | --- |
|>2000 | Slow Indexing <br> Rate limit errors when getting PR/Builds/Deployments data during indexing <br> Long loading times (or even timeout errors during loading) of development data. |

## Number of Pull/Merge Requests

| Limit | Possible issues |
| --- | --- |
|>2000 | Slow Indexing <br> Rate limit errors when getting PR/Builds/Deployments data during indexing <br> Long loading times (or even timeout errors during loading) of development data. |

## Number of Builds and/or Deployments

| Limit | Possible issues |
| --- | --- |
|>2000 | Slow Indexing <br> Rate limit errors when getting PR/Builds/Deployments data during indexing <br> Long loading times (or even timeout errors during loading) of development data. |

