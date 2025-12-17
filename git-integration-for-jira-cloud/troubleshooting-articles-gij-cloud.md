---

title: Troubleshooting articles
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

Read through our collection of troubleshooting guides which will show you the recommended workarounds, solutions and other helpful options to get you up and running with the Git Integration for Jira app.

&nbsp;

## On this page

- [Why don't I see commits? (Git Integration for Cloud)](#why-dont-i-see-commits-git-integration-for-cloud)
- [When a GIJ license expires, it shows up as a session error](#when-a-gij-license-expires-it-shows-up-as-a-session-error)
- [Licensing error - installCheck failed](#licensing-error-installcheck-failed)
- [Why don't I see the Create branch or pull request features?](#why-dont-i-see-the-create-branch-or-pull-request-features)
- [Connection error for self-hosted git servers](#connection-error-for-self-hosted-git-servers)
- [Repositories missing from Azure DevOps (or VSTS) integration](#repositories-missing-from-azure-devops-or-vsts-integration)
- [SSH key file format is invalid](#ssh-key-file-format-is-invalid)
- [Error while reindexing - Java heap space / Object too large](#error-while-reindexing-java-heap-space-object-too-large)
- [OAuth connection error or error 401 page with Azure DevOps integration](#oauth-connection-error-or-error-401-page-with-azure-devops-integration)
- [OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](#oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration)
- [Empty list of repositories after integration of Azure Repos](#empty-list-of-repositories-after-integration-of-azure-repos)
- [Reconnecting Azure DevOps and VSTS OAuth integrations](#reconnecting-azure-devops-and-vsts-oauth-integrations)

* * *

&nbsp;

## Why don't I see commits? (Git Integration for Cloud)

![](/wp-content/uploads/gij-troubleshoot-how-do-i-see-commits-top.png)

<p style='font-size:20px;text-align:center;'>&#8681;</p>

### Check if Git Integration for Jira app is installed, licensed and active

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

1.  Follow the [link](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) to install from the Atlassian Marketplace. You can verify that the Git Integration for Jira Cloud app is installed by visiting &nbsp;![](/wp-content/uploads/actions-icon.png) Jira Settings ➜ Apps ➜ **Manage apps**.

2.  Verify that the license is valid and that the application is active (installed, subscription is active).

<img src='/wp-content/uploads/gij-gitcloud-manage-apps-1455.png' style='max-width:100%;margin:25px auto;display:block' />

<p style='font-size:20px;text-align:center;'>&#8681;</p>

<p align=center>Git Integration for Jira Cloud is installed, licensed and active</p>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

### Check if user has "Development Tools" permission

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

Using the **Permission Helper** within Jira Cloud - verify that the user in question has the **Development Tools** permission.

The Permission Helper is available to Jira admins: &nbsp;![](/wp-content/uploads/actions-icon.png) Jira settings ➜ System ➜ **Permission Helper**.

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/21vd3arsj6?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:10px;margin-bottom:15px'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/21vd3arsj6'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

<p align=center>Permissions are correct</p>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

### Check if repository with commit is connected to Jira

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

A couple ways to do this:

*   Via repotories in Manage Repositories page

    ![](/wp-content/uploads/gij-gitcloud-idontsee-commits-via-repo-1455.png)

*   Via Repository Browser (shows the list of all the repositories that are connected in one list)

    ![](/wp-content/uploads/gij-gitcloud-idontsee-commits-reindex-since-commit-1455.png)

<p style='font-size:20px;text-align:center;'>&#8681;</p>

<p align=center>The repository with the missing commit is connected</p>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

### Check if repository has been reindexed since commit

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

Reindexing integrations (or repositories) manually. Note: all repositories are updated regularly without any manual updating required.

Approximately every 8-15 minutes.

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-reindex-manually-01.png)

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-reindex-manually-02.png)

Admins can setup webhooks to index commits immediately

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-webhooks.png)

<p style='font-size:20px;text-align:center;'>&#8681;</p>

<p align=center>The repository has indexed since the commit was pushed</p>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

### Check if repository is associated with Jira project

<b style='background-color:#EAE5FE;padding:1px 5px;color:#412C92; border-radius:3px;margin:0 5px;font-size:small;'>JIRA ADMIN</b>

It allows an admin to associate an integration (and all the repositories) or just a single repository to a set of Jira projects (one, many, or all).

Go to Manage integrations page.

On selected integration/repository, click on &nbsp;![](/wp-content/uploads/actions-icon.png) Actions ➜ **Edit integration**.

Scroll down to **Project Permissions**.

Set project associations to the current integration/repository on the provided box.

Check **Associate all projects** -- if you want the repository to be associated with all Jira projects.

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-associate-projects.png)

<p style='font-size:20px;text-align:center;'>&#8681;</p>

<p align=center>The Jira project is associated with the repository</p>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

### Check if commit has a valid Jira issue key

The association between Jira issues and commits is created by adding the Jira issue key (ABC-123 or MAIN-345) in the commit message.

Example commit messages:

**```ABC-123 added a bug fix```**

**```MAIN-345 adding important new feature.```**

Valid Jira issue key examples are shown in the following screenshot:

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-valid-key.png)

GitLab showing an actual commit and the commit message:

![](/wp-content/uploads/gij-gitcloud-idontsee-commits-gitlab.png)

Check the video for more instructions:

<div class='embed-container embed-container--16-10'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/cs229y2gzj?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin:10px 0 30px 0'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/cs229y2gzj'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

<p align=center>Commit has a valid Jira issue key</p>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

### Try to find indexed commit in Jira Cloud

The commit may be indexed by Jira Cloud - but not associated with any Jira issues. You can verify this with the following steps:

1.  Navigate to **Repository browser**.

2.  Find the repository and then the indexed commit (may need to select the branch).

3.  If you find the commit - you can then fix commit association by clicking on **Change**.

![](/wp-content/uploads/gij-gitcloud-finding-indexed-commits-in-jira-cloud.gif)

<p style='font-size:20px;text-align:center;'>&#8681;</p>

<p align=center>Commit is indexed</p>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

### Check if commit is showing now

Where you can see commits:

*   New Jira issue view

    ![](/wp-content/uploads/gij-gitcloud-idontsee-commits-new-jira.png)

<p style='font-size:20px;text-align:center;'>&#8681;</p>

<p align=center>I still do not see my commits</p>

<p style='font-size:20px;text-align:center;'>&#8681;</p>

<p align=center>Contact <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a> by email or via the <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>GIJ Cloud Support Portal</a>.

&nbsp;

* * *

&nbsp;

## When a GIJ license expires, it shows up as a session error

### Problem

I'm getting an error message that says it's a session error, `SessionTokenNotFoundException`, and I cannot proceed to use any GIJ features anymore.

### Diagnosis

While session errors can just go away when the page is reloaded, this specific session error still remains. Jira admins will see a message similar to the one below:

![](/wp-content/uploads/gij-dc-cloud-session-token-not-found-error.png)

### Solution

Session error message that persist can mean that the trial or license to GIJ had expired. GIJ can detect a license expiration before it tries to detect a valid session. When valid, GIJ will display the correct message about the current license status.

Once you have renewed you Git Integration for Jira app license, this error message should stop appearing. Please note that if the license has been expired for too long, you might start seeing a different error noting 'There is no Enabled installID'. If you start seeing this error message after renewing your license. Please submit a [support request ](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/), as our dev team will need to manually enable your install.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Licensing error - installCheck failed

### Problem

Occasionally when the Git Integration for Jira Cloud app is installed - the licensing fails to fully provision.

### Diagnosis

Jira administrators and users will see a message similar to the one below.

![](/wp-content/uploads/gij-licensing-installcheck-failed-error.png)

**Example Error:**

```java
com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.TaskException: Install does not satisfies requirements. Must correspond at least one of enabledFolder
at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.InstallCheckTask.run(InstallCheckTask.java:42)
at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.Task.runWithMappedExceptions(Task.java:36)
at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoint.runTasks(ApiEndPoint.java:162)
at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoints.handleRequest(ApiEndPoints.java:79)
at com.bigbrassband.gitforjiracloud.appserver.AppServer$SuperHandler.handle(AppServer.java:219)
at com.bigbrassband.common.util.httpplumbing.WebServer$InternalRequestHandler.handle(WebServer.java:164)
at org.apache.http.protocol.HttpService.doService(HttpService.java:437)
at org.apache.http.protocol.HttpService.handleRequest(HttpService.java:342)
at com.bigbrassband.common.util.httpplumbing.Worker.run(Worker.java:41)
at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
at java.util.concurrent.FutureTask.run(FutureTask.java:266)
at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
at java.lang.Thread.run(Thread.java:748)
```

### Solution

Most users can resolve this issue on their own by re-installing the app.

1.  Navigate to the **Manage Apps** screen.

2.  Locate and expand the **Git Integration for Jira Cloud** app.

3.  Prior to uninstalling the app - you must **Unsubscribe**.

4.  Proceed to **Uninstall** the app.

5.  Install the **Git Integration for Jira** app.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Stopping trial</b>
        The evaluation/trial must be stopped before you can uninstall the app.<br>
        <img src='/wp-content/uploads/gij-gitcloud-manage-apps-git-cloud-admin.png' style='margin:25px auto;max-width:100%;display:block;' />
    </div>
    </div>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>support@gitkraken.com.</a>
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Why don't I see the Create branch or pull request features?

### Problem

Users cannot see the **Create branch** or **Create pull/merge request** actions on the [Jira issue developer panel](/git-integration-for-jira-cloud/jira-git-integration-development-panel-gij-cloud).

<img src='/wp-content/uploads/gij-gitcloud-troubleshoot-createbranch-pullrequest.png' style='max-width:100%;margin:25px auto;display:block;' />

### Solution

The **Create branch** and **Create pull/merge requests** features are enabled by connecting to one of the Full feature integrations.

<img src='/wp-content/uploads/gij-gitcloud-managed-ui-webhook-idx-setup-c.png' style='max-width:100%;margin:25px auto;display:block;' />

1.  Navigate to the Manage integrations page.

2.  Click **Add integration** and select OAuth or PAT integration options (GitHub, GitLab, etc.).

3.  Complete the integration steps of the connection wizard.

See our [Integration Guides](/git-integration-for-jira-cloud/integration-guide-gij-cloud) for each Full feature integration option.

The regular Git integration and Limited connect feature Git option does not offer the Create branch and Create pull/merge request features.

<img src='/wp-content/uploads/gij-add-new-integration-plain-git-sel.png' style='max-width:100%;margin:25px auto;display:block;' />

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Connection error for self-hosted git servers

### Problem

Jira admins are not able to connect Jira Cloud to self-hosted git servers when hosted behind a firewall or otherwise not reachable by the Git Integration for Jira Cloud indexing service.

### Diagnosis

Jira admins will see a message similar to the one below when connecting to self-hosted git servers hosted behind a firewall or otherwise not reachable.

**Example Error:**

```java
com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.TaskException: com.bigbrassband.gitforjiracloud.indexer.sources.TrackedGitLabRepoException: Can not connect to GitLab server<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.Task.runWithMappedExceptions(Task.java:56)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoint.runTasks(ApiEndPoint.java:162)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.ApiEndPoints.handleRequest(ApiEndPoints.java:79)<br>at com.bigbrassband.gitforjiracloud.appserver.AppServer$SuperHandler.handle(AppServer.java:219)<br>at com.bigbrassband.common.util.httpplumbing.WebServer$InternalRequestHandler.handle(WebServer.java:164)<br>at org.apache.http.protocol.HttpService.doService(HttpService.java:437)<br>at org.apache.http.protocol.HttpService.handleRequest(HttpService.java:342)<br>at com.bigbrassband.common.util.httpplumbing.Worker.run(Worker.java:41)<br>at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)<br>at java.util.concurrent.FutureTask.run(FutureTask.java:266)<br>at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)<br>at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)<br>at java.lang.Thread.run(Thread.java:748)<br>Caused by: com.bigbrassband.gitforjiracloud.indexer.sources.TrackedGitLabRepoException: Can not connect to GitLab server<br>at com.bigbrassband.gitforjiracloud.indexer.sources.GitlabApiMonster.getGitlabApi(GitlabApiMonster.java:34)<br>at com.bigbrassband.gitforjiracloud.indexer.sources.GitlabRepoSource.getRepositories(GitlabRepoSource.java:47)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.git.repos.PingRepoTask.pingRepoSource(PingRepoTask.java:91)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.git.repos.PingRepoTask.run(PingRepoTask.java:71)<br>at com.bigbrassband.gitforjiracloud.appserver.apiendpoint.tasks.Task.runWithMappedExceptions(Task.java:36)<br>... 12 more<br>Caused by: org.gitlab.api.GitlabAPIException<br>at org.gitlab.api.http.GitlabHTTPRequestor.handleAPIError(GitlabHTTPRequestor.java:543)<br>at org.gitlab.api.http.GitlabHTTPRequestor.to(GitlabHTTPRequestor.java:201)<br>at org.gitlab.api.http.GitlabHTTPRequestor.to(GitlabHTTPRequestor.java:167)<br>at org.gitlab.api.GitlabAPI.getVersion(GitlabAPI.java:3199)<br>at org.gitlab.api.GitlabAPI.createPATAuthOnly(GitlabAPI.java:158)<br>at org.gitlab.api.GitlabAPI.create(GitlabAPI.java:145)<br>at com.bigbrassband.gitforjiracloud.indexer.sources.GitlabApiMonster.getGitlabApi(GitlabApiMonster.java:29)<br>... 16 more<br>Caused by: com.fasterxml.jackson.core.JsonParseException: Unexpected character ('<' (code 60)): expected a valid value (number, String, array, object, 'true', 'false' or 'null')
```

### Solution

See [Whitelist GIJ Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Repositories missing from Azure DevOps (or VSTS) integration

### Problem

Some or all repositories in Azure DevOps (or Visual Studio Team Services - VSTS) integrations are not showing or seen by the integration user.

### Diagnoses

**1\. Permissions**

The connecting Azure DevOps user must have access to the repository to be added to the Git Integration for Jira app.

**2\. Access Level**

Jira admins will notice that some repositories expected in the Azure DevOps integration do not appear in the Git Integration for Jira app.  `Basic` or `Visual Studio Professional` access is the minimum access level necessary for the Git Integration for Jira app as **Code** access level is required.

![](/wp-content/uploads/gij-azure-devops-code-access-level.png)

For more information - see Microsoft's article on [Azure DevOps Access Levels.](https://docs.microsoft.com/en-us/azure/devops/organizations/security/access-levels?view=azure-devops)

**3\. Repository format**

Only git format repositories are supported by the Git Integration for Jira app. Team Foundation Version Control (TFVC) formatted repositories are not supported.

### Solutions

**1\. Permissions**

Assign the connecting Azure DevOps user appropriate access to the repository or repositories.

**2\. Access level**

 Grant at least `Basic` or `Visual Studio Professional` access is the minimum access level necessary for the Git Integration for Jira app.

**3\. Repository format**

Convert the Team Foundation Version Control (TFVC) formatted repositories to git format repositories

*   Microsoft article: [**Migrate from TFVC to Git**](https://docs.microsoft.com/en-us/devops/develop/git/migrate-from-tfvc-to-git)

*   Microsoft article: [**Import repositories from TFVC to Git**](https://docs.microsoft.com/en-us/azure/devops/repos/git/import-from-tfvc?view=azure-devops)

### Workarounds

See the following sections on this page:

- [OAuth connection error or error 401 page with Azure DevOps integration](#oauth-connection-error-or-error-401-page-with-azure-devops-integration)
- [OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](#oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration)
- [Empty list of repositories after integration of Azure Repos](#empty-list-of-repositories-after-integration-of-azure-repos)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## SSH key file format is invalid

### Problem

Git Integration for Jira application SSH keys:

1.  Must not be created using the OpenSSH format

2.  Must be the private SSH key

3.  Must use the supported certificate format: RSA

4.  Must use the supported storage format: OpenSSL PEM

### Diagnosis

Jira admins will see a message similar to the one below when adding the SSH key:

> _The key format is invalid. Please check your private key._

<img src='/wp-content/uploads/gij-private-key.png' width=494 height=454 style='max-width:100%;display:block;margin:25px auto;' />

Full error (stack trace) available in the Manage Git Repositories wizard or in Jira logs `/application-logs/atlassian-jira.log`:

**Example Error:**

```java
com.bigbrassband.jira.git.exceptions.repository.InvalidPrivateKeyException: Private SSH key is invalid or empty
at com.bigbrassband.jira.git.services.ssh.KeyManagerImpl.needPassphrase(KeyManagerImpl.java:103)
at com.bigbrassband.jira.git.rest.wizard.WizardResource.validateRepoOrigin(WizardResource.java:104)
at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
...
at org.apache.tomcat.util.net.NioEndpoint$SocketProcessor.doRun(NioEndpoint.java:1498)
at org.apache.tomcat.util.net.SocketProcessorBase.run(SocketProcessorBase.java:49)
at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
at org.apache.tomcat.util.threads.TaskThread$WrappingRunnable.run(TaskThread.java:61)
at java.lang.Thread.run(Thread.java:748)
Caused by: com.jcraft.jsch.JSchException: invalid privatekey: [C@17h421rm
at com.jcraft.jsch.KeyPair.load(KeyPair.java:664)
at com.bigbrassband.jira.git.services.ssh.KeyManagerImpl.needPassphrase(KeyManagerImpl.java:99)
... 264 more
```

### Cause

Jira admin has provided an SSH public key or an SSH private key with an incorrect format.

### Solutions

**1. Create a new SSH key:**

**On Linux and macOS:**

Use the following command to create a certificate:

```powershell
ssh-keygen -t rsa -b 4096 -m pem -C your_email@example.com
```

<div class="bbb-callout bbb--alert">
  <div class="irow">
    <div class="ilogobox">
      <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
      MacOS often incorrectly creates an OpenSSH format certificate. For more details, see information on this <a href='https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key' target='_blank'><b>common problem</b></a>.
    </div>
  </div>
</div>

**On Windows:**

Download [**PuTTY**](https://www.putty.org/) and use PuTTYgen to generate an SSH key pair:

1.  Set _**Type of key...**_ to **RSA**.

2.  Set _**Number of bits...**_ to **4096**.

3.  Click **Generate**. Move mouse pointer on the blank area as instructed.

4.  Follow screen instructions such as moving your mouse pointer on random locations on the blank area of the PuTTYgen dialog. Do this until the progress bar completely fills up and the SSH key pair is generated.

5.  Entering a **Passphrase** for the generated key is optional but will ensure a more secure connection.

6.  Save your generated public and private key to a file by clicking the respective options.

7.  Copy the generated key. This is the public key that you will be using on the SSH configuration page of your git host.

8.  For the private key, PuTTY creates a private key in its own ".ppk" format. Convert it to ".pem" via menu **Conversions** \> **Export OpenSSH key** in PuTTYgen. Add/upload this file to Git Integration for Jira app \> **SSH Keys** or when prompted on connecting SSH git repositories in Jira.

**2.**  Create a new SSH key using RSA certificate format. See Solution #1.

**3.**  Use OpenSSL PEM storage format. See Solution #1.

**4.**  Provide the public SSH key to the SSH configuration of your git host.

**5.**  Provide the private SSH key to the Git Integration for Jira app \> **SSH Keys** or when prompted on connecting SSH git repositories in Jira.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Error while reindexing - Java heap space / Object too large

### Problem

The Git Integration for Jira application uses the [JGit](https://www.eclipse.org/jgit/) library which does not support objects over 2GB in size stored in git repositories.

### Diagnosis

Jira admins will see a message similar to the one below in the Jira `/application-logs/atlassian-jira.log:`

**Example Error:**

```java
Cannot auto-deploy a new repository https://server/project/repository.git
com.bigbrassband.jira.git.exceptions.InvalidRemoteOperationException: Specified origin https://server/project/repository.git is incorrect or not supported
at com.bigbrassband.jira.git.services.gitmanager.MultipleGitRepositoryManagerImpl.setupRepository(MultipleGitRepositoryManagerImpl.java:800)
at com.bigbrassband.jira.git.services.gitmanager.MultipleGitRepositoryManagerImpl.deployRepository(MultipleGitRepositoryManagerImpl.java:868)
at com.bigbrassband.jira.git.services.async.DoSynchronizationOfAggregatedRepoTask.createNewRepository(DoSynchronizationOfAggregatedRepoTask.java:156)
at com.bigbrassband.jira.git.services.async.DoSynchronizationOfAggregatedRepoTask.run(DoSynchronizationOfAggregatedRepoTask.java:117)
at com.bigbrassband.jira.git.services.async.BigReindexTask.synchronize(BigReindexTask.java:185)
at com.bigbrassband.jira.git.services.async.BigReindexTask.run(BigReindexTask.java:95)
at com.bigbrassband.jira.git.services.async.AsyncProcessorImpl$AsyncTaskWrapper.run(AsyncProcessorImpl.java:110)
at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
at java.util.concurrent.FutureTask.run(FutureTask.java:266)
at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
at java.lang.Thread.run(Thread.java:748)<br>Caused by: org.eclipse.jgit.api.errors.TransportException: Object too large (2,271,263,009 bytes), rejecting the pack. Max object size limit is 2,147,483,639 bytes.
at org.eclipse.jgit.api.FetchCommand.call(FetchCommand.java:254)
at org.eclipse.jgit.api.CloneCommand.fetch(CloneCommand.java:306)
at org.eclipse.jgit.api.CloneCommand.call(CloneCommand.java:200)
at com.bigbrassband.jira.git.services.gitmanager.MultipleGitRepositoryManagerImpl.runCloneCommand(MultipleGitRepositoryManagerImpl.java:693)
at com.bigbrassband.jira.git.services.gitmanager.MultipleGitRepositoryManagerImpl.setupRepository(MultipleGitRepositoryManagerImpl.java:789)
... 11 more
```

### Solutions

<div class="bbb-callout bbb--alert">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Making any changes to a git repository's history can result in loss of data. Please do proceed with care.
    </div>
    </div>
</div>

*   Remove objects larger than 2GB from the git repository history. See following articles for suggestions:

    *   [Removing large files from Git without losing history](https://support.acquia.com/hc/en-us/articles/360004334093-Removing-large-files-from-Git-without-losing-history)

    *   [GitHub: Removing files from a repository's history](https://help.github.com/en/articles/removing-files-from-a-repositorys-history)

    *   [GitLab: Reducing the repository size using Git](https://docs.gitlab.com/ee/user/project/repository/reducing_the_repo_size_using_git.html)

    *   [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)

*   Move large files to [GitLFS](https://git-lfs.github.com/) which is supported by the Git Integration for Jira app.

*   Filter out the repository from the special integrations (GitHub, GitLab, AWS CodeCommit, Microsoft TFS/Azure DevOps/VSTS, etc) using [Custom API Path](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud) or [JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## OAuth connection error or error 401 page with Azure DevOps integration

### Problem

You are getting the OAuth connection error or a 401 web page error is displayed when integrating Azure DevOps.

### Diagnosis

These issues are related to the security settings in your Azure DevOps portal where certain security policies are rejecting connections to Git Integration for Jira app.

### Cause

On most cases, this is caused by an OAuth setting being turned OFF.

### Solution

Git Integration for Jira Cloud requires Git admins to allow the third-party app access OAuth security policy in their organization settings:

1.  On your VSTS/Azure DevOps portal, go to the home page.

2.  Click an organization then go to **Organization Settings** (sidebar).

3.  Under _**Security**_, click **Policies**.

4.  Ensure that the **Third-party application access via OAuth** option is set to ON.

![](/wp-content/uploads/gij-vsts-azure-devops-org-cfg-policy-oauth.png)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## OAuth connection error or error 401 page with Azure DevOps with Active Directory integration

### Problem

You are getting the OAuth connection error or a 401 web page error is displayed when integrating with Azure DevOps connected to Active Directory.

### Diagnosis

These issues are related to the security settings in your Azure DevOps portal where certain security policies are rejecting connections to Git Integration for Jira app.

Moreover, for Azure Active Directory connections, the conditional access policy setting (when enabled) will force all untrusted location to require MFA in order to connect with Azure DevOps.

### Cause

For Azure DevOps with Active Directory connections, this is due to the conditional access security setting being enabled.

### Solution

Git Integration for Jira Cloud requires Git admins to allow the third-party app access OAuth security policy in their organization settings:

1.  On your VSTS/Azure DevOps portal, go to the home page.

2.  Click an organization then go to **Organization Settings** (sidebar).

3.  Under _**Security**_, click **Policies**.

4.  Ensure that the **Third-party application access via OAuth** option is set to ON.

![](/wp-content/uploads/gij-vsts-azure-devops-org-cfg-policy-oauth.png)

For projects connected with Azure Active Directory, the above requirement must also be enabled and set the conditional access policy validation to OFF:

![](/wp-content/uploads/gij-enable-conditional-access-policy-AD.png)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Empty list of repositories after integration of Azure Repos

### Problem

After integrating Azure DevOps to Jira, the list filter for Azure repositories returns empty.

### Diagnosis

The integration status is <b style='background-color:#E2FCEF; padding:1px 5px; color:#006745; border-radius:3px; margin: 0 5px; font-size: small;'>INDEXED</b> but users still see a blank list on the Manage repositories list with MS Azure list filter set.

![](/wp-content/uploads/gij-gitcloud-azure-no-repo-manage-repos.png)

### Solution

If the integration is using the oAuth access, switch to personal access token instead. Also check PAT configuration when [Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud).

If the problem still persists, follow the solutions outlined in the following sections on this page:

- [Reconnecting Azure DevOps and VSTS OAuth integrations](#reconnecting-azure-devops-and-vsts-oauth-integrations)
- [OAuth connection error or error 401 page with Azure DevOps integration](#oauth-connection-error-or-error-401-page-with-azure-devops-integration)
- [OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](#oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration)

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

&nbsp;

* * *

&nbsp;

## Reconnecting Azure DevOps and VSTS OAuth integrations

<b style='background-color:#FFEED1; padding:1px 5px; color:#CC5900; border-radius:3px; margin: 0 5px; font-size: small;'>WORKAROUND</b>

On March 2, 2022, all OAuth integrations between Git Integration for Jira and Azure DevOps and VSTS were interrupted. Our investigation found that Microsoft OAuth apps' client secrets expire after 5 years. This limitation has a single workaround and that is -- **for all customers to reconnect**. We apologize for this inconvenience and interruption in service. Below are the steps to reconnect.

### Requirements:

1.  Jira administrator permissions

2.  Azure DevOps / VSTS account or service account.

### Steps:

1.  Go to the **Manage integrations** page in the [Git Integration for Jira](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview) app.

2.  Click on the integration name.

3.  Click on **Reconnect**.

4.  Login to Azure DevOps / VSTS with the account you wish to associate with Git Integration for Jira Cloud.

### Videos:

**GIJ Cloud**

<div class='embed-container' style='padding-bottom:47.29%'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/6jon0nfpu4?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:12px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/6jon0nfpu4'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

&nbsp;

**GIJ Server/DC**

<div class='embed-container' style='padding-bottom:50.33%'>
    <iframe width='709' height='443' src='https://fast.wistia.com/embed/iframe/63ndpswgmc?videoFoam=true' frameborder='0' allowfullscreen ></iframe>
</div>

<div align='center' style='margin-top:12px;'>
    <i>Right click <a href='https://bigbrassband.wistia.com/medias/63ndpswgmc'><b>here</b></a> to open this video in a new browser tab for more viewing options.</i>
</div>

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>

