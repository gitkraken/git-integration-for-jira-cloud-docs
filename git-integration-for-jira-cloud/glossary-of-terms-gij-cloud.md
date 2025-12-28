---

title: Glossary of terms
description: Definitions of common terms used in Git Integration for Jira documentation
taxonomy:
    category: git-integration-for-jira-cloud

---

### Git

Git is a distributed version control system that tracks changes in files. Developers use Git repositories to manage and maintain their source code.

### Branch

A branch is a temporary copy of source code for a single purpose, such as adding a particular feature or fixing a bug.

### Merge

A merge safely moves changes from one branch to another, typically merging into the main or master branch.

### Jira Server

Jira Server is a self-hosted Jira Software installation that runs on your own server, whether hosted by AWS or other hosting services.

### Jira Cloud

Jira Cloud is a cloud-hosted service managed by Atlassian and sold as a subscription service.

### Issue Key

The issue key is a combination of the project key and issue number. For example, if the project key is `TEST` and there is issue `#123` in the `TEST` project, the resulting issue key is `TEST-123`. Include the issue key in your commit message so that pushed commits are associated with that issue and can be viewed inside Jira.

### Remote Repository

A remote repository is the central hosting location used by your team for pushing commits and pulling updates.

### Local Repository Clone

A clone of the remote repository located on the same server as your Jira service. It is cached locally for performance reasons and queried every time the list of git commits is displayed.

### Lucene Indexes

Lucene is an index service within your Jira instance. It ships with Jira, and Git Integration for Jira also uses it.

This database stores information about all commits (comment, author, etc.) as well as the branch name to which the commit belongs.

&nbsp;
* * *

[**Prev:** Localization support](/git-integration-for-jira-cloud/localization-support-gij-cloud)

[**Next:** Licensing notice](/git-integration-for-jira-cloud/licensing-notice-gij-cloud)

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
