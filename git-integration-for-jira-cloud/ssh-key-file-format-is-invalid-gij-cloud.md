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

&nbsp;

## Diagnosis

Jira admins will see a message similar to the one below when adding the SSH key:

    \> _The key format is invalid. Please check your private key._

<br>

<img src='/wp-content/uploads/gij-private-key.png' width=494 height=454 style='max-width:100%;display:block;margin:25px auto;' />

Full error (stack trace) available in the Manage Git Repositories wizard or in Jira logs `/application-logs/atlassian-jira.log`:

**Example Error:**

```java
com.bigbrassband.jira.git.exceptions.repository.InvalidPrivateKeyException: Private SSH key is invalid or empty
at com.bigbrassband.jira.git.services.ssh.KeyManagerImpl.needPassphrase(KeyManagerImpl.java:103)
at com.bigbrassband.jira.git.rest.wizard.WizardResource.validateRepoOrigin(WizardResource.java:104)
at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
...
at org.apache.tomcat.util.net.NioEndpoint$SocketProcessor.doRun(NioEndpoint.java:1498)
at org.apache.tomcat.util.net.SocketProcessorBase.run(SocketProcessorBase.java:49)
at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
at org.apache.tomcat.util.threads.TaskThread$WrappingRunnable.run(TaskThread.java:61)
at java.lang.Thread.run(Thread.java:748)
Caused by: com.jcraft.jsch.JSchException: invalid privatekey: [C@17h421rm
at com.jcraft.jsch.KeyPair.load(KeyPair.java:664)
at com.bigbrassband.jira.git.services.ssh.KeyManagerImpl.needPassphrase(KeyManagerImpl.java:99)
... 264 more
```

&nbsp;

## Cause

Jira admin has provided an SSH public key or an SSH private key with an incorrect format.

&nbsp;

## Solutions

1. Create a new SSH key:

    **On Linux and macOS:**

    Use the following command to create a certificate:<br>

    ```powershell
    ssh-keygen -t rsa -b 4096 -m pem -C your_email@example.com
    ```

    <div class="bbb-callout bbb--alert">
      <div class="irow">
        <div class="ilogobox">
          <span class="logoimg"></span>
        </div>
        <div class="imsgbox">
          MacOS often incorrectly creates an OpenSSH format certificate. For more details, see information on this <a href='https://serverfault.com/questions/939909/ssh-keygen-does-not-create-rsa-private-key' target='_blank'><b>common problem</b></a>.
        </div>
      </div>
    </div>
    <br>

    **On Windows:**

    Download [**PuTTY**](https://www.putty.org/) and use PuTTYgen to generate an SSH key pair:

    1.  Set _**Type of key...**_ to **RSA**.

    2.  Set _**Number of bits...**_ to **4096**.

    3.  Click **Generate**. Move mouse pointer on the blank area as instructed.

    4.  Follow screen instructions such as moving your mouse pointer on random locations on the blank area of the PuTTYgen dialog. Do this until the progress bar completely fills up and the SSH key pair is generated.

    5.  Entering a **Passphrase** for the generated key is optional but will ensure a more secure connection.

    6.  Save your generated public and private key to a file by clicking the respective options.

    7.  Copy the generated key. This is the public key that you will be using on the SSH configuration page of your git host.

    8.  For the private key, PuTTY creates a private key in its own ".ppk" format. Convert it to ".pem" via menu **Conversions** \> **Export OpenSSH key** in PuTTYgen. Add/upload this file to Git Integration for Jira app \> **SSH Keys** or when prompted on connecting SSH git repositories in Jira.

2.  Create a new SSH key using RSA certificate format. See Solution #1.

3.  Use OpenSSL PEM storage format. See Solution #1.

4.  Provide the public SSH key to the SSH configuration of your git host.

5.  Provide the private SSH key to the Git Integration for Jira app \> **SSH Keys** or when prompted on connecting SSH git repositories in Jira.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        <b>Contact Us</b><br>
        If you still have a question - reach out to our <a href='https://help.gitkraken.com/git-integration-for-jira-cloud/gij-cloud-contact-support/' target='_blank'>Support Desk</a> or email us at <a href='mailto:gijsupport@gitkraken.com'>gijsupport@gitkraken.com</a>.
    </div>
    </div>
</div>
<br>

## Related articles

[Why don't I see commits? (Git Integration for Cloud)](/git-integration-for-jira-cloud/why-dont-i-see-commits-git-integration-for-cloud-gij-cloud) (Git Integration for Jira Cloud)

[Repositories missing from Azure DevOps (or VSTS) integration](/git-integration-for-jira-cloud/repositories-missing-from-azure-devops-or-vsts-integration-gij-cloud) (Git Integration for Jira Cloud)

[Licensing error - installCheck failed](/git-integration-for-jira-cloud/licensing-error-installcheck-failed-gij-cloud) (Git Integration for Jira Cloud)

[Why don't I see the Create branch or pull request features?](/git-integration-for-jira-cloud/why-dont-i-see-the-create-branch-or-pull-request-features-gij-cloud) (Git Integration for Jira Cloud)

[Connection error for self-hosted git servers](/git-integration-for-jira-cloud/connection-error-for-self-hosted-git-servers-gij-cloud) (Git Integration for Jira Cloud)

**SSH key file format is invalid** (this page)

[Error while reindexing - Java heap space / Object too large, rejecting the pack](/git-integration-for-jira-cloud/error-while-reindexing-java-heap-space-object-too-large-rejecting-the-pack-gij-cloud) (Git Integration for Jira Cloud)

[OAuth connection error or error 401 page with Azure DevOps integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-integration-gij-cloud) (Git Integration for Jira Cloud)

[OAuth connection error or error 401 page with Azure DevOps with Active Directory integration](/git-integration-for-jira-cloud/oauth-connection-error-or-error-401-page-with-azure-devops-with-active-directory-integration-gij-cloud) (Git Integration for Jira Cloud)

[Empty list of repositories after integration of Azure Repos](/git-integration-for-jira-cloud/empty-list-of-repositories-after-integration-of-azure-repos-gij-cloud) (Git Integration for Jira Cloud)

[Reconnecting Azure DevOps and VSTS OAuth integrations](/git-integration-for-jira-cloud/reconnecting-azure-devops-and-vsts-oauth-integrations-gij-cloud)

