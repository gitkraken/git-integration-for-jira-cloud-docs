---
title: Allow list (whitelist) GIJ Cloud
description: Configure firewall settings to allow Git Integration for Jira Cloud to access your self-hosted git repositories.
taxonomy:
    category: git-integration-for-jira-cloud
---

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        This page applies to GIJ Atlassian Cloud products only, including Git Integration for Jira Cloud and Dev Info for Jira Cloud.<br>
        <span style='margin-top:10px;margin-bottom:0px'>GitKraken does not host Jira Server or Jira Data Center products.</span>
    </div>
    </div>
</div>

If your firewall or proxy server restricts outbound connections, add the IP addresses listed below to your allow list. This configuration enables GIJ Cloud applications to connect to your private git server (GitHub Enterprise, GitLab CE/EE, Microsoft TFS, Azure DevOps Server, Gerrit, Bitbucket Server, or a plain git server).

Alternatively, use the [Webhook indexing feature](#webhooks-indexing-integration-for-private-networks) to avoid incoming API requests.

**On this page:**
- [Configure allow list for self-hosted git repositories](#configure-allow-list-for-self-hosted-git-repositories)
- [Open required ports](#open-required-ports)
- [Configure allow list for GitHub.com, Azure DevOps Repos, and GitLab.com](#configure-allow-list-for-githubcom-azure-devops-repos-and-gitlabcom)
- [Verify network reachability](#verify-network-reachability)
- [Use webhook indexing for private networks](#webhooks-indexing-integration-for-private-networks)

&nbsp;
* * *
&nbsp;

## Configure Allow List for Self-Hosted Git Repositories

GIJ Cloud supports [Atlassian's Data Residency](https://www.atlassian.com/software/data-residency) hosting model. Jira Cloud instances can be assigned to specific geographic regions. GIJ Cloud currently supports hosting in the USA and EU. Customers not pinned to a specific region are assigned to the Global region (hosted in the USA). All applications and data are hosted in Amazon Web Services (AWS). For more information, see the [Trust & Security](https://www.gitkraken.com/git-integration-for-jira/security-and-trust) page.

To find your geographic region, see [How do I find my app data](https://help.gitkraken.com/git-integration-for-jira-cloud/faq-support-gij-cloud/#where-can-i-find-my-app-information).

&nbsp;

### <img src='/wp-content/uploads/gij-global-icon.png' height=22 width=22 valign=middle />&nbsp; Global Hosted Customers (US-East-1)

Add these IP addresses for customers hosted in the Global region (Northern Virginia, USA AWS region US-East-1):

| Server | IP address |
| :--- | :--- |
| App server 0 | **52.73.151.196** |
| App server 1 | **54.156.212.90** |

&nbsp;

### <img src='/wp-content/uploads/gij-eu-icon.png' height=24 width=24 valign=middle />&nbsp; European Union Hosted Customers (EU-West-1)

Add this IP address for customers hosted in the EU stack (Ireland, EU-West-1):

| IP address |
| :--- |
| **18.202.139.125** |

&nbsp;

### <img src='/wp-content/uploads/gij-eu-icon.png' height=24 width=24 valign=middle />&nbsp; European Union Hosted Customers (EU-Central-1)

Add this IP address for customers hosted in the EU stack (Frankfurt, Germany, EU-Central-1):

| IP address |
| :--- |
| **18.156.13.64** |

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <a href='https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?tab=overview&hosting=cloud'>Dev Info for Jira Cloud</a> does not support EU hosting.
    </div>
    </div>
</div>

&nbsp;

### <img src='/wp-content/uploads/gij-us-icon.png' height=24 width=24 valign=middle />&nbsp; USA Hosted Customers (US-East-2)

Add these IP addresses for customers hosted in the US stack (Ohio, USA AWS region):

| Server | IP address |
| :--- | :--- |
| App Server 0 | **18.218.206.0** |
| App Server 1 | **18.218.116.230** |

&nbsp;

### Southeast Asia Hosted Customers (AP-Southeast-1)

Add this IP address for customers hosted in the Southeast Asian stack (Singapore):

| IP address |
| :--- |
| **13.215.67.222** |

&nbsp;

### <img src='/wp-content/uploads/gij-au-icon.png' height=24 width=24 valign=middle />&nbsp; Australia Hosted Customers (AP-Southeast-2)

Add these IP addresses for customers hosted in the Australia stack:

| Server | IP address |
| :--- | :--- |
| App Server 0 | **52.65.83.20** |
| App Server 1 | **13.237.217.178** |

&nbsp;

## Open Required Ports

Open the following ports to allow GIJ Cloud applications to index your self-hosted git repositories:

| Protocol | Port | Notes |
| :--- | :--- | :--- |
| HTTPS | 443 | Most common configuration |
| HTTP | 80 | Rarely used |
| SSH | 22 | Required only when using SSH keys for authentication |

<div class="bbb-callout bbb--note">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        Open only the ports your git server requires.<br><br>
        <span style='margin-top:10px;margin-bottom:0px;'><i><b>Example:</b> If your self-managed GitLab or GitHub Enterprise uses HTTPS, open only port 443.</i></span>
    </div>
    </div>
</div>

&nbsp;

## Configure Allow List for GitHub.com, Azure DevOps Repos, and GitLab.com

GitHub.com, Azure DevOps Repos, and GitLab.com provide enterprise-level allow listing features that require additional IP addresses.

### <img src='/wp-content/uploads/gij-global-icon.png' height=22 width=22 valign=middle />&nbsp; Global Region (US-East-1)

54.196.201.91, 34.228.185.171, 34.224.218.252, 3.80.89.149, 34.224.101.92, 34.224.75.91, 52.23.171.14, 54.147.140.182, 54.235.62.22, 54.175.233.217, 18.208.171.222, 54.90.148.157, 54.242.227.154, 54.209.11.3, 3.88.216.216, 3.80.49.193, 54.87.49.117, 54.174.135.57, 52.54.150.111

### <img src='/wp-content/uploads/gij-us-icon.png' height=22 width=22 valign=middle />&nbsp; USA Region (US-East-2)

3.130.34.25, 18.218.122.134, 3.131.213.149, 3.143.100.15, 3.133.34.235, 18.190.109.9, 18.119.80.14, 3.14.197.223, 3.142.176.34, 3.130.151.4

### <img src='/wp-content/uploads/gij-eu-icon.png' height=24 width=24 valign=middle />&nbsp; Central EU Region (EU-Central-1)

3.123.136.62, 18.156.8.182, 18.198.71.138, 3.69.186.247, 3.70.82.79, 18.159.165.4, 3.125.231.184, 3.68.13.136, 3.67.63.5, 52.58.106.61

### <img src='/wp-content/uploads/gij-eu-icon.png' height=24 width=24 valign=middle />&nbsp; Western EU Region (EU-West-1)

34.247.19.97, 54.72.243.188, 52.210.99.19, 54.76.253.102

### Southeast Asia - Singapore Region

18.140.19.30, 18.143.232.103, 54.151.179.195, 18.138.219.190

### <img src='/wp-content/uploads/gij-au-icon.png' height=24 width=24 valign=middle />&nbsp; Australia Region

54.206.176.144, 3.105.72.140, 52.64.118.63, 13.238.136.180

If you use these IP addresses for allow listing, contact [GIJ Cloud Support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/) so we can notify you if these addresses change.

&nbsp;

## Verify Network Reachability

Your self-hosted git server must have a public address that the GIJ Cloud indexing service can reach.

If your git server sits behind a firewall, add the indexing service IP addresses to your allow list (see [Configure allow list](#configure-allow-list-for-self-hosted-git-repositories)).

If your git server is accessible only through a private intranet or VPN, the GIJ Cloud indexing service cannot reach it—even with an allow list. Use [webhook indexing](#webhooks-indexing-integration-for-private-networks) instead.

**Reachability examples:**

| Reachable? | Example |
| :--- | :--- |
| ![](/wp-content/uploads/gij-check.png) | `https://git.corp.com/repository/widget-production.git` — Hosted git repository |
| ![](/wp-content/uploads/gij-check.png) | `https://git.corp.com` — Git server running GitHub/GitLab |
| ![](/wp-content/uploads/gij-check.png) | `https://gitlab.corp.com:8088` — Server on non-standard port |
| ![](/wp-content/uploads/gij-check.png) | `http://52.123.19.12` — Server without DNS |
| ![](/wp-content/uploads/gij-error.png) | `192.168.1.92` — Private IP address |
| ![](/wp-content/uploads/gij-error.png) | `git.corp` — Private network hostname |

&nbsp;

## Webhooks Indexing Integration for Private Networks

Webhook indexing supports indexing commits and pull requests using webhook metadata. This approach keeps your git server in a private network while sending sufficient git metadata to associate activity with Jira issues.

**Limitations:**
- Cannot view source code (Jira issue ➜ **Git Commits** tab ➜ **View full commit**)
- Cannot create branches or pull/merge requests from within Jira

For more information, see:
- [Classic webhook indexing explainer](/git-integration-for-jira-cloud/classic-indexing-explainer-gij-cloud)
- [Webhook indexing integration](/git-integration-for-jira-cloud/webhook-indexing-explainer-gij-cloud)
  - [GitHub](/git-integration-for-jira-cloud/github-webhook-indexing-integration-gij-cloud)
  - [GitLab](/git-integration-for-jira-cloud/gitlab-webhook-indexing-integration-gij-cloud)
  - [Microsoft](/git-integration-for-jira-cloud/microsoft-webhook-indexing-integration-gij-cloud)

&nbsp;

## GIJ Cloud Apps

- [Git Integration for Jira Cloud](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview)
- [Dev Info for Jira Cloud](https://marketplace.atlassian.com/apps/1219270/dev-info-for-jira?hosting=cloud&tab=overview)

## Get Support

Contact [GIJ Cloud Support](https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/) for help connecting self-hosted git servers or repositories.

<kbd>Last updated: December 2025</kbd>
