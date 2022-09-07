---

title: Working with Custom API Path
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

The Custom API Path is a relative path that starts with "/". The maximum allowed length is **2000** characters. The integration will use the relative REST API path to retrieve the list of tracked repositories.

The Custom API Path is called in the integration setup, settings changes, on a regular scheduled reindex and for a manual reindex.

**What’s on this page:**
- [Accessible Locations](#accessible-locations)
- [GitHub.com examples](#githubcom-examples)
- [GitHub Enterprise examples](#github-enterprise-examples)
- [GitLab.com | GitLab CE/EE examples](#gitlabcom--gitlab-ceee-examples)
- [Bitbucket Cloud examples](#bitbucket-cloud-examples)

<hr>

## Accessible Locations

*   Go to Manage Git repositories page ➜ Full feature integration wizard ➜ **Connect** screen ➜ _Advanced_ ➜ **Custom API Path**. In this case, we use GitHub as an example:

    <img src='/wp-content/uploads/gij-gitcloud-autoconnect-github-custom-api-path.png' width=566 height=510 style='max-width:100%;margin:25px 0' />

*   Go to Manage Git repositories page ➜ <img src='/wp-content/uploads/actions-icon.png' /> Actions ➜ Edit integration settings (for integration) or Edit repository settings (for repositories) ➜ Integration settings section ➜ **Custom API Path**.

    <img src='/wp-content/uploads/gij-gitcloud-actions-edit-integration-settings-cAPI-path.png' width=566 height=211 style='max-width:100%;margin:25px 0' />

<hr>

<img src='/wp-content/uploads/github-mobile-dark.png' width=48 height=48 style='margin-top:30px;' />

## GitHub.com examples

**1. Lists all repositories (default)**

```java
/user/repos
```

Gets a list of repositories. This is the same as when no API path is specified.

**2. Display all repositories from \<username\>**

```java
/users/<username>/repos
```

Gets a list of public repositories for the specified user, **\<username\>**.

For example: `/users/johnsmith/repos`

**3. Displays starred repositories**

```java
/user/starred
```

Gets the list of starred repositories for the authenticated user.

```java
/users/<username>/starred
```

Gets the list of starred public/private repositories for the specified user, **\<username\>**.

For example: `/users/johnsmith/starred`

**4. List all repositories for the specified organization**

```java
/orgs/<org>/repos
```

Gets a list of repositories for the specified org, **\<org\>**. _BigBrassBand_

**For instance:**<br>
```/orgs/BigBrassBand/repos```<br>
This will filter for repositories only within the org: BigBrassBand. This works for GitHub.com integrations.

* * *

<img src='/wp-content/uploads/gij-github-ent-64.png' width=48 height=46 style='margin-top:30px;' />

## GitHub Enterprise examples

**1. Lists all repositories (default)**

```java
/api/v3/user/repos
```

Gets the list of starred repositories for the authenticated user.

**2. Display all repositories from \<username\>**

```java
/api/v3/users/<username>/repos
```

Gets a list of public repositories for the specified user, **\<username\>**.

For example: `/api/v3/users/johnsmith/repos`

**3. Display starred repositories**

```java
/api/v3/user/starred
```

Gets the list of starred repositories for the authenticated user.

```java
/api/v3/users/<username>/starred
```

Gets the list of public/private starred repositories for the specified user, **\<username\>**.

For example: `/api/v3/users/johnsmith/starred`

**4. List all repositories for the specified organization**

```java
/api/v3/orgs/<org>/repos
```

Gets a list of repositories for the specified org, **\<org\>**. _BigBrassBand_

**For instance:**<br>
```/api/v3/orgs/BigBrassBand/repos```<br>
This will filter for repositories only within the org: _BigBrassBand_. This works for GitHub Enterprise integrations.

* * *

<img src='/wp-content/uploads/gij-gitlab-mobile.png' width=48 height=48 style='margin-top:30px;' />

## GitLab.com | GitLab CE/EE examples

**1. Lists all projects (default)**

```java
/api/v4/projects?membership=true
```

Gets a list of projects. This is the same as when no API path is specified.

**2. Display all projects from \<user\_id\>**

```java
/api/v4/users/<user_id>/projects
```

Gets a list of projects for the specified user, **\<user\_id\>**.

For example: `/api/v4/users/johnsmith/projects`

**3. Displays starred projects**

```java
/api/v4/projects?starred=true
```

Returns GitLab projects that have been starred by the connecting GitLab user.

**4. Limit to owned projects**

```java
/api/v4/projects?owned=true
```

The current user will be limited to the projects it's explicitly owned.

**5. List projects from within a Group**

```java
/api/v4/groups/5245789/projects<br>/api/v4/groups/BigBrassBand/projects
```

Returns the list of repositories within a GitLab Group (or GitLab Subgroup).

In the above examples, you can use the **Group id** or your **Group name** as query parameter.

**6. List projects from the specified sub-group**

```java
/api/v4/groups/5245789/projects?include_subgroups=true

/api/v4/groups/BigBrassBand/projects?include_subgroups=true
```

In the above examples, the <b><i>?include_subgroups=true</i></b> API extension will return a recursive list of repositories within a nested GitLab Group (or GitLab Subgroup) where the #, **5245789**, is the **Group id**; and **BigBrassBand** is the **Group name**.

For more information on GitLab custom API paths, see [**GitLab API**](https://docs.gitlab.com/ee/api/projects.html).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>GitLab version API support:</b><br>
        Gitlab v9.5 and above -- only API v4
        Gitlab v9.0 to v9.4.x -- API v3 and API v4
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Remember:</b><br>
        The GitLab.com API can see all the public projects. For GitLab.com, we recommend using JMESPath over the Custom API path when possible. For more information, see <a href='/git-integration-for-jira-cloud/working-with-jmespath-filters'>Working with JMESPath filters</a>.
    </div>
    </div>
</div>
<br>

* * *

<img src='/wp-content/uploads/gij-bitbucket-mobile.png' width=48 height=48 style='margin-top:30px;' />

## Bitbucket Cloud examples

**1. Lists all repositories for the specific user (default)**

```java
/!api/2.0/repositories/<username>
```

Displays a list of git repositories of the user with the specified username. This is the same as when no API path is specified.

**For example:**<br>
```/!api/2.0/repositories/wcoyote```

**2. Lists all repositories for the specified workspace ID**

```java
/!api/2.0/repositories/<workspaceID>
```

Displays a list of git repositories for the specified workspace ID.

**For example:**<br>
```/!api/2.0/repositories/acmegroup```

While Custom API Path and JMESPath filter are mutually exclusive, you can use one, the other, both or neither.

<br>
<br>
<div style='border-top: 1px solid #456; width: 40%; padding-bottom: 12px'></div>
<div style='font-size: 12px;'>
    <sup>1</sup> <i>Logo owned by <a href='https://gitlab.com/'>GitLab Inc</a> used under <a href='https://creativecommons.org/licenses/by-nc-sa/4.0/'>license</a>.
    <p>&nbsp;&nbsp;All product names, logos, and brands are property of their respective owners.<p><i>
</div>

