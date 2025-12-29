---
title: Working with Custom API Path
description: Configure Custom API Path to filter and retrieve specific repositories from GitHub, GitLab, and Bitbucket integrations in Git Integration for Jira Cloud.
taxonomy:
    category: git-integration-for-jira-cloud
---

The Custom API Path is a relative path that starts with `/`. Use it to filter which repositories Git Integration for Jira retrieves from your git service. The maximum length is **2,000 characters**.

Git Integration for Jira calls the Custom API Path during:
- Initial integration setup
- Settings changes
- Scheduled reindexing
- Manual reindexing

**On this page:**
- [Access Custom API Path settings](#access-custom-api-path-settings)
- [GitHub.com examples](#githubcom-examples)
- [GitHub Enterprise examples](#github-enterprise-examples)
- [GitLab.com and GitLab CE/EE examples](#gitlabcom-and-gitlab-ceee-examples)
- [Bitbucket Cloud examples](#bitbucket-cloud-examples)

&nbsp;
* * *
&nbsp;

## Access Custom API Path Settings

### During Integration Setup

1. Go to **Manage Git repositories** ➜ **Add integration** ➜ select a supported git service.
2. On the **Connect** screen, expand **Advanced**.
3. Enter your path in the **Custom API Path** field.

![](/wp-content/uploads/gij-gitcloud-autoconnect-github-custom-api-path-2025.png)

### From Integration Settings

1. Go to **Manage Git repositories**.
2. Click <img src='/wp-content/uploads/actions-icon.png' /> **Actions** ➜ **Edit integration settings** (or **Edit repository settings**).
3. Scroll to **Integration settings** ➜ **Custom API Path**.

![](/wp-content/uploads/gij-gitcloud-actions-edit-integration-settings-cAPI-path-2025.png)

&nbsp;
* * *
&nbsp;

<img src='/wp-content/uploads/github-mobile-dark.png' width=48 height=48 style='margin-top:30px;' />

## GitHub.com Examples

### List All Repositories (Default)

```java
/user/repos
```

Returns all repositories. This is the default behavior when no API path is specified.

### List Repositories for a Specific User

```java
/users/<username>/repos
```

Returns public repositories for the specified user.

**Example:** `/users/johnsmith/repos`

### List Starred Repositories

```java
/user/starred
```

Returns repositories the authenticated user has starred.

```java
/users/<username>/starred
```

Returns starred repositories (public and private) for the specified user.

**Example:** `/users/johnsmith/starred`

### List Repositories for an Organization

```java
/orgs/<org>/repos
```

Returns repositories for the specified organization.

**Example:** `/orgs/BigBrassBand/repos` returns only repositories within the BigBrassBand organization.

&nbsp;
* * *
&nbsp;

<img src='/wp-content/uploads/gij-github-ent-64.png' width=48 height=46 style='margin-top:30px;' />

## GitHub Enterprise Examples

### List All Repositories (Default)

```java
/api/v3/user/repos
```

Returns repositories for the authenticated user.

### List Repositories for a Specific User

```java
/api/v3/users/<username>/repos
```

Returns public repositories for the specified user.

**Example:** `/api/v3/users/johnsmith/repos`

### List Starred Repositories

```java
/api/v3/user/starred
```

Returns repositories the authenticated user has starred.

```java
/api/v3/users/<username>/starred
```

Returns starred repositories (public and private) for the specified user.

**Example:** `/api/v3/users/johnsmith/starred`

### List Repositories for an Organization

```java
/api/v3/orgs/<org>/repos
```

Returns repositories for the specified organization.

**Example:** `/api/v3/orgs/BigBrassBand/repos`

&nbsp;
* * *
&nbsp;

<img src='/wp-content/uploads/gij-gitlab-mobile.png' width=48 height=48 style='margin-top:30px;' />

## GitLab.com and GitLab CE/EE Examples

### List All Projects (Default)

```java
/api/v4/projects?membership=true
```

Returns all projects. This is the default behavior when no API path is specified.

### List Projects for a Specific User

```java
/api/v4/users/<user_id>/projects
```

Returns projects for the specified user.

**Example:** `/api/v4/users/johnsmith/projects`

### List Starred Projects

```java
/api/v4/projects?starred=true
```

Returns projects the authenticated user has starred.

### List Owned Projects Only

```java
/api/v4/projects?owned=true
```

Returns only projects the authenticated user explicitly owns.

### List Projects from a Group

```java
/api/v4/groups/<group_id>/projects
```

Returns projects within a GitLab Group or Subgroup.

**Examples:**
- `/api/v4/groups/5245789/projects` (using group ID)
- `/api/v4/groups/BigBrassBand/projects` (using group name)

### List Projects Including Subgroups

```java
/api/v4/groups/<group_id>/projects?include_subgroups=true
```

Returns projects within a group and all its nested subgroups.

**Examples:**
- `/api/v4/groups/5245789/projects?include_subgroups=true`
- `/api/v4/groups/BigBrassBand/projects?include_subgroups=true`

For more information, see the [GitLab API documentation](https://docs.gitlab.com/ee/api/projects.html).

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>GitLab API version support:</b><br>
        <ul style='margin-bottom:0px'>
            <li>GitLab v9.5 and later: API v4 only</li>
            <li>GitLab v9.0 to v9.4.x: API v3 and API v4</li>
        </ul>
    </div>
    </div>
</div>

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The GitLab.com API returns all public projects. For GitLab.com, use JMESPath filters instead of Custom API Path when possible. See <a href='/git-integration-for-jira-cloud/working-with-jmespath-filters'>Working with JMESPath filters</a>.
    </div>
    </div>
</div>

&nbsp;
* * *
&nbsp;

<img src='/wp-content/uploads/gij-bitbucket-mobile.png' width=48 height=48 style='margin-top:30px;' />

## Bitbucket Cloud Examples

### List Repositories for a Specific User (Default)

```java
/!api/2.0/repositories/<username>
```

Returns repositories for the specified user. This is the default behavior when no API path is specified.

**Example:** `/!api/2.0/repositories/wcoyote`

### List Repositories for a Workspace

```java
/!api/2.0/repositories/<workspaceID>
```

Returns repositories for the specified workspace ID.

**Example:** `/!api/2.0/repositories/acmegroup`

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Custom API Path and JMESPath filters are not mutually exclusive. You can use one, both, or neither.
    </div>
    </div>
</div>

&nbsp;

<div style='border-top: 1px solid #456; width: 40%; padding-bottom: 12px'></div>
<div style='font-size: 12px;'>
    <sup>1</sup> <i>Logo owned by <a href='https://gitlab.com/'>GitLab Inc</a> used under <a href='https://creativecommons.org/licenses/by-nc-sa/4.0/'>license</a>.
    <p>&nbsp;&nbsp;All product names, logos, and brands are property of their respective owners.<p><i>
</div>

<kbd>Last updated: December 2025</kbd>
