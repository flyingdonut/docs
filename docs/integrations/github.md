---
layout: default
title: GitHub
parent: Integrations
nav_order: 1
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

# GitHub Integration
{: .no_toc .fs-9 }

## What is GitHub?
[GitHub](https://github.com){:target="_blank"} is a powerful collaboration, code review, and code management for open 
source and private projects. GitHub offers online source code hosting for Git projects, with powerful collaboration, 
code review, and issue tracking.

---

## What do I get?
With this integration, GitHub will post the commits, and the commit comments to a Flying Donut project.
You will be able to see which commit is part of which task (or card) with a quick link to the GitHub commit.

You will also be able to apply the Flying Donut workflow via the commit messages. For example, you can update the
time left of a task to 5 hours from within the commit message by typing `#1556 -left 5h`.

Enabling integration with GitHub Issues allows you to apply Scrum or Kanban to your issues. All linked issues are 
tracked in real time and updates appear in both Flying Donut and GitHub.

---

## Getting Started
1. Navigate to your project and locate its settings. If you have admin permissions, you will see the integrations tab.
   Click on the enable button to enable the GitHub integration. Only project administrators (or owners) are allowed
   to set up GitHub integration.

   ![GitHub - Enable Integration](/assets/tutorial/github/enable.github.integration.png)

1. Click on the `Details` button to see the GitHub configuration details. You will see:
   - an option to login to GitHub and proceed with automatic GitHub configuration/integration.
   - an option to create endpoints to be used for manual configuration.

We recommend the auto configuration.

   ![GitHub - Details start](/assets/tutorial/github/details.start.png)

---

## Configuration with GitHub Authentication
1. Login to GitHub. When setting up a GitHub integration for the first time, you will be presented with a GitHub 
   consent page that lists the permissions that Flying Donut is requesting. If you are not signed in to GitHub, 
   you will be asked to do so. Once you give the required consent, you will be able to select the repository you want 
   to link with the project.

   ![GitHub - Logged-in details](/assets/tutorial/github/details.logged-in.png)

1. Configure new repo. Once you have given the required consent, you will be presented with a list of the GitHib 
   repositories you have access to. Click on the Create Webhook button once you have selected the repository.

   ![GitHub - Link bucket with repo](/assets/tutorial/github/repo.to.link.bucket.png)

1. You are done. The project is linked with the repository. If you wish to undo, then unlink the project and click on 
   the Logout from GitHub button.

   ![GitHub - Linked bucket with repo](/assets/tutorial/github/linked.repo.bucket.png)

---

## Why do Flying Donut require write permissions to the GitHub repos?
When setting up a GitHub integration for the first time, you will be presented with a GitHub consent page that lists 
the permissions that Flying Donut is requesting.

![GitHub - Review Permissions](/assets/tutorial/github/github.authorize.permissions.png)

Unfortunately, the only way that Flying Donut can access and configure of your public and private repositories is 
with GitHub's "repo" scope, which provides all the other permissions listed above.

We don't use all of them. Of this list, the only permissions Flying Donut use are the ones to read repo data 
(to get a list of your public and private repositories) and the **write** permission to create the webhooks on GitHub. 

In case you enabled the **issues** integration to sync the issues between GitHub and Flying Donut then we will use the
**write** permission to update the issues and the labels in GitHub. 

---

## Manual Configuration
1. **Generate a new Payload URL**. If you wish to configure GitHub manually, click on the
   `Generate a new Payload URL` button.

   ![GitHub - Details start](/assets/tutorial/github/details.start.png)

1. **Use the Key**. Once you generate the key, you will have the configuration options available to configure the 
   GitHub webhook. Go through the 
   [GitHub instructions](https://developer.github.com/webhooks/creating)
   page on how to set up webhooks for more general details.
   
   ![GitHub - Endpoint URL](/assets/tutorial/github/endpoint.url.png)

1. **Add webhook in GitHub**. In GitHub, set up the project webhook to complete the integration. When setting up the 
   required webhook paste the generated `Payload URL` and the `Secret`. Select `application/json` for the Content Type. 
   Flying Donut also requires you to select the following individual events:
   
   1. Push
   1. Commit Comment

   ![GitHub - Add new webhook](/assets/tutorial/github/github.webhook.png)

---

## Commit Message
### Card & Tasks
Once you have linked the Flying Donut project with a GitHub repository you will get updates on the latest commits
on your cards and tasks. When clicking on the git hash, you will be redirected to the GitHub commit page.

![GitHub - Task with commit hover](/assets/tutorial/github/task.with.commit.hover.png)
![GitHub - Task with commit list](/assets/tutorial/github/task.with.commit.list.png)

### Commit Message
You just tag your commits with Card/Task IDs, and GitHub automatically comments on your card or task with the
commit message. Most importantly, you will be able to apply the Flying Donut workflow via the commit messages.
The Card/Task IDs identifiers are the ones at the upper left `#{id}`.

![Idea commit message](/assets/tutorial/idea.commit.message.png)

#### Task
Flying Donut understands the following commands in the commit message in regard to the task:
- `-todo`: Move the task to *To Do*.
- `-doing`: Move task to *Doing*. Use it when a task is in *Done* and, you need to move it back to *Doing*.
- `-done`: Move the task to *Done*.
- `-left`: Update the *time left*. Example of supported syntax is: `-left 5h 20m` or the equivalent `-left 5:20`
- `-spent`: Aggregate the *time spent*. Example of supported syntax is: `-spent 5h 20m` or the equivalent `-spent 5:20`

You can combine the `-left` and `-spent` to update the task in a single commit. For example: `#532 -left 2h -spent 8h`
will move the task to *Doing*, update the *time left*, and update the *time spent*. When using `#{id}` by default the
task moves to *Doing* when in *To Do*.


#### Card.
Flying Donut understands the following commands in the commit message in regard to the card:
- `-done`: Move the tasks of the card to *Done*. The card will move into Done state

**Examples**
If in a single commit you have multiple tasks that should be updated then you just add all of them in the commit message.
An example of a commit message that could someone could use is:
```
Refactored database for the needs of: #3224 -done #3236 -left 15h
```

Or a more verbal one:
```
#3224 is -done and I -spent 12h. 
Started working on #3236. I already -spent 3h but it was underestimated. I think it has -left 15h
```

---

## User Identification
### Make sure you have verified email
Flying Donut uses the email address you set in your local Git configuration to associate commits with your
Flying Donut account. To see the email address you have in your local git type:
```
$ git config user.email # your_email@example.com
```

You have to have `your_email@example.com` added and verified in your Flying Donut account.

For a detailed description, on how to configure you email in `GitHub`, please refer to the github instructions.

### Add your email to your account
In case the git email is not added to your Flying Donut account then add it in the  **account settings** and verify it.
Then you will be able to apply the Flying Donut workflow via the commit messages.

---

## GitHub Issues
When linking a GitHub repository and Flying Donut project, we create custom labels that will give you a reflection on 
what is going on in Flying Donut. All labels created by Flying Donut have an `fd:` prefix.

![GitHub - Labels](/assets/tutorial/github/issues/labels.png)

Linked cards will have an indication at the top left. Clicking at the GitHub issue number will open up a new tab with 
the issue at GitHub. A card linked to a GitHub issue displays the labels of the issue in readonly mode.

![GitHub - Linked task](/assets/tutorial/github/linked.task.png)
![GitHub - Linked task label](/assets/tutorial/github/linked.task.label.png)

Setting any of the approval statuses (e.g. approve) of a linked cards will close the issue in GitHub.

![GitHub - Linked task approved label](/assets/tutorial/github/linked.task.label.approved.png)
![GitHub - Linked task rejected label](/assets/tutorial/github/linked.task.label.rejected.png)

When you include an auto-linked backlog bucket, you will have an indication next to its name. Clicking at the link will 
open up a new tab with the issues in GitHub.

![GitHub - Linked bucket](/assets/tutorial/github/linked.bucket.png)

All cards created in this bucket will be created as issues in GitHub and vice versa. Cards created outside the 
bucket will only exist in Flying Donut. Moving a card in to the bucket will not link the card to a GitHub issue.

---

## Import GitHub Issues
Once you have linked a project, will have the option to import existing GitHub issues to Flying Donut.

![GitHub - Linked bucket button](/assets/tutorial/github/linked.bucket.hover.png)

You will be presented with all the issues in GitHub sorted by date. You may select individual issues one by one all at 
once with a click at the check-box at the left top.

![GitHub - Linked bucket modal top](/assets/tutorial/github/linked.bucket.import.png)

At the bottom of the page you have the option to move to the next or previous page and continue with the selection of 
issues. Then import issues you selected.

![GitHub - Linked bucket modal bottom](/assets/tutorial/github/linked.bucket.import.bottom.png)

---

## Issues User Identification
At this point we don't provide user identification for the GitHub Issues.