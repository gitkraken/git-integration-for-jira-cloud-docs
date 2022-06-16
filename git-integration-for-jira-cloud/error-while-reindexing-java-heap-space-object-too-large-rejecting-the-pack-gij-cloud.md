---

title: Error while reindexing - Java heap space / Object too large, rejecting the pack
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Problem

The Git Integration for Jira application uses the [JGit](https://www.eclipse.org/jgit/) library which does not support objects over 2GB in size stored in git repositories.

## Diagnosis

Jira admins will see a message similar to the one below in the Jira `/application-logs/atlassian-jira.log:`

| **Error** |
| --- |
| ```java<br>Сan't auto-deploy a new repository https://server/project/repository.git<br>com.bigbrassband.jira.git.exceptions.InvalidRemoteOperationException: Specified origin https://server/project/repository.git is incorrect or not supported<br>        at com.bigbrassband.jira.git.services.gitmanager.MultipleGitRepositoryManagerImpl.setupRepository(MultipleGitRepositoryManagerImpl.java:800)<br>        at com.bigbrassband.jira.git.services.gitmanager.MultipleGitRepositoryManagerImpl.deployRepository(MultipleGitRepositoryManagerImpl.java:868)<br>        at com.bigbrassband.jira.git.services.async.DoSynchronizationOfAggregatedRepoTask.createNewRepository(DoSynchronizationOfAggregatedRepoTask.java:156)<br>        at com.bigbrassband.jira.git.services.async.DoSynchronizationOfAggregatedRepoTask.run(DoSynchronizationOfAggregatedRepoTask.java:117)<br>        at com.bigbrassband.jira.git.services.async.BigReindexTask.synchronize(BigReindexTask.java:185)<br>        at com.bigbrassband.jira.git.services.async.BigReindexTask.run(BigReindexTask.java:95)<br>        at com.bigbrassband.jira.git.services.async.AsyncProcessorImpl$AsyncTaskWrapper.run(AsyncProcessorImpl.java:110)<br>        at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)<br>        at java.util.concurrent.FutureTask.run(FutureTask.java:266)<br>        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)<br>        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)<br>        at java.lang.Thread.run(Thread.java:748)<br>Caused by: org.eclipse.jgit.api.errors.TransportException: Object too large (2,271,263,009 bytes), rejecting the pack. Max object size limit is 2,147,483,639 bytes.<br>        at org.eclipse.jgit.api.FetchCommand.call(FetchCommand.java:254)<br>        at org.eclipse.jgit.api.CloneCommand.fetch(CloneCommand.java:306)<br>        at org.eclipse.jgit.api.CloneCommand.call(CloneCommand.java:200)<br>        at com.bigbrassband.jira.git.services.gitmanager.MultipleGitRepositoryManagerImpl.runCloneCommand(MultipleGitRepositoryManagerImpl.java:693)<br>        at com.bigbrassband.jira.git.services.gitmanager.MultipleGitRepositoryManagerImpl.setupRepository(MultipleGitRepositoryManagerImpl.java:789)<br>        ... 11 more<br>``` |

## Solutions

Making any change to a git repository's history can result in loss of data. Proceed with care.

*   Remove objects larger than 2GB from the git repository history. See following articles for suggestions:

    *   [Removing large files from Git without losing history](https://support.acquia.com/hc/en-us/articles/360004334093-Removing-large-files-from-Git-without-losing-history)

    *   [GitHub: Removing files from a repository's history](https://help.github.com/en/articles/removing-files-from-a-repositorys-history)

    *   [GitLab: Reducing the repository size using Git](https://docs.gitlab.com/ee/user/project/repository/reducing_the_repo_size_using_git.html)

    *   [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)

*   Move large files to [GitLFS](https://git-lfs.github.com/) which is supported by the Git Integration for Jira app.

*   Filter out the repository from the special integrations (GitHub, GitLab, AWS CodeCommit, Microsoft TFS/Azure DevOps/VSTS, etc) using [Custom API Path](/git-integration-for-jira-cloud/working-with-custom-api-path-gij-cloud) or [JMESPath Filters](/git-integration-for-jira-cloud/working-with-jmespath-filters-gij-cloud).


**Contact Us**

If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).

