---

title: Viewing builds and deployments in Jira issue
description:
taxonomy:
    category: git-integration-for-jira-cloud

---

When an issue is associated with a build or deployment, additional information will be available in the right hand panel.

<img src='/wp-content/uploads/gij-cloud-cicd-Issuepanel-1.png' height=588 width=514 style='margin: 15px auto 25px auto; max-width: 100%' />

Builds and Deployments will show as successful or failed based on the icon to the right (<img src='/wp-content/uploads/bbb-tips-20.png' style='' /> green checkmark). Clicking on a build or a release will pop up a new window with a link out to the pipeline for more information.

For pipeline errors, wherein a step within your pipeline has failed, there are several external factors that is causing it to fail. For example:

*   a misconfiguration in your deployment too
*   an incorrectly set environment variable

If a pipeline fails, you have the option to rerun the whole pipeline, or any failed steps. For more information, see Atlassian docs on [How to view your pipeline](https://support.atlassian.com/bitbucket-cloud/docs/view-your-pipeline/#Viewyourpipeline-CI_RerunStep).

<img src='/wp-content/uploads/gij-cloud-cicd-Issuepanel-2.png' height=215 width=933 style='margin: 15px auto 25px auto; max-width: 100%' />

Clicking on **Open Git Integration** will open a view that rolls up all commits by file and developer, and reports change statistics. From here you can click individual commits, builds, and deployments to see more information.

<img src='/wp-content/uploads/gij-cloud-cicd-Issuepanel-3.png' height=726 width=519 style='margin: 15px auto 25px auto; max-width: 100%' />

