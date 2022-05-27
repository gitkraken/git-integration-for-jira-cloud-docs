---

title: Pull or merge requests (Development panel)
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The **Pull Requests** (GitHub or other connected git hosts) or **Merge Requests** (if GitLab is connected) section lists the merge/pull requests and their status. All merge/pull requests from all types of sources are shown here (for now, GitLab/GitHub/Azure/TFS/VSTS).

The displayed information depends on which supported git hosts are connected to Jira. For example:

*   GitLab integrations only  –  merge requests

*   Other integrations  –  pull requests

*   Both GitLab and GitHub integrations  –  separate sections for merge requests and pull requests


For necessary permissions that GitLab users must have for creating pull/merge requests, see [**GitLab Documentation: Permissions »**](https://docs.gitlab.com/ee/user/permissions.html).

This function does not work for single git repository connections. Use the Full feature integration instead.

##
Getting started

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025925/gitcloud-devpanel-create-pullreq-sel.png?version=1&modificationDate=1637293973700&cacheVersion=1&api=v2&width=340&height=465)

If a git host is connected to Jira, create a pull/merge request by clicking **Create pull request** or **Create merge request** label link on the Jira Git integration development panel. The following dialog is displayed.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025925/gitcloud-create-pr-dlg.png?version=1&modificationDate=1635941712612&cacheVersion=1&api=v2&width=680&height=327)

*   Select **Repository** from the list.
    GITHUB If there are several repositories with the same name, the listed GitHub repositories will have their names attached with a GitHub organization name. For example, `BigBrassBand/second-webhook-test-repo`.
    GITLAB If there are several repositories with the same name, the listed GitLab repositories will have their names attached with a GitLab owner name. For example, `johnsmith/second-webhook-test-repo`.

*   Choose a branch as the **Source branch**. This branch will be merged to the target branch.

*   Set _**master**_ as the **Target branch**.

*   Enter a descriptive **Title** or leave it as is (recommended).


OPTIONAL
Jira users can provide their own PATS even if they are not required/mandated by the Jira admin. Click on the **Provide a personal access token** label. A dialog for setting up personal access tokens is displayed (see below).

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025925/gitcloud-setup-pat-dlg.png?version=1&modificationDate=1635942313659&cacheVersion=1&api=v2&width=442&height=292)

*   Paste a valid PAT of the current user to proceed. Invalid PATs will fail the branch creation process.

*   Click on **New token** to generate a new PAT via your remote git host service.

*   Click **Update** to use this PAT and save it to the current user profile. Otherwise, click **Cancel** to discard setting up PAT.


Click **Create pull request** on the Create pull request dialog. The newly-created pull request is now listed in the developer panel under **Pull requests**.

This feature is available on connected GitLab, GitHub, Microsoft TFS/VSTS and AWS CodeCommit git hosts for Jira Cloud.

##
GitLab merge request

If you want to create a merge request for GitLab, click **Create merge request**. It has the same process described in the pull request creation steps above.

The merge request is displayed on the developer panel and will also be associated to the mentioned Jira issue by fulfilling the following condition:

*   Merge request **Title** contains the issue key. For example, `TEST-1-Fix-binaries`.


This will also allow a service user to associate a Merge/Pull Request with multiple Jira issues regardless of commit associations.

BigBrassBand recommends service users to enable pull/merge requests webhook trigger events. This way, any changes to pull/merge requests gets reindexed quickly.


The Pull/merge request list provides status information about the pull/merge request if it is opened or merged. For example:

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025925/gitcloud-devpanel-merge-req.png?version=1&modificationDate=1635943761256&cacheVersion=1&api=v2&width=340&height=154)


Hover the mouse pointer on the pull/merge request label to see information of the repository and branch where it belongs.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923025925/gitcloud-devpanel-merge-req-hover.png?version=1&modificationDate=1635943769049&cacheVersion=1&api=v2&width=442&height=206)

* * *

### Video Guide (UPDATED VIDEO COMING SOON)

_Right click_ [_**here**_](https://bigbrassband.wistia.com/medias/1jwzeex5qa) _to open this video in a new tab/window for more viewing options._

[« Branches (Developer panel)](/wiki/spaces/GITCLOUD/pages/1923025879)

[Git tags »](/git-integration-for-jira-cloud/git-tags-gij-cloud/)

