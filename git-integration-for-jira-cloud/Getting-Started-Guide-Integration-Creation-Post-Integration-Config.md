---

title: Integration Creation and Post Integration Configuration
description: Step-by-step guidance for creating integrations and configuring post-integration settings
taxonomy:
    category: git-integration-for-jira-cloud

---

## Integration Creation

### Choosing Authentication Type

Decide which authentication option works best for you. Full Featured integrations support both PAT (Personal Access Token) and OAuth-based authentication, though availability varies by Git service. Functionally, both options work similarly in most cases.

We recommend OAuth authentication when available. OAuth allows GIJ to perform certain automatic actions depending on the account's permission level and the Git service. In some cases, GIJ can automatically create indexing triggers for your repositories, saving you time and effort.

<div class="bbb-callout bbb--tip">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
        If you use multiple service accounts for authentication, use an incognito or private browser window when creating integrations. This lets you sign in with different accounts and avoids using cached credentials, which would associate the same account with multiple integrations.
    </div>
    </div>
</div>

PAT authentication is easier to maintain at an organizational level, especially when using multiple service accounts. Git Service Admins typically have easy access to generate PATs for accounts. For detailed instructions, see [Creating Personal Access Tokens](/git-integration-for-jira-cloud/creating-personal-access-tokens-gij-cloud).

### Creating Your Integrations

Ready for the fun part? It's time to create your integrations.

For detailed step-by-step instructions by Git service, refer to our [Integration Guides](/git-integration-for-jira-cloud/integration-guide-gij-cloud/). See the [Webhook Indexing Integration Guides](/git-integration-for-jira-cloud/webhook-indexing-integration-gij-cloud/) for instructions on supported Git services.

All your planning and decisions from previous steps apply during integration creation. You should now feel confident choosing your authentication type, selecting repositories to include, and applying Project Association permissions to limit visibility.

If using multiple integrations, consider creating only one or two at a time. Wait until the initial indexing phase completes for each new integration before creating the next one. This approach reduces the probability of rate limiting issues or overloading the application with a large backlog of tasks.

While this approach takes longer to complete, it avoids common issues and quickly surfaces important problems to address before committing time to create all integrations. For any issues, contact our support team to work through problems and save time.

&nbsp;

## Post Integration Configuration

After creating all your integrations, we recommend the following actions to complete your configuration.

### Edit Integration Feature Settings

#### Display Name

Edit each integration and modify the display name to better reflect what it contains or which org/group it connects to.

#### Require User PAT

We strongly recommend enabling the "Require User PAT" integration setting. This option requires all users to provide their own PAT the first time they create a branch or pull/merge request from inside Jira.

This is important because GIJ uses their PAT to authenticate newly created branches and pull/merge requests, attributing them to the correct user on your Git service. If you don't enable this option, branches and pull/merge requests are still created, but they're authenticated using the integration connection credentials and attributed to whatever account those credentials belong to.

See [Require Personal Access Tokens](/git-integration-for-jira-cloud/require-personal-access-tokens-for-user-actions-create-branch-pull-request-gij-cloud/) for further details.

&nbsp;

---

[<b style='background-color:#FFFCC3; padding:1px 5px; color:#181D28; border-radius:3px; margin: 0 5px; font-size: medium;'>NEXT</b>](/git-integration-for-jira-cloud/Getting-Started-Guide-Optional-Features) <a href="https://help.gitkraken.com/git-integration-for-jira-cloud/Getting-Started-Guide-Optional-Features/">Optional Features and Add-on Extensions</a>

[<b style='background-color:#F1F1F1; padding:1px 5px; color:#181D28; border-radius:3px; margin: 0 5px; font-size: medium;'>PREVIOUS</b>](/git-integration-for-jira-cloud/Getting-Started-Guide-App-operations-and-planning/) <a href="https://help.gitkraken.com/git-integration-for-jira-cloud/Getting-Started-Guide-App-operations-and-planning/">Application Operations and Planning</a>

<p>&nbsp;</p>

<p style="text-align: center; margin: 0; padding: 0;"><kbd>Last updated: December 2025</kbd></p>
