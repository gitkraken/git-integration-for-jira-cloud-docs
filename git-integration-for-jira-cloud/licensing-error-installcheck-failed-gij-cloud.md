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

![](/wp-content/uploads/gij-licensing-installcheck-failed-error.png)

| Error |
| :--- |
| ```java<br>com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.TaskException: Install does not satisfies requirements. Must correspond at least one of enabledFolder<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.InstallCheckTask.run(InstallCheckTask.java:42)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.Task.runWithMappedExceptions(Task.java:36)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoint.runTasks(ApiEndPoint.java:162)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoints.handleRequest(ApiEndPoints.java:79)<br>at com.bigbrassband.gitforjiracloud.appserver.AppServer$SuperHandler.handle(AppServer.java:219)<br>at com.bigbrassband.common.util.httpplumbing.WebServer$InternalRequestHandler.handle(WebServer.java:164)<br>at org.apache.http.protocol.HttpService.doService(HttpService.java:437)<br>at org.apache.http.protocol.HttpService.handleRequest(HttpService.java:342)<br>at com.bigbrassband.common.util.httpplumbing.Worker.run(Worker.java:41)<br>at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)<br>at java.util.concurrent.FutureTask.run(FutureTask.java:266)<br>at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)<br>at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)<br>at java.lang.Thread.run(Thread.java:748)<br>``` |

## Solution

Most users can resolve this issue on their own by re-installing the app.

1.  Navigate to the **Manage Apps** screen

2.  Locate and expand the **Git Integration for Jira Cloud** app

3.  Prior to uninstalling the app - you must **Stop trial\***

4.  Proceed to **Uninstall** the app

5.  Install the **Git Integration for Jira** app


**Stopping trial**<br><br>The evaluation/trial must be stopped before you can uninstall the app

![](/wp-content/uploads/gij-manage-apps-git-cloud-admin.png)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a> or email us at <a href='mailto:support@gitkraken.com'>support@gitkraken.com.
    </div>
    </div>
</div>
<br>

## Related articles

[Why don't I see commits? (Git Integration for Cloud)](/git-integration-for-jira-cloud/why-dont-i-see-commits-git-integration-for-cloud-gij-cloud) (Git Integration for Jira Cloud)

[Repositories missing from Azure DevOps (or VSTS) integration](/git-integration-for-jira-cloud/repositories-missing-from-azure-devops-or-vsts-integration-gij-cloud) (Git Integration for Jira Cloud)

**Licensing error - installCheck failed** (this page)

[Why don't I see the Create branch or pull request features?](/git-integration-for-jira-cloud/why-dont-i-see-the-create-branch-or-pull-request-features-gij-cloud) (Git Integration for Jira Cloud)

[Connection error for self-hosted git servers](/git-integration-for-jira-cloud/connection-error-for-self-hosted-git-servers-gij-cloud) (Git Integration for Jira Cloud)

[SSH key file format is invalid](/git-integration-for-jira-cloud/ssh-key-file-format-is-invalid-gij-cloud) (Git Integration for Jira Cloud)

[Error while reindexing - Java heap space / Object too large, rejecting the pack](/git-integration-for-jira-cloud/error-while-reindexing-java-heap-space-object-too-large-rejecting-the-pack-gij-cloud) (Git Integration for Jira Cloud)

[OAuth connection error or error 401 page with Azure DevOps integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-integration-gij-cloud) (Git Integration for Jira Cloud)

[OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration-gij-cloud) (Git Integration for Jira Cloud)

[Empty list of repositories after integration of Azure Repos](/git-integration-for-jira-cloud/empty-list-of-repositories-after-integration-of-azure-repos-gij-cloud) (Git Integration for Jira Cloud)

[Reconnecting Azure DevOps and VSTS OAuth integrations](/git-integration-for-jira-cloud/reconnecting-azure-devops-and-vsts-oauth-integrations-gij-cloud)
