---

title: Allow list (whitelist) GIJ Cloud
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
        The information on this page is for GIJ Atlassian Cloud products only. These currently include Git Integration for Jira Cloud and Dev Info for Jira Cloud.<br>
        <span style='margin-top:10px;margin-bottom:0px'>Jira Server and Jira Data Center products are not hosted by GIJ or GitKraken.</span>
    </div>
    </div>
</div>

If using restrictive firewall or proxy server settings, you or your network admin will need to allow (allow list / whitelist) a specific IP  address to ensure GIJ Cloud applications work as expected. Specifically – if your team hosts a private git server (GitHub Enterprise, GitLab CE/EE, Microsoft TFS or Azure DevOps Server, Gerrit, Bitbucket Server, or a plain git server).

Alternatively, you can use our [Webhook indexing feature](#Webhooks-indexing-integration-for-private-networks) to avoid incoming API requests.

* * *
&nbsp;

## Allow list IP address for self-hosted git repositories

We support [Atlassian’s Data Residency](https://www.atlassian.com/software/data-residency) hosting model where customer’s Jira Cloud instances can be assigned to a specific geographic region. We currently support hosting specifically in the USA and EU. Customers not pinned to a specific geographic region are assigned to the Global region (which we host in the USA). All applications and data are hosted in Amazon Web Services (AWS). For more information - see our [Trust & Security](https://www.gitkraken.com/git-integration-for-jira/security-and-trust) page.

How to find out which geographic region your Git Integration for Jira Cloud application is hosted at - see [How do I find my app data](https://help.gitkraken.com/git-integration-for-jira-cloud/faq-support-gij-cloud/#where-can-i-find-my-app-information)

&nbsp;

### <img src='/wp-content/uploads/gij-global-icon.png' height=22 width=22 valign=middle />&nbsp; Global hosted customers (US-East-1)

For customers that are hosted on the Global (hosted in the Northern Virginia, USA AWS region US-East-1), set the allow list/whitelist for self-hosted git repositories:

| Server | IP address |
| :--- | :--- |
|App server 0 | **52.73.151.196** |
|App server 1 | **54.156.212.90** |

&nbsp;

### <img src='/wp-content/uploads/gij-eu-icon.png' height=24 width=24 valign=middle />&nbsp; European Union hosted customers (EU-West-1)

For customers that are hosted on the EU stack (hosted in Ireland, EU-West-1), set the allow list/whitelist for self-hosted git repositories:

| IP address |
| :--- |
| **18.202.139.125** |

&nbsp;

### <img src='/wp-content/uploads/gij-eu-icon.png' height=24 width=24 valign=middle />&nbsp; European Union hosted customers (EU-Central-1)

For customers that are hosted on the EU stack (hosted in Frankfurt, Germany, EU-Central-1), set the allow list/whitelist for self-hosted git repositories:

| IP address |
| :--- |
| **18.156.13.64** |

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

&nbsp;

### <img src='/wp-content/uploads/gij-us-icon.png' height=24 width=24 valign=middle />&nbsp; USA hosted customers (US-East-2)

For customers that are hosted on the US stack (hosted in the Ohio, USA AWS region), set the allow list/whitelist for self-hosted git repositories:

| Server | IP address |
| :--- | :--- |
|App Server 0 | **18.218.206.0** |
|App Server 1 | **18.218.116.230** |

&nbsp;

### Southeast Asia hosted customers (AP-Southeast-1)

For customers that are hosted on the Southeast Asian stack (Singapore), set the allow list/whitelist for self-hosted git repositories:

| IP address |
| :--- |
| **13.215.67.222** |


&nbsp;

### <img src='/wp-content/uploads/gij-au-icon.png' height=24 width=24 valign=middle />&nbsp; Australia hosted customers (AP-Southeast-2)

For customers that are hosted on the Australia stack, set the allow list/whitelist for self-hosted git repositories:

| Server | IP address |
| :--- | :--- |
| App Server 0 | **52.65.83.20** |
| App Server 1 | **13.237.217.178** |

&nbsp;

## Ports

To allow self-hosted git repositories to be indexed by GIJ Cloud applications - the following port(s) may be necessary to be open:

| Protocol | Port | Notes |
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
        Only open the ports required by your git server.<br><br>
        <span style='margin-top:10px;margin-bottom:0px;'><i><b>For example:</b> If your self-managed GitLab or GitHub Enterprise is using HTTPS, only open port 443.</i></span>
    </div>
    </div>
</div>

&nbsp;

## Allow list IP address for GitHub.com, Azure DevOps Repos, and GitLab.com

GitHub.com, Azure DevOps Repos, and GitLab.com have enterprise level features allowing for allow listing and require an additional set of IP addresses for allow listing:

### <img src='/wp-content/uploads/gij-global-icon.png' height=22 width=22 valign=middle />&nbsp; Global Region Hosted IP addresses (US-East-1)

54.196.201.91  
34.228.185.171  
34.224.218.252  
3.80.89.149  
34.224.101.92  
34.224.75.91  
52.23.171.14  
54.147.140.182  
54.235.62.22  
54.175.233.217  
18.208.171.222  
54.90.148.157  
54.242.227.154  
54.209.11.3  
3.88.216.216  
3.80.49.193  
54.87.49.117  
54.174.135.57  
52.54.150.111  

### <img src='/wp-content/uploads/gij-us-icon.png' height=22 width=22 valign=middle />&nbsp; USA Region Hosted IP addresses (US-East-2)

3.130.34.25  
18.218.122.134  
3.131.213.149  
3.143.100.15  
3.133.34.235  
18.190.109.9  
18.119.80.14  
3.14.197.223  
3.142.176.34  
3.130.151.4  

### <img src='/wp-content/uploads/gij-eu-icon.png' height=24 width=24 valign=middle />&nbsp; Central EU Region Hosted IP addresses (EU-Central-1)

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

### <img src='/wp-content/uploads/gij-eu-icon.png' height=24 width=24 valign=middle />&nbsp; Western EU Region Hosted IP addresses (EU-West-1)

34.247.19.97

54.72.243.188

52.210.99.19

54.76.253.102

### Southeast Asia - Singapore Region Hosted IP addresses

18.140.19.30

18.143.232.103

54.151.179.195

18.138.219.190

### <img src='/wp-content/uploads/gij-au-icon.png' height=24 width=24 valign=middle />&nbsp; Australia Region Hosted IP addresses

54.206.176.144  
3.105.72.140  
52.64.118.63  
13.238.136.180

If you use these IP addresses for allow listing - we ask that you contact us at [GIJ Cloud Support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/) so we can notify you if these IP addresses are ever changed.

&nbsp;

## Reachable network address

To allow self-hosted git servers, the git server must be reachable with a public address/IP by the indexing service.

If your git server is simply behind a firewall, whitelist the IP address of the indexing service (see [Whitelist IP address](#allow-list-ip-address-for-githubcom-azure-devops-repos-and-gitlabcom)).

If your git server is only reachable on a private intranet or through a virtual private network (VPN), the Git Integration for Jira indexing service will not be able to reach your git server, even if you whitelist our IP. See [Webhooks indexing integration](#webhooks-indexing-integration-for-private-networks) section below.

**Examples:**

| Reachable? | Example |
| :--- | :--- |
| ![](/wp-content/uploads/gij-check.png) | [https://git.corp.com/repository/widget-production.git](https://git.corp.com/repository/widget-production.git) -- a hosted git repository added directly |
|![](/wp-content/uploads/gij-check.png) | [https://git.corp.com](https://git.corp.com) -- a git server running GitHub/Gitlab/etc |
| ![](/wp-content/uploads/gij-check.png) | [https://gitlab.corp.com:8088](https://gitlab.corp.com:8088) -- a server running on a non-standard port |
| ![](/wp-content/uploads/gij-check.png) | [http://52.123.19.12](http://52.123.19.12) -- server without DNS, just an IP |
| ![](/wp-content/uploads/gij-error.png) | 192.168.1.92 |
| ![](/wp-content/uploads/gij-error.png) | git.corp (private network) |

&nbsp;

## Webhooks indexing integration for private networks

Webhook indexing integration supports indexing of commits and pull requests using webhook metadata. This allows the git server to remain in a private network while sending sufficient git metadata for association with Jira issues. There are some feature limitations -- such as viewing source code (Jira issue ➜ **Git Commits** tab ➜ **View full commit**). However, functions such as branches and pull/merge requests creation inside Jira are not available.

For more information on this feature, see the following articles:

*   [Classic webhook indexing explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud)

*   [Webhook indexing integration](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud)

    *   [GitHub](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud)

    *   [GitLab](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud)

    *   [Microsoft](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud)

## GIJ Cloud apps

[Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview)

[Dev Info for Jira Cloud](https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview)

## GIJ Cloud Support

If you need additional support connecting your self-hosted git servers or repositories - please contact [GIJ Cloud Support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/).

