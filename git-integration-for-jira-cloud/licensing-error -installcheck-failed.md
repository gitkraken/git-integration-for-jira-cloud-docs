---

title: Licensing error - installCheck failed
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Problem

Occasionally when the Git Integration for Jira Cloud app is installed - the licensing fails to fully provision.

## Diagnosis

Jira administrators and users will see a message similar to the one below.

![](https://bigbrassband.atlassian.net/wiki/download/attachments/420282445/licensing-installcheck-failed-error.png?version=1&modificationDate=1586316709675&cacheVersion=1&api=v2)

| **Error** |
| --- |
| ```java<br>com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.TaskException: Install does not satisfies requirements. Must correspond at least one of enabledFolder<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.InstallCheckTask.run(InstallCheckTask.java:42)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.Task.runWithMappedExceptions(Task.java:36)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoint.runTasks(ApiEndPoint.java:162)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoints.handleRequest(ApiEndPoints.java:79)<br>at com.bigbrassband.gitforjiracloud.appserver.AppServer$SuperHandler.handle(AppServer.java:219)<br>at com.bigbrassband.common.util.httpplumbing.WebServer$InternalRequestHandler.handle(WebServer.java:164)<br>at org.apache.http.protocol.HttpService.doService(HttpService.java:437)<br>at org.apache.http.protocol.HttpService.handleRequest(HttpService.java:342)<br>at com.bigbrassband.common.util.httpplumbing.Worker.run(Worker.java:41)<br>at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)<br>at java.util.concurrent.FutureTask.run(FutureTask.java:266)<br>at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)<br>at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)<br>at java.lang.Thread.run(Thread.java:748)<br>``` |

## Solution

Most users can resolve this issue on their own by re-installing the app.

1.  Navigate to the **Manage Apps** screen

2.  Locate and expand the **Git Integration for Jira Cloud** app

3.  Prior to uninstalling the app - you must **Stop trial\***

4.  Proceed to **Uninstall** the app

5.  Install the **Git Integration for Jira** app


|     |
| --- |
| **Stopping trial**<br><br>The evaluation/trial must be stopped before you can uninstall the app |
| ![](https://bigbrassband.atlassian.net/wiki/download/attachments/420282445/manage-apps-git-cloud-admin.png?version=1&modificationDate=1586317006632&cacheVersion=1&api=v2) |

**Contact Us**

If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).

## Related articles

*   Page:

    [Why don't I see commits? (Git Integration for Cloud)](/wiki/spaces/GITCLOUD/pages/110755841) (Git Integration for Jira Cloud)

*   Page:

    [Repositories missing from Azure DevOps (or VSTS) integration](/wiki/spaces/GITCLOUD/pages/421462017/Repositories+missing+from+Azure+DevOps+%28or+VSTS%29+integration) (Git Integration for Jira Cloud)

*   Page:

    [Licensing error - installCheck failed](/wiki/spaces/GITCLOUD/pages/420282445/Licensing+error+-+installCheck+failed) (Git Integration for Jira Cloud)

*   Page:

    [Why don't I see the Create branch or pull request features?](/wiki/spaces/GITCLOUD/pages/421593107) (Git Integration for Jira Cloud)

*   Page:

    [Connection error for self-hosted git servers](/wiki/spaces/GITCLOUD/pages/419659840/Connection+error+for+self-hosted+git+servers) (Git Integration for Jira Cloud)

*   Page:

    [SSH key file format is invalid](/wiki/spaces/GITCLOUD/pages/421363756/SSH+key+file+format+is+invalid) (Git Integration for Jira Cloud)

*   Page:

    [Error while reindexing - Java heap space / Object too large, rejecting the pack](/wiki/spaces/GITCLOUD/pages/421462043) (Git Integration for Jira Cloud)

*   Page:

    [OAuth connection error or error 401 page with Azure DevOps integration](/wiki/spaces/GITCLOUD/pages/420282493/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+integration) (Git Integration for Jira Cloud)

*   Page:

    [OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/wiki/spaces/GITCLOUD/pages/421527629/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+with+Active+Directory+integration) (Git Integration for Jira Cloud)

*   Page:

    [Empty list of repositories after integration of Azure Repos](/wiki/spaces/GITCLOUD/pages/421298248/Empty+list+of+repositories+after+integration+of+Azure+Repos) (Git Integration for Jira Cloud)