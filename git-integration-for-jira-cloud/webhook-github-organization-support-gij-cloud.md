---

title: Webhook GitHub Organization support
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

The Git Integration for Jira app supports GitHub Organization webhooks. Rather than creating a webhook for each repository manually, configure the webhook at the GitHub Organization level to automatically register webhook for each repository.

![](/wp-content/uploads/gij-new-github-org-webhook-settings-page.png)

To configure GitHub organization webhook:

1.  Login to your GitHub account and go to your GitHub Organization.

2.  Go to **Settings**.

3.  Under _Organization Settings_, go to **Webhooks**.

4.  Click **Add webhook**.

5.  Paste the webhook URL into the Payload URL field. (The webhook url is acquired from the Git Integration for Jira Cloud app ➜ Indexing triggers configuration page.)

6.  ![](/wp-content/uploads/gij-gitcloud-indexing-trigger-webhook-url-level-1.png)

    Set the _**Content type**_ to **application/json**.

7.  Select/enable the "Let me select individual events" option:

    1.  Select **Branch or tag deletion**

    2.  Select **Branch or tag creation**

    3.  Select **Pull requests**

    4.  Select **Pushes**

8.  Click **Add webhook** to complete this setup.


