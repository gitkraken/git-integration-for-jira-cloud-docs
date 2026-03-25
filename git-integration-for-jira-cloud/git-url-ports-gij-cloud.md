---
title: "Git URL Ports"
description: "Default port configurations for Git URL protocols"
product: "Git Integration for Jira Cloud"
feature: "Git URL Ports"
content_type: "install"
audience: "admin"
plan_required: "all"
deployment: "Jira Cloud"
git_host_support: []
role_required: "Jira Administrator"
version_required: "all"
status: "GA"
last_verified: "2026-03"
tags: ["Git Integration for Jira Cloud", "Jira Cloud", "install", "admin"]
taxonomy:
    category: git-integration-for-jira-cloud
---
<kbd>Last updated: March 2026</kbd>

If your Git servers are running through a firewall, configure the firewall to allow access using the URL schemes for git repositories. For authentication issues, make sure to check the correct port for the connection.

Below are the default ports for common git URL protocols:

| **Protocol** | **Default Port** |
| --- | --- |
| ssh:// | port 22 |
| git:// | port 9418 |
| http:// | port 80 |
| https:// | port 443 |

&nbsp;

## Testing Git Connection

Test the git connection and repository URL by doing the following:

1.  Install the git client (or run `sudo apt-get install git`).

2.  Place your SSH key into `~/.ssh`.

3.  Clone the repository (or run `git clone <your_repository_url>`).

Git Integration for Jira will run successfully if the above connection test completes without errors.

For detailed information on whitelisting your Git server, see [Allow list (whitelist) BigBrassBand Cloud](/git-integration-for-jira-cloud/allow-list-whitelist-bigbrassband-cloud-gij-cloud).

<p>&nbsp;</p>
