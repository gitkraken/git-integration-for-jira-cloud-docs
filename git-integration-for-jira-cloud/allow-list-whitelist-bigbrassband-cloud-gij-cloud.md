---

title: Allow list (whitelist) BigBrassBand Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        The information on this page is for BigBrassBand Atlassian Cloud products only. These currently include Git Integration for Jira Cloud and Dev Info for Jira Cloud.
        <div class='nextpara'><b>Jira Server and Jira Data Center products are not hosted by BigBrassBand.</b><div>
    </div>
    </div>
</div>
<br>

If using restrictive firewall or proxy server settings, you or your network admin will need to allow (allow list / whitelist) a specific IP address to ensure BigBrassBand Cloud applications work as expected. Specifically – if your team hosts a private git server (GitHub Enterprise, GitLab CE/EE, Microsoft TFS or Azure DevOps Server, Gerrit, Bitbucket Server, or a plain git server).

Alternatively, you can use our [Webhook indexing feature](#Webhooks-indexing-integration-for-private-networks) to avoid incoming API requests.

**What's on this page:**
- [Allow list IP address for self-hosted git repositories](#allow-list-ip-address-for-self-hosted-git-repositories)
  - [<img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f30e.png' height=22 width=22 valign=middle />&nbsp; Global hosted customers](#-global-hosted-customers)
  - [<img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1ea-1f1fa.png' height=24 width=24 valign=middle />&nbsp; European Union hosted customers](#-european-union-hosted-customers)
  - [<img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1fa-1f1f8.png' height=24 width=24 valign=middle />&nbsp; USA hosted customers](#-usa-hosted-customers)
  - [<img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1e6-1f1fa.png' height=24 width=24 valign=middle />&nbsp; Australia hosted customers](#-australia-hosted-customers)
- [Ports](#ports)
- [Allow list IP address for GitHub.com, Azure DevOps Repos, and GitLab.com:](#allow-list-ip-address-for-githubcom-azure-devops-repos-and-gitlabcom)
  - [<img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f30e.png' height=22 width=22 valign=middle />&nbsp; Global Region Hosted IP addresses](#-global-region-hosted-ip-addresses)
  - [<img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1fa-1f1f8.png' height=22 width=22 valign=middle />&nbsp; USA Region Hosted IP addresses](#-usa-region-hosted-ip-addresses)
  - [<img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1ea-1f1fa.png' height=24 width=24 valign=middle />&nbsp; EU Region Hosted IP addresses](#-eu-region-hosted-ip-addresses)
  - [<img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1e6-1f1fa.png' height=24 width=24 valign=middle />&nbsp; Australia Region Hosted IP addresses](#-australia-region-hosted-ip-addresses)
- [Reachable network address](#reachable-network-address)
- [Webhooks indexing integration for private networks](#webhooks-indexing-integration-for-private-networks)
- [BigBrassBand Cloud apps](#bigbrassband-cloud-apps)
- [Support](#support)

* * *

## Allow list IP address for self-hosted git repositories

We support [Atlassian’s Data Residency](https://www.atlassian.com/software/data-residency) hosting model where customer’s Jira Cloud instances can be assigned to a specific geographic region. We currently support hosting specifically in the USA and EU. Customers not pinned to a specific geographic region are assigned to the Global region (which we host in the USA). All applications and data are hosted in Amazon Web Services (AWS). For more information - see our [Trust & Security](https://bigbrassband.com/security-and-trust.html) page.

How to find out which geographic region your Git Integration for Jira Cloud application is hosted at - see…

<br>

### <img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f30e.png' height=22 width=22 valign=middle />&nbsp; Global hosted customers

For customers that are hosted on the Global (hosted in the Northern Virginia, USA AWS region), set the allow list/whitelist for self-hosted git repositories:

| **IP address** |
| --- |
| `52.73.151.196` |

<br>

### <img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1ea-1f1fa.png' height=24 width=24 valign=middle />&nbsp; European Union hosted customers

For customers that are hosted on the EU stack (hosted in Frankfurt, Germany), set the allow list/whitelist for self-hosted git repositories:

| **IP address** |
| --- |
| `18.156.13.64` |

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <a href='https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?tab=overview&hosting=cloud'>Dev Info for Jira Cloud</a> does not have EU hosting support.
    </div>
    </div>
</div>
<br>

### <img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1fa-1f1f8.png' height=24 width=24 valign=middle />&nbsp; USA hosted customers

For customers that are hosted on the US stack (hosted in the Ohio, USA AWS region), set the allow list/whitelist for self-hosted git repositories:

| **IP address** |
| --- |
| `18.218.206.0` |

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <a href='https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?tab=overview&hosting=cloud'>Dev Info for Jira Cloud</a> does not have EU hosting support.
    </div>
    </div>
</div>
<br>

### <img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1e6-1f1fa.png' height=24 width=24 valign=middle />&nbsp; Australia hosted customers

For customers that are hosted on the Australia stack, set the allow list/whitelist for self-hosted git repositories:

| **IP address** |
| --- |
| `52.65.83.20` |

## Ports

To allow self-hosted git repositories to be indexed by BigBrassBand Cloud applications - the following port(s) may be necessary to be open:

| **Protocol** | **Port** | **Notes** |
| :--- | :--- | :--- |
| HTTPS | 443 | Common case |
| HTTP | 80  | Very uncommon |
| SSH | 22  | Only if using SSH keys for authentication to repositories |

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Only open the ports required by your git server.
        <div class='nextpara'>
            <i><b>For example:</b> If your self-managed GitLab or GitHub Enterprise is using HTTPS, only open port 443.</i>
        </div>
    </div>
    </div>
</div>
<br>

## Allow list IP address for GitHub.com, Azure DevOps Repos, and GitLab.com:

GitHub.com, Azure DevOps Repos, and GitLab.com have enterprise level features allowing for allow listing and require an additional set of IP addresses for allow listing:

### <img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f30e.png' height=22 width=22 valign=middle />&nbsp; Global Region Hosted IP addresses

```powershell
54.175.75.157
54.198.195.73
54.226.216.3
3.83.233.216
100.24.7.48
18.208.222.41
54.221.46.106
54.172.45.1
18.234.60.156
54.157.63.246
34.224.91.167
3.89.224.7
54.144.124.44
174.129.126.205
54.167.77.230
54.91.24.123
23.22.153.253
54.209.186.87
54.157.14.229
52.54.150.111
```

### <img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1fa-1f1f8.png' height=22 width=22 valign=middle />&nbsp; USA Region Hosted IP addresses

```powershell
3.130.34.25
18.218.122.134
3.131.213.149
3.143.100.15
18.218.206.0
3.133.34.235
18.190.109.9
18.119.80.14
3.14.197.223
3.142.176.34
3.130.151.4
```

### <img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1ea-1f1fa.png' height=24 width=24 valign=middle />&nbsp; EU Region Hosted IP addresses

```powershell
18.156.13.64
3.123.136.62
18.156.8.182
18.198.71.138
3.69.186.247
3.70.82.79
18.159.165.4
3.125.231.184
3.68.13.136
3.67.63.5
52.58.106.61
```

### <img src='https://bigbrassband.atlassian.net/wiki/s/-1385669512/6452/79ea784589356386e2ff787614d18662b42105a6/_/images/icons/emoticons/72/1f1e6-1f1fa.png' height=24 width=24 valign=middle />&nbsp; Australia Region Hosted IP addresses

```powershell
13.238.136.180
3.105.72.140
54.206.176.144
52.64.118.63
```

If you use these IP addresses for allow listing - we ask that you contact us at [support@bigbrassband.com](mailto:support@bigbrassband.com) so we can notify you if these IP addresses are ever changed.

## Reachable network address

To allow self-hosted git servers, the git server must be reachable with a public address/IP by the indexing service.

If your git server is simply behind a firewall, whitelist the IP address of the indexing service (see [Whitelist IP address](#allow-list-ip-address-for-githubcom-azure-devops-repos-and-gitlabcom)).

If your git server is only reachable on a private intranet or through a virtual private network (VPN), the Git Integration for Jira indexing service will not be able to reach your git server, even if you whitelist our IP. See [Webhooks indexing integration](#webhooks-indexing-integration-for-private-networks) section below.

**Examples:**

![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) [https://git.corp.com/repository/widget-production.git](https://git.corp.com/repository/widget-production.git) - a hosted git repository added directly

![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) [https://git.corp.com](https://git.corp.com) - a git server running GitHub/Gitlab/etc

![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) [https://gitlab.corp.com:8088](https://gitlab.corp.com:8088) - a server running on a non-standard port

![(tick)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/check.png) [http://52.123.19.12](http://52.123.19.12) - server without DNS, just an IP

![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) 192.168.1.92

![(error)](https://bigbrassband.atlassian.net/wiki/s/-1639011364/6452/8b4898d3c114827e64ec143b4fa79bb76a6cfa5b/_/images/icons/emoticons/error.png) git.corp (private network)

## Webhooks indexing integration for private networks

Webhook indexing integration supports indexing of commits and pull requests using webhook metadata. This allows the git server to remain in a private network while sending sufficient git metadata for association with Jira issues. There are some feature limitations -- such as viewing source code (Jira issue ➜ **Git Commits** tab ➜ **View full commit**). However, functions such as branches and pull/merge requests creation inside Jira are not available.

For more information on this feature, see the following articles:

*   [Classic webhook indexing explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud/)

*   [Webhook indexing integration](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud/)

    *   [GitHub](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud/)

    *   [GitLab](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud/)

    *   [Microsoft](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud/)

## BigBrassBand Cloud apps

[Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview)

[Dev Info for Jira Cloud](https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview)

## Support

If you need additional support connecting your self-hosted git servers or repositories - please contact [BigBrassBand Support](https://bigbrassband.atlassian.net/servicedesk/customer/portals).

