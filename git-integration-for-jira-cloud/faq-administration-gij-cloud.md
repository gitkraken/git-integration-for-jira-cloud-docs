---

title: Administration FAQ
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

This page contains solutions targeted for administrators.

Use the FAQ below to find answers to common questions. Feel free to contact our support team (support@bigbrassband.com) if you don’t see what you’re looking for.


* * *

## Does Jira+GitHub integration support multiple Jira projects (many) to multiple git repositories (many)?  If it does not, how about many-to-one or one-to-many?

Yes - it does support repositories supporting many projects. That said, the associations are made by the developers when they commit code to a specific issue key (which is part of a project). The permission that allows a user to see these commits in a Jira project is whether they have the "View Development Tools" permission for that project (that's a Jira setting).

