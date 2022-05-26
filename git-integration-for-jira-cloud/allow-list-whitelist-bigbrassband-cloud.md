---

title: Allow list (whitelist) BigBrassBand Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
The information on this page is for BigBrassBand Atlassian Cloud products only. These currently include Git Integration for Jira Cloud and Dev Info for Jira Cloud.

_**Jira Server and Jira Data Center products are not hosted by BigBrassBand.**_


If using restrictive firewall or proxy server settings, you or your network admin will need to allow (allow list / whitelist) a specific IP address to ensure BigBrassBand Cloud applications work as expected. Specifically – if your team hosts a private git server (GitHub Enterprise, GitLab CE/EE, Microsoft TFS or Azure DevOps Server, Gerrit, Bitbucket Server, or a plain git server).

Alternatively, you can use our [Webhook indexing feature](#Webhooks-indexing-integration-for-private-networks) to avoid incoming API requests.

## Allow list IP address for self-hosted git repositories

We support [Atlassian’s Data Residency](https://www.atlassian.com/software/data-residency) hosting model where customer’s Jira Cloud instances can be assigned to a specific geographic region. We currently support hosting specifically in the USA and EU. Customers not pinned to a specific geographic region are assigned to the Global region (which we host in the USA). All applications and data are hosted in Amazon Web Services (AWS). For more information - see our [Trust & Security](https://bigbrassband.com/security-and-trust.html) page.

How to find out which geographic region your Git Integration for Jira Cloud application is hosted at - see…

#### ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) Global hosted customers

For customers that are hosted on the Global (hosted in the Northern Virginia, USA AWS region), set the allow list/whitelist for self-hosted git repositories:

|     |
| --- |
| **IP address** |
| `52.73.151.196` |

#### ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) European Union hosted customers

For customers that are hosted on the EU stack (hosted in Frankfurt, Germany), set the allow list/whitelist for self-hosted git repositories:

|     |
| --- |
| **IP address** |
| `18.156.13.64` |

[Dev Info for Jira Cloud](https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?tab=overview&hosting=cloud) does not have EU hosting support.

#### ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) USA hosted customers

For customers that are hosted on the US stack (hosted in the Ohio, USA AWS region), set the allow list/whitelist for self-hosted git repositories:

|     |
| --- |
| **IP address** |
| `18.218.206.0` |

[Dev Info for Jira Cloud](https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?tab=overview&hosting=cloud) does not have USA hosting support.

## Ports

To allow self-hosted git repositories to be indexed by BigBrassBand Cloud applications - the following port(s) may be necessary to be open:

|     |     |     |
| --- | --- | --- |
| **Protocol** | **Port** | **Notes** |
| HTTPS | 443 | Common case |
| HTTP | 80  | Very uncommon |
| SSH | 22  | Only if using SSH keys for authentication to repositories |

Only open the ports required by your git server.

_**For example:** If your self-managed GitLab or GitHub Enterprise is using HTTPS, only open port 443._

## Allow list IP address for GitHub.com, Azure DevOps Repos, and GitLab.com:

GitHub.com, Azure DevOps Repos, and GitLab.com have enterprise level features allowing for allow listing and require an additional set of IP addresses for allow listing:

|     |
| --- |
| ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **Global Region Hosted IP addresses** |
| 54.175.75.157 |
| 54.198.195.73 |
| 54.226.216.3 |
| 3.83.233.216 |
| 100.24.7.48 |
| 18.208.222.41 |
| 54.221.46.106 |
| 54.172.45.1 |
| 18.234.60.156 |
| 54.157.63.246 |
| 34.224.91.167 |
| 3.89.224.7 |
| 54.144.124.44 |
| 174.129.126.205 |
| 54.167.77.230 |
| 54.91.24.123 |
| 23.22.153.253 |
| 54.209.186.87 |
| 54.157.14.229 |
| 52.54.150.111 |

|     |
| --- |
| #### ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **USA Region Hosted IP addresses** |
| 3.130.34.25 |
| 18.218.122.134 |
| 3.131.213.149 |
| 3.143.100.15 |
| 18.218.206.0 |
| 3.133.34.235 |
| 18.190.109.9 |
| 18.119.80.14 |
| 3.14.197.223 |
| 3.142.176.34 |
| 3.130.151.4 |

|     |
| --- |
| #### ![(blue star)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/star_blue.png) **EU Region Hosted IP addresses** |
| 18.156.13.64 |
| 3.123.136.62 |
| 18.156.8.182 |
| 18.198.71.138 |
| 3.69.186.247 |
| 3.70.82.79 |
| 18.159.165.4 |
| 3.125.231.184 |
| 3.68.13.136 |
| 3.67.63.5 |
| 52.58.106.61 |

If you use these IP addresses for allow listing - we ask that you contact us at [support@bigbrassband.com](mailto:support@bigbrassband.com) so we can notify you if these IP addresses are ever changed.

## Reachable network address

To allow self-hosted git servers, the git server must be reachable with a public address/IP by the indexing service.

If your git server is simply behind a firewall, whitelist the IP address of the indexing service (see **Whitelist IP address**).

If your git server is only reachable on a private intranet or through a virtual private network (VPN), the Git Integration for Jira indexing service will not be able to reach your git server, even if you whitelist our IP. See [Webhooks indexing integration](#Webhooks-indexing-integration-for-private-networks) section below.

|     |
| --- |
| **Examples:** |
| ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) [https://git.corp.com/repository/widget-production.git](https://git.corp.com/repository/widget-production.git) - a hosted git repository added directly |
| ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) [https://git.corp.com](https://git.corp.com) - a git server running GitHub/Gitlab/etc |
| ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) [https://gitlab.corp.com:8088](https://gitlab.corp.com:8088) - a server running on a non-standard port |
| ![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) [http://52.123.19.12](http://52.123.19.12) - server without DNS, just an IP |
| ![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) 192.168.1.92 |
| ![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) git.corp (private network) |

## Webhooks indexing integration for private networks

Webhook indexing integration supports indexing of commits and pull requests using webhook metadata. This allows the git server to remain in a private network while sending sufficient git metadata for association with Jira issues. There are some feature limitations -- such as viewing source code (Jira issue ➜ **Git Commits** tab ➜ **View full commit**) and branches and pull/merge requests creation inside Jira are not available.

For more information on this feature, see the following articles:

*   [Classic webhook indexing explainer](/wiki/spaces/GITCLOUD/pages/183369754/Classic+Indexing+Explainer)

*   [Webhook indexing explainer](/wiki/spaces/GITCLOUD/pages/1422819484/Webhook+Indexing+Explainer)

*   [Webhook indexing integration](/wiki/spaces/GITCLOUD/pages/1508081882/Webhook+indexing+integration)

    *   [GitHub](/wiki/spaces/GITCLOUD/pages/1494646787/GitHub+webhook+indexing+integration)

    *   [GitLab](/wiki/spaces/GITCLOUD/pages/1503494176/GitLab+webhook+indexing+integration)

    *   [Microsoft](/wiki/spaces/GITCLOUD/pages/1509032469/Microsoft+webhook+indexing+integration)


## BigBrassBand Cloud apps

[Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview)

[Dev Info for Jira Cloud](https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview)

## Support

If you need additional support connecting your self-hosted git servers or repositories - please contact [BigBrassBand Support](https://bigbrassband.atlassian.net/servicedesk/customer/portals).
