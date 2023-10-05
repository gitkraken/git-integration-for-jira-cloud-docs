---

title: Microsoft | VSTS | TFS | Azure Repos JMESPath filter examples
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

&nbsp;

![](/wp-content/uploads/azure2-logo.png)

&nbsp;

An optional JMESPath filter can be configured when adding Azure Repos integration or repositories.

&nbsp;

### 1\. Contains (include)

`{value:value[?contains(name, 'example')]}`

This is a filter based on text in the repository name. It will list repositories with names containing the word `'example'`. Do note that the declared string format is case-sensitive.

### 2\. Contains (exclude)

`{value:value[?(!contains(name, 'Test'))]}`

The `"!"` expression excludes all repositories with `'test'` in the repository name.

### 3\. Starts with or ends with

`{value:value[?(starts_with(name, 'git')||(ends_with(name, 'test')))]}`
`{value:value[?(starts_with(name, 'git') || (ends_with(name, 'test')))]}`

Lists repositories with names that starts with `'git'` or ends with `'test'`.

### Other examples

`{value:value[?contains(project.state, 'wellFormed')]}`

`{value:value[?contains(project.name, 'test2')]}`

`{value:value[?contains(project.visibility, 'private')]}`

`{value:value[?contains(project.visibility, 'public')]}`

1.  Displays repositories from projects where its state is _completely created and ready to use_.

2.  List all repositories from project named "_**test2**_".

3.  Displays all private repositories.

4.  Displays all public repositories.

&nbsp;

### Git services that support JMESPath filters

*   [GitHub.com | GitHub Enterprise JMESPath filter examples](/git-integration-for-jira-cloud/github-com-github-enterprise-jmespath-filter-examples-gij-cloud)

*   [GitLab.com | GitLab CE/EE JMESPath filter examples](/git-integration-for-jira-cloud/gitlab-com-gitlab-ce-ee-jmespath-filter-examples-gij-cloud)

*   **Microsoft \| VSTS \| TFS \| Azure Repos JMESPath filter examples** (this page)

*   [Bitbucket JMESPath filter examples](/git-integration-for-jira-cloud/bitbucket-jmespath-filter-examples-gij-cloud)

