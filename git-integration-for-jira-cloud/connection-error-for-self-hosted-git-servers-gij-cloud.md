---

title: Connection error for self-hosted git servers
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Problem

Jira admins are not able to connect Jira Cloud to self-hosted git servers when hosted behind a firewall or otherwise not reachable by the Git Integration for Jira Cloud indexing service.

## Diagnosis

Jira admins will see a message similar to the one below when connecting to self-hosted git servers hosted behind a firewall or otherwise not reachable.

| **Error** |
| --- |
| ```java<br>com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.TaskException: com.bigbrassband.gitforjiracloud.indexer.sources.TrackedGitLabRepoException: Can not connect to GitLab server<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.Task.runWithMappedExceptions(Task.java:56)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoint.runTasks(ApiEndPoint.java:162)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoints.handleRequest(ApiEndPoints.java:79)<br>at com.bigbrassband.gitforjiracloud.appserver.AppServer$SuperHandler.handle(AppServer.java:219)<br>at com.bigbrassband.common.util.httpplumbing.WebServer$InternalRequestHandler.handle(WebServer.java:164)<br>at org.apache.http.protocol.HttpService.doService(HttpService.java:437)<br>at org.apache.http.protocol.HttpService.handleRequest(HttpService.java:342)<br>at com.bigbrassband.common.util.httpplumbing.Worker.run(Worker.java:41)<br>at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)<br>at java.util.concurrent.FutureTask.run(FutureTask.java:266)<br>at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)<br>at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)<br>at java.lang.Thread.run(Thread.java:748)<br>Caused by: com.bigbrassband.gitforjiracloud.indexer.sources.TrackedGitLabRepoException: Can not connect to GitLab server<br>at com.bigbrassband.gitforjiracloud.indexer.sources.GitlabApiMonster.getGitlabApi(GitlabApiMonster.java:34)<br>at com.bigbrassband.gitforjiracloud.indexer.sources.GitlabRepoSource.getRepositories(GitlabRepoSource.java:47)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.git.repos.PingRepoTask.pingRepoSource(PingRepoTask.java:91)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.git.repos.PingRepoTask.run(PingRepoTask.java:71)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.Task.runWithMappedExceptions(Task.java:36)<br>... 12 more<br>Caused by: org.gitlab.api.GitlabAPIException<br>at org.gitlab.api.http.GitlabHTTPRequestor.handleAPIError(GitlabHTTPRequestor.java:543)<br>at org.gitlab.api.http.GitlabHTTPRequestor.to(GitlabHTTPRequestor.java:201)<br>at org.gitlab.api.http.GitlabHTTPRequestor.to(GitlabHTTPRequestor.java:167)<br>at org.gitlab.api.GitlabAPI.getVersion(GitlabAPI.java:3199)<br>at org.gitlab.api.GitlabAPI.createPATAuthOnly(GitlabAPI.java:158)<br>at org.gitlab.api.GitlabAPI.create(GitlabAPI.java:145)<br>at com.bigbrassband.gitforjiracloud.indexer.sources.GitlabApiMonster.getGitlabApi(GitlabApiMonster.java:29)<br>... 16 more<br>Caused by: com.fasterxml.jackson.core.JsonParseException: Unexpected character ('<' (code 60)): expected a valid value (number, String, array, object, 'true', 'false' or 'null')<br><br>``` |

## Solution

See [Whitelist BigBrassBand Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud).

**Contact Us**

If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).

