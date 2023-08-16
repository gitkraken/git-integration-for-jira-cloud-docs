---

title: GitLab.com | GitLab CE/EE JMESPath filter examples
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

![](/wp-content/uploads/gitlab-mobile-custom1.png)

An optional JMESPath filter can be configured when adding GitLab integration or repositories.

### 1\. Contains (include)

```java
[?contains(name, 'git') | contains(name, 'Slap') | contains(name, 'est')]
```

This is a filter based on text in the repository name. It will list all the repositories that contain the specified names. Do note that the declared string format is case-sensitive.

### 2\. Contains (exclude)

```java
[?(!contains(tag_list, 'largemedia'))]
```

```java
[?(!contains(name, 'firstword'))]
```

```java
[?(!contains(name, 'firstword')) | (!contains(name, 'secondword'))]
```

**1** – Blacklists project tag.

**2** – Lists repositories with names that either do not contain the word `'firstword'`.

**3** – Lists repositories with names that either do not contain the words `'firstword'` OR `'secondword'`.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The <code>!condition</code> must be wrapped in a parenthesis so it won’t invert the whole expression.
    </div>
    </div>
</div>

### 3\. Tags

```java
[?contains(tag_list, 'largemedia')]
```

Whitelists project tag.

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Note!</b><br>
        GitLab refers to <b><i>project tags</i></b> as tags in the API and in some places in the UI but the actual setting is called <b>Topics</b>.
    </div>
    </div>
</div>

### 4\. Starts with or ends with

```java
[?starts_with(name, 'git') | ends_with(name, 'test')]
```

Lists repositories with names that starts with `'git'` or ends with `'test'`.

### 5\. Exclude projects without repositories

```java
[?!empty_repo]
```

Lists only repositories from projects that have existing repositories.

&nbsp;
&nbsp;
* * *

1 _Logo owned by_ [_GitLab Inc_](https://gitlab.com/) _used under_ [_license_](https://creativecommons.org/licenses/by-nc-sa/4.0/)

