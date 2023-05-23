---

title: Error creating git branches - GitLabPropertiesNotInitializedException and also using NFS
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<b style='background-color:#DEEAFE; padding:1px 5px; color:#0C42A3; border-radius:3px; margin: 0 5px; font-size: small;'>JIRA SELF-MANAGED</b>

Also relates to the following exception errors:
*   `GitHubPropertiesNotInitializedException`
*   `GerritPropertiesNotInitializedException`

&nbsp;

## Problem

An error is encountered with the next exception ( `GitLabPropertiesNotInitializedException` ) and you are using NFS.

**Example Error log**

```java
/rest/gitplugin/1.0/repository/12300/pullRequest [c.b.j.g.rest.exceptionmappers.LoggerHolder] REST API has thrown exception.
com.bigbrassband.jira.git.exceptions.operations.GitLabPropertiesNotInitializedException: Initialization
at com.bigbrassband.jira.git.services.integration.gitlab.GitLabApiService$GitLabRepoApi.getExternalRepoProps(GitLabApiService.java:107)
at com.bigbrassband.jira.git.services.integration.gitlab.GitLabApiService$GitLabRepoApi.getRepoExternalIdForMergeRequests(GitLabApiService.java:113)
at com.bigbrassband.jira.git.services.integration.gitlab.GitLabApiService$GitLabRepoApi.createMergeRequest(GitLabApiService.java:68)
at com.bigbrassband.jira.git.rest.repository.RepositoryResource.createPullRequest(RepositoryResource.java:832)
at com.bigbrassband.jira.git.rest.repository.RepositoryResource.restCreatePullRequest(RepositoryResource.java:796)
at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
at java.base/java.lang.reflect.Method.invoke(Method.java:566)
```

&nbsp;

## Diagnosis

Check the root of the reason by  [turning on DEBUG logging]() for the package – `com.bigbrassband.jira.git.services.integration`.

The root reason of the exception error can be one of the following: 

not a valid json entry in repo.auto.json

incapability to lock file (java.io.IOException: No locks available)