---

title: SSH key file format is invalid
description:
taxonomy:
    category: git-integration-for-jira-cloud

---
## Problem

Git Integration for Jira application SSH keys:

1.  Must not be created using the OpenSSH format

2.  Must be the private SSH key

3.  Must use the supported certificate format: RSA

4.  Must use the supported storage format: OpenSSL PEM


## Diagnosis

Jira admins will see a message similar to the one below when adding the SSH key:

> The key format is invalid. Please check your private key.

![](https://bigbrassband.atlassian.net/wiki/download/thumbnails/421363756/private-key.png?version=1&modificationDate=1586319555483&cacheVersion=1&api=v2&width=453&height=416)

Full error (stack trace) available in the Manage Git Repositories wizard or in Jira logs `/application-logs/atlassian-jira.log`:

|     |
| --- |
| **Error** |
| ```java<br>com.bigbrassband.jira.git.exceptions.repository.InvalidPrivateKeyException: Private SSH key is invalid or empty<br>    at com.bigbrassband.jira.git.services.ssh.KeyManagerImpl.needPassphrase(KeyManagerImpl.java:103)<br>    at com.bigbrassband.jira.git.rest.wizard.WizardResource.validateRepoOrigin(WizardResource.java:104)<br>    at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)<br>    at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)<br>    ...<br>    at org.apache.tomcat.util.net.NioEndpoint$SocketProcessor.doRun(NioEndpoint.java:1498)<br>    at org.apache.tomcat.util.net.SocketProcessorBase.run(SocketProcessorBase.java:49)<br>    at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)<br>    at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)<br>    at org.apache.tomcat.util.threads.TaskThread$WrappingRunnable.run(TaskThread.java:61)<br>    at java.lang.Thread.run(Thread.java:748)<br>Caused by: com.jcraft.jsch.JSchException: invalid privatekey: [C@17h421rm<br>    at com.jcraft.jsch.KeyPair.load(KeyPair.java:664)<br>    at com.bigbrassband.jira.git.services.ssh.KeyManagerImpl.needPassphrase(KeyManagerImpl.java:99)<br>    ... 264 more<br>``` |

## Cause

Jira admin has provided an SSH public key or an SSH private key with an incorrect format.

## Solutions

1\. Create a new SSH key:

|     |
| --- |
| **On Linux and macOS:** |
| Use the following command to create a certificate:<br><br>```java<br>ssh-keygen -t rsa -b 4096 -m pem -C your_email@example.com<br>```<br><br>MacOS often incorrectly creates an OpenSSH format certificate. For more details, see information on this [**common problem**](https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key). |
| **On Windows:** |
| Download [**PuTTY**](https://www.putty.org/) and use PuTTYgen to generate an SSH key pair:<br><br>1.  Set _**Type of key...**_ to **RSA**.<br>    <br>2.  Set _**Number of bits...**_ to **4096**.<br>    <br>3.  Click **Generate**. Move mouse pointer on the blank area as instructed.<br>    <br>4.  Follow screen instructions such as moving your mouse pointer on random locations on the blank area of the PuTTYgen dialog. Do this until the progress bar completely fills up and the SSH key pair is generated.<br>    <br>5.  Entering a **Passphrase** for the generated key is optional but will ensure a more secure connection.<br>    <br>6.  Save your generated public and private key to a file by clicking the respective options.<br>    <br>7.  Copy the generated key. This is the public key that you will be using on the SSH configuration page of your git host.<br>    <br>8.  For the private key, PuTTY creates a private key in its own ".ppk" format. Convert it to ".pem" via menu **Conversions** > **Export OpenSSH key** in PuTTYgen. Add/upload this file to Git Integration for Jira app > **SSH Keys** or when prompted on connecting SSH git repositories in Jira. |

2\. Create a new SSH key using RSA certificate format. See Solution #1.

3\. Use OpenSSL PEM storage format. See Solution #1.

4\. Provide the public SSH key to the SSH configuration of your git host.

5\. Provide the private SSH key to the Git Integration for Jira app > **SSH Keys** or when prompted on connecting SSH git repositories in Jira.

**Contact Us**

If you still have a question - reach out to our [Support Desk](https://bigbrassband.atlassian.net/servicedesk/customer/portals) or email us at [support@bigbrassband.com](mailto:support@bigbrassband.com).

## Related articles

*   Page:

    [Why don't I see commits? (Git Integration for Cloud)](/wiki/spaces/GITCLOUD/pages/110755841) (Git Integration for Jira Cloud)

*   Page:

    [Repositories missing from Azure DevOps (or VSTS) integration](/wiki/spaces/GITCLOUD/pages/421462017/Repositories+missing+from+Azure+DevOps+%28or+VSTS%29+integration) (Git Integration for Jira Cloud)

*   Page:

    [Licensing error - installCheck failed](/wiki/spaces/GITCLOUD/pages/420282445/Licensing+error+-+installCheck+failed) (Git Integration for Jira Cloud)

*   Page:

    [Why don't I see the Create branch or pull request features?](/wiki/spaces/GITCLOUD/pages/421593107) (Git Integration for Jira Cloud)

*   Page:

    [Connection error for self-hosted git servers](/wiki/spaces/GITCLOUD/pages/419659840/Connection+error+for+self-hosted+git+servers) (Git Integration for Jira Cloud)

*   Page:

    [SSH key file format is invalid](/wiki/spaces/GITCLOUD/pages/421363756/SSH+key+file+format+is+invalid) (Git Integration for Jira Cloud)

*   Page:

    [Error while reindexing - Java heap space / Object too large, rejecting the pack](/wiki/spaces/GITCLOUD/pages/421462043) (Git Integration for Jira Cloud)

*   Page:

    [OAuth connection error or error 401 page with Azure DevOps integration](/wiki/spaces/GITCLOUD/pages/420282493/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+integration) (Git Integration for Jira Cloud)

*   Page:

    [OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/wiki/spaces/GITCLOUD/pages/421527629/OAuth+connection+error+or+error+401+page+with+Azure+DevOps+with+Active+Directory+integration) (Git Integration for Jira Cloud)

*   Page:

    [Empty list of repositories after integration of Azure Repos](/wiki/spaces/GITCLOUD/pages/421298248/Empty+list+of+repositories+after+integration+of+Azure+Repos) (Git Integration for Jira Cloud)