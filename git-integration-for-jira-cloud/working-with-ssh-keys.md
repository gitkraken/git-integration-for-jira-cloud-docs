---

title: Working with SSH keys
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

# Working with SSH keys

<https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/1923023617/Working+with+SSH+keys>

* * *

SSH keys are required in order to provide secure connection with the remote git host. The Git Integration for Jira app uses one set of keys for accessing all configured repositories.

Follow this guide if you are one of the users who are limited to or wanted to use SSH to securely connect to your git repositories.

Features such as branch and pull/merge request creation is only available to repositories/git hosts that were connected via the Full feature integration (_formerly Auto-connect integration_).

## Getting started

Before connecting repositories via SSH, users are required to generate SSH keys for use with the remote git host (_public key_) and for Git Integration app in Jira (_private key_).

Generated SSH keys always come in pair. (**Example:** `id_rsa.pub` and `id_rsa`)

For establishing safety connection with SSH, upload a **public key** to the SSH server and set the **private key** to the SSH client.

In this case, the SSH server is the Git server and the SSH client is the Jira server. Therefore:

*   Git server — public key
    
*   Jira server — private key
    

Note that Git Integration for Jira app SSH key:

*   must not be created using the OpenSSH format.
    
*   must be the private key.
    
*   must use the supported certificate format: RSA.
    
*   must use the supported storage format: OpenSSL PEM.
    

\------------------------------------------------------------------------------------------------------------  
For more information, see known issue [SSH key format is invalid](https://bigbrassband.atlassian.net/wiki/spaces/GITCLOUD/pages/421363756/SSH+key+file+format+is+invalid).

|     |
| --- |
| **Windows** |
| For Windows, we recommend to use [**PuTTY**](https://www.putty.org/) and use PuTTYgen to generate public and private SSH keys.<br><br>![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/1923023617/puttygen-key-dlg.png?version=1&modificationDate=1630063568037&cacheVersion=1&api=v2&width=442&height=434)<br><br>1.  Launch **PuTTYgen** and refer to the above image for the rest of the steps on this section.<br>    <br>2.  Set _**Type of key to generate**_ to **RSA**.<br>    <br>3.  Set _**Number of bits in a generated key**_ to **4096**.<br>    <br>4.  Click **Generate**.<br>    <br>5.  Follow screen instructions such as moving your mouse pointer on random locations on the blank area of the PuTTYgen dialog. Do this until the progress bar completely fills up and the SSH key pair is generated.<br>    <br>6.  Entering a **Passphrase** for the generated key is optional but will ensure a more secure connection.<br>    <br>7.  Save your generated public and private key to a file by clicking the respective options.<br>    <br>8.  Copy the generated key. This is the public key that you will be using on the SSH configuration page of your git host.<br>    <br>9.  For the private key, see the note below.<br>    <br><br>PuTTY creates a private key in its own ".ppk" format. To convert it to ".pem", the user should do the **Conversions** ➜ **Export OpenSSH key** menu option in PuTTYgen. Add/upload this file to Git Integration for Jira app ➜ **SSH keys** or when prompted on connecting SSH git repositories in Jira via Connect wizard.<br><br>You can also use the git bash command line to generate SSH key pair. For detailed information, see [**Generate SSH via Git bash**](https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key).<br><br>Read on the article, [Generating SSH Keys](/wiki/spaces/GITCLOUD/pages/1923023647/Generating+SSH+Keys), and follow specific information for the git host and platform that you use. |

|     |
| --- |
| **Linux/MacOS** |
| On Linux and MacOS, this generates an SSH key in RSA format:<br><br>```java<br>ssh-keygen -t rsa -b 4096 -m pem -C "your_email@example.com"<br>```<br><br>MacOS often incorrectly creates an OpenSSH format certificate. For more details, see information on this [**common problem**](https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key). |

[« Getting started for Git administrators](/wiki/spaces/GITCLOUD/pages/1923023183/Getting+started+for+Git+administrators)

[Generating SSH keys »](/wiki/spaces/GITCLOUD/pages/1923023647/Generating+SSH+Keys)

### More related topics about SSH integration

*   Page:
    
    [Working with SSH keys](/wiki/spaces/GITCLOUD/pages/1923023617/Working+with+SSH+keys) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Generating SSH Keys](/wiki/spaces/GITCLOUD/pages/1923023647/Generating+SSH+Keys) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Connecting SSH Git Repositories (Jira Cloud)](/wiki/spaces/GITCLOUD/pages/1923023732) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Adding a public SSH Key](/wiki/spaces/GITCLOUD/pages/1923023758/Adding+a+public+SSH+Key) (Git Integration for Jira Cloud)
    
*   Page:
    
    [Working with SSH keys](/wiki/spaces/GITSERVER/pages/1923027331/Working+with+SSH+keys) (Git Integration for Jira Server)
    
*   Page:
    
    [Generating SSH keys](/wiki/spaces/GITSERVER/pages/1923027361/Generating+SSH+keys) (Git Integration for Jira Server)
    
*   Page:
    
    [Adding a private SSH key](/wiki/spaces/GITSERVER/pages/1923027446/Adding+a+private+SSH+key) (Git Integration for Jira Server)
    
*   Page:
    
    [Adding a public SSH Key](/wiki/spaces/GITSERVER/pages/1923745275/Adding+a+public+SSH+Key) (Git Integration for Jira Server)
    
*   Page:
    
    [SSH keys configuration](/wiki/spaces/GITSERVER/pages/1923745291/SSH+keys+configuration) (Git Integration for Jira Server)
    
*   Page:
    
    [Adding and associating SSH keys](/wiki/spaces/GITSERVER/pages/1923745314/Adding+and+associating+SSH+keys) (Git Integration for Jira Server)
    
*   Page:
    
    [Removing SSH keys](/wiki/spaces/GITSERVER/pages/1923031128/Removing+SSH+keys) (Git Integration for Jira Server)
    
*   Page:
    
    [Reconfigure Git repositories and SSH keys](/wiki/spaces/GITSERVER/pages/1923031158/Reconfigure+Git+repositories+and+SSH+keys) (Git Integration for Jira Server)
    
*   Page:
    
    [Working with SSH keys](/wiki/spaces/GIJDC/pages/1930396577/Working+with+SSH+keys) (Git Integration for Jira Data Center)
    
*   Page:
    
    [Generating SSH keys](/wiki/spaces/GIJDC/pages/1930396609/Generating+SSH+keys) (Git Integration for Jira Data Center)
    
*   Page:
    
    [Adding a private SSH key](/wiki/spaces/GIJDC/pages/1930396698/Adding+a+private+SSH+key) (Git Integration for Jira Data Center)