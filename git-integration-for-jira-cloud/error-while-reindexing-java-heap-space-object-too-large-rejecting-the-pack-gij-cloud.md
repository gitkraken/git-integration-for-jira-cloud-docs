---

title: Error while reindexing - Java heap space / Object too large, rejecting the pack
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

### Problem

The Git Integration for Jira application uses the [JGit](https://www.eclipse.org/jgit/) library which does not support objects over 2GB in size stored in git repositories.

&nbsp;

### Diagnosis

Jira admins will see a message similar to the one below in the Jira `/application-logs/atlassian-jira.log:`

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

&nbsp;

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

    *   [GitLab: Reducing the repository size using Git](https://docs.gitlab.com/ee/user/project/repository/reducing_the_repo_size_using_git.html)

    *   [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)

*   Move large files to [GitLFS](https://git-lfs.github.com/) which is supported by the Git Integration for Jira app.

*   Filter out the repository from the special integrations (GitHub, GitLab, AWS CodeCommit, Microsoft TFS/Azure DevOps/VSTS, etc) using [Custom API Path](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud) or [JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/'>Support Desk</a> or email us at [gijsupport@gitkraken.com](mailto:gijsupport@gitkraken.com).
    </div>
    </div>
</div>

&nbsp;

### Related articles

[Why don't I see commits? (Git Integration for Cloud)](/git-integration-for-jira-cloud/why-dont-i-see-commits-git-integration-for-cloud-gij-cloud) (Git Integration for Jira Cloud)

[Repositories missing from Azure DevOps (or VSTS) integration](/git-integration-for-jira-cloud/repositories-missing-from-azure-devops-or-vsts-integration-gij-cloud) (Git Integration for Jira Cloud)

[Licensing error - installCheck failed](/git-integration-for-jira-cloud/licensing-error-installcheck-failed-gij-cloud) (Git Integration for Jira Cloud)

[Why don't I see the Create branch or pull request features?](/git-integration-for-jira-cloud/why-dont-i-see-the-create-branch-or-pull-request-features-gij-cloud) (Git Integration for Jira Cloud)

[Connection error for self-hosted git servers](/git-integration-for-jira-cloud/connection-error-for-self-hosted-git-servers-gij-cloud) (Git Integration for Jira Cloud)

[SSH key file format is invalid](/git-integration-for-jira-cloud/ssh-key-file-format-is-invalid-gij-cloud) (Git Integration for Jira Cloud)

**Error while reindexing - Java heap space / Object too large, rejecting the pack** (this page)

[OAuth connection error or error 401 page with Azure DevOps integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-integration-gij-cloud) (Git Integration for Jira Cloud)

[OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration-gij-cloud) (Git Integration for Jira Cloud)

[Empty list of repositories after integration of Azure Repos](/git-integration-for-jira-cloud/empty-list-of-repositories-after-integration-of-azure-repos-gij-cloud) (Git Integration for Jira Cloud)

[Reconnecting Azure DevOps and VSTS OAuth integrations](/git-integration-for-jira-cloud/reconnecting-azure-devops-and-vsts-oauth-integrations-gij-cloud)