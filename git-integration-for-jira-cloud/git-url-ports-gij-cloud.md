---

title: Git URL Ports
description: Default port configurations for Git URL protocols
taxonomy:
    category: git-integration-for-jira-cloud

---

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

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
