---

title: Connecting SSH Git Repositories to Jira Cloud
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
**What’s on this page:**

* * *

## Introduction

SSH git repositories can be integrated with Jira Cloud via [**Git Integration for Jira app**](https://marketplace.atlassian.com/apps/4984/git-integration-for-jira?hosting=cloud&tab=overview).

## Generating SSH Keys

Initially, the SSH key pair must be generated to proceed. We recommend to generate a **4096-bit key**.

|     |
| --- |
| **Windows** |
| For Windows users, we recommend to use [**PuTTY**](https://www.putty.org/) and use PuTTYgen to generate public and private SSH keys.<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/864288769/image-20201102-074007.png?version=1&modificationDate=1604302815352&cacheVersion=1&api=v2&width=479&height=471)<br><br>1.  Launch **PuTTYgen** and refer to the above image for the rest of the steps on this section.<br>    <br>2.  Set _**Type of key to generate**_ to **RSA**.<br>    <br>3.  Set _**Number of bits in a generated key**_ to **4096**.<br>    <br>4.  Click **Generate**.<br>    <br>5.  Follow screen instructions such as moving your mouse pointer on random locations on the blank area of the PuTTYgen dialog. Do this until the progress bar completely fills up and the SSH key pair is generated.<br>    <br>6.  Entering a **Passphrase** for the generated key is optional but will ensure a more secure connection.<br>    <br>7.  Save your generated public and private key to a file by clicking the respective options.<br>    <br>8.  Copy the generated key. This is the public key that you will be using on the SSH configuration page of your git host.<br>    <br>9.  For the private key, see the note below.<br>    <br><br>PuTTY creates a private key in its own ".ppk" format. To convert it to ".pem", the user should do the **Conversions** ➜ **Export OpenSSH key** menu option in PuTTYgen. Add/upload this file to Git Integration for Jira app ➜ **SSH keys** or when prompted on connecting SSH git repositories in Jira.<br><br>You can also use the git bash command line to generate SSH key pair. For detailed information, see [**Generate SSH via Git bash**](https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key).<br><br>Read on the section in our online documentation, [**Generating SSH Keys**](https://bigbrassband.com/git-integration-for-jira/documentation/working-with-ssh-keys.html#generate_SSH_keys), and follow specific information for the git host and platform that you use. |
| **Linux/MacOS** |
| On Linux and MacOS, this generates an SSH key in RSA format:<br><br>```ssh-keygen -t rsa -b 4096 -m pem -C "your_email@example.com"```<br><br>MacOs often incorrectly creates an OpenSSH format certificate. For more details, see information on this [common problem](https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key). |

## Power Users

The Git Integration for Jira app supports one format for private SSH keys ➜ RSA. To change your SSH key pair to the supported format, use the following syntax on your terminal or bash/powershell:

```
ssh-keygen -p -P "old_password" -N "new_password" -m pem
```

## Connecting SSH Git Repositories

1.  Generate an SSH key pair as stated in the previous section.

2.  Obtain the Clone SSH git URL from your git host repository page.

3.  On your Jira Cloud dashboard, go to menu **Apps** ➜ **Git Integration: Manage integrations**.

4.  On the top-right corner click on **Add integration**.

5.  Select the **Single git repository integration (Plain git)** option.

6.  Paste the clone URL into the **Host URL** field.

7.  Paste the Private SSH key on the provided box or click **Upload Key File** to upload a private SSH key file.

8.  Enter the **Passphrase** of the private SSH key, if any. Otherwise, leave it blank.

9.  Click on **Add Integration**.


The connected repository is listed in the git configuration page.

For Jira Cloud integration, we recommend to use the [**Git service integration**](/using-the-git-service-integration-wizard-gij-cloud) panel for connecting multiple git repositories. It provides additional features that are not present with SSH integrations in Jira Cloud.