# Webhook GitHub Organization support

<https://bigbrassband.atlassian.net/spaces/GITCLOUD/pages/171278791/Webhook+GitHub+Organization+support>

* * *

The Git Integration for Jira app supports GitHub Organization webhooks. Rather than creating a webhook for each repository manually, configure the webhook at the GitHub Organization level to automatically register webhook for each repository.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171278791/new-github-org-webhook-settings-page.png?version=2&modificationDate=1617192450844&cacheVersion=1&api=v2&width=680&height=607)

To configure GitHub organization webhook:

1.  Login to your GitHub account and go to your GitHub Organization.
    
2.  Go to ![(blue star)](/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Settings**.
    
3.  Under _Organization Settings_, go to **Webhooks**.
    
4.  Click **Add webhook**.
    
5.  Paste the webhook URL into the Payload URL field. (The webhook url is acquired from the Git Integration for Jira Cloud app ➜ Indexing triggers configuration page.)
    
6.  ![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/171278791/jira-cloud-webhook-url-loc(c1).png?version=1&modificationDate=1617192450865&cacheVersion=1&api=v2&width=652&height=434)
    
    Set the _**Content type**_ to **application/json**.
    
7.  Select/enable the "Let me select individual events" option:
    
    1.  Select **Branch or tag deletion**
        
    2.  Select **Branch or tag creation**
        
    3.  Select **Pull requests**
        
    4.  Select **Pushes**
        
8.  Click **Add webhook** to complete this setup.