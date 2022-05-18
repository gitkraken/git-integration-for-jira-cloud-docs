---

title: Admin
description:
taxonomy:
    category: git-integration-for-jira-cloud

---


This page contains solutions targeted for administrators.

Use the FAQ below to find answers to common questions.  Feel free to contact our support team ([support@bigbrassband.com](mailto:support@bigbrassband.com)) if you don't see what you're looking for.

[Does the Git Integration for Jira Cloud app have API commands that allow addition/removal of a Git project?](/wiki/pages/resumedraft.action?draftId=87130238#Admin-haveapicmds)

[After upgrading Jira from _4.1.1_ to _5.2.9_, I get some errors _"Folder ... FORNEOnlineSolver git doesn't exist"_.  Where can I set the path correctly?  Is there any properties file?](/wiki/pages/resumedraft.action?draftId=87130238#Admin-setpathpropfile)

[Does Jira+GitHub integration support multiple Jira projects (many) to multiple git repositories (many)?  If it does not, how about many-to-one or one-to-many?](/wiki/pages/resumedraft.action?draftId=87130238#Admin-multjiraprojsupport)



* * *



## **Does the Git Integration for Jira Cloud app have API commands that allow addition/removal of a Git project?**

Yes.  As of **v2.8.3** of the Git add-on, the **REST API** for add, update, and delete repository is implemented.  The documentation for this feature is available at **[Git add-on: Hook and API Reference - Repository REST API »](https://bigbrassband.com/api/jira-git-rest-api-repository.html)**.



## **After upgrading Jira from _4.1.1_ to _5.2.9_, I get some errors _"Folder ... FORNEOnlineSolver git doesn't exist"_.  Where can I set the path correctly?  Is there any properties file?**

Please visit add-on config and check Git Repositories tab.  Also, upgrade of Jira may lead to changing of user account used to run the service, which in turn, may result in lack of permissions.



## **Does Jira+GitHub integration support multiple Jira projects (many) to multiple git repositories (many)?  If it does not, how about many-to-one or one-to-many?**

Yes — it does support repositories supporting many projects.  That said, the associations are made by the developers when they commit code to a specific issue key (which is part of a project).  The permission that allows a user to see these commits in a Jira project is whether they have the "**View Development Tools**" permission for that project (that's a Jira setting).