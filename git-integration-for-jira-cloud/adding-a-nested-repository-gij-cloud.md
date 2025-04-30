---

title: Adding and connecting a nested repository
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

## Adding a nested repository with Git Submodule

While, GitHub does not allow nested repositories (Git doesn't allow this for bare repositories), you can use submodules to nest repositories on the "client side" in the working tree:

1.  Clone the parent directory.

2.  Add the sub-repository as a [submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules):

    `git submodule add https://github.com/\<username\>/\<sub_repo\>.git`

    The `\<sub_repo\>` module will then be linked to the parent repo and can be found in the `\<sub_repo\>` directory.

3.  Commit (`.gitmodules` and `\<sub_repo\>`), push and you're done.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <code>git submodule add</code> command works on most Git services that supports it. Check with your Git service documentation on how to add a submodule.
    </div>
    </div>
</div>

&nbsp;

## Connecting a nested repository with Git Integration for Jira Cloud app

Connecting a nested repository is similar to adding a plain Git repository through the Git Integration for Jira Cloud app.

1.  Go to the **Manage integrations** configuration page from your Jira dashboard **Apps** menu ➜ **Git Integration: Manage integrations**.

    ![](/wp-content/uploads/gij-cloud-nested-repo-add-integration-new.png)

2.  Click **Add integration** then click **Plain Git repository** on the list of hosting service or use the **Quick start** panel. The following screen is displayed.

    ![](/wp-content/uploads/gij-cloud-nested-repo-add-integration-single.png)

3.  For the Quick start panel, paste the **clone URL of the submodule** from your git service portal. If you clicked on Plain Git Repository, paste the **clone URL of the submodule** from your git service portal on the following screen.

    For this guide, we will be using GitLab as an example.

    ![](/wp-content/uploads/gij-cloud-nested-repo-add-integration-auth.png)

4.  On the Connect single Git repository screen, the input fields depends on what type of clone URL you’ll be using:

    *   **HTTPS authentication** – Enter your credentials such as username and password. For the password, provide the PAT as the password.

    *   **SSH authentication** – Provide the private ssh key. If your SSH key requires a passphrase, provide that as well.

    For this guide, we used an HTTP(S) authentication as an example. Therefore, enter **Username** and **PAT** (personal access token) as the password. Click **Add integration** to proceed.

5.  On the Settings screen, leave all options as is. Click **Finish** to complete this setup.

&nbsp;

The nested repository configuration is added to the Manage integrations list.

&nbsp;

## Connecting an integration that contains nested repositories

Adding an integration containing nested repositories is similar to connecting a new integration via the Git Integration for Jira Cloud app.

![](/wp-content/uploads/gij-cloud-nested-repo-add-integration-new.png)

1.  Go to the **Manage integrations** configuration page. Click **Add integration**. The following screen is displayed.

    ![](/wp-content/uploads/git-cloud-nested-repo-add-full-integration-new.png)

2.  For this session, we will use GitLab as an example. Click the **GitLab** full-feature integration icon on the integration panel. The following screen is displayed.

    ![](/wp-content/uploads/gij-cloud-nested-repo-add-full-integration-pat.png)

3.  You can either use the OAuth or PAT integration connection. For OAuth integration, enter the required credentials. For PAT integration, enter the personal access token.

    Click **Connect and select repositories** to continue.

    The Git Integration for Jira Cloud app will scan the remote git service and connect detected repositories.

    ![](/wp-content/uploads/gij-cloud-nested-repo-add-full-integration-select-repos.png)

4.  On the **Select repositories to connect** screen, select one or more repositories to connect or connect all repositories and groups. Click **Connect repositories** to continue.

5.  On the **Configure additional options** screen, leave all options as is. Click **Save options** to complete this setup.

&nbsp;

The integration configuration containing nested repositories is added to the Manage integrations list.

To view the nested repository settings, go to the Manage repositories page and navigate to that specific nested repository.

&nbsp;
* * *

[**Prev:** Nested repository](/git-integration-for-jira-cloud/nested-repository-gij-cloud)

[**Next:** Edit a nested repository settings](/git-integration-for-jira-cloud/edit-nested-repository-settings-gij-cloud)


