---

title: Bitbucket JMESPath filter examples
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

&nbsp;

![](/wp-content/uploads/bitbucket-mobile2.png)

&nbsp;

An optional JMESPath filter can be configured when adding Bitbucket integration or repositories.

&nbsp;

### 1\. Contains (include)

```java
{values: values[?contains(name, 'myrepo')]}
```

This is a filter based on the text in the repository name. It will list repositories with names that contain the word `'myrepo'`. Do note that the declared string format is case-sensitive.

### 2\. Starts with or ends with

```java
{values: values[?starts_with(name, 'test') || ends_with(name, 'lab')]}
```

Lists repositories with names that starts with `'test'` or ends with `'lab'`.

### 3\. Contains (exclude)

```java
{values: values[?(!contains(name, 'firstword'))]}

{values: values[?(!contains(name, 'firstword')) || (!contains(name, 'secondword'))]}
```

1 – Lists repositories with names that either do not contain the word `'firstword'`.

2 – Lists repositories with names that either do not contain the words `‘firstword’` OR `‘secondword’`.

The `!condition` must be wrapped in a parenthesis so it won’t invert the whole expression.

### 4\. Has repository name

```java
{values: values[?(name == 'repo1name') || (name == 'repo2name')]}
```

Lists repositories with names `'repo1name'` and `'repo2name'`.

&nbsp;

### Git services that support JMESPath filters

*   [GitHub.com | GitHub Enterprise JMESPath filter examples](/git-integration-for-jira-cloud/github-com-github-enterprise-jmespath-filter-examples-gij-cloud)

*   [GitLab.com | GitLab CE/EE JMESPath filter examples](/git-integration-for-jira-cloud/gitlab-com-gitlab-ce-ee-jmespath-filter-examples-gij-cloud)

*   [Microsoft | VSTS | TFS | Azure Repos JMESPath filter examples](/git-integration-for-jira-cloud/microsoft-vsts-tfs-azure-repos-jmespath-filter-examples-gij-cloud)

*   **Bitbucket JMESPath filter examples** (this page)

