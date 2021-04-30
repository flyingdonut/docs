---
layout: default
title: GitLab
parent: Integrations
nav_order: 3
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

# GitLab Integration
{: .no_toc .fs-9 }

## What is GitLab?
[GitLab](https://gitlab.com){:target="_blank"} is an open source web-based Git repository manager with wiki and issue tracking 
features. GitLab includes git repository management, code reviews, an issue tracking and wiki’s.

---

## What do I get?
With this integration, GitLab will post the commits, and the commit comments to a Flying Donut project.
You will be able to see which commit is part of which task (or card) with a quick link to the GitLab commit.

You will also be able to apply the Flying Donut workflow via the commit messages. For example, you can update the
time left of a task to 5 hours from within the commit message by typing `#1556 -left 5h`.

---

## Getting Started
1. Navigate to your project and locate its settings. If you have admin permissions, you will see the integrations tab.
   Click on the enable button to enable the GitLab integration. Only project administrators (or owners) are allowed
   to set up GitLab integration.

   ![GitLab - Enable Integration](/assets/tutorial/gitlab/enable.gitlab.integration.png)

1. Click on the `Details` button to see the GitLab configuration details. You have the option to proceed with a
   manual configuration.

   ![GitLab - Details](/assets/tutorial/gitlab/details.start.png)

---

## Configuration
1. **Generate a new Payload URL**. To configure GitLab you click on the `Generate a new Payload URL` button.

   ![GitLab - Details](/assets/tutorial/gitlab/details.start.png)

1. **Use the Key**. Once you generate the key, you will have the configuration options available to configure the 
   GitLab webhook. Go through the
   [GitLab instructions](https://docs.gitlab.com/ee/user/project/integrations/webhooks.html){:target="_blank"}
   on how to set up webhooks for more details.


   ![GitLab - Endpoint URL](/assets/tutorial/gitlab/endpoint.url.png)

1. **Setup Webhooks in GitLab**. In GitLab, set up the project webhook to complete the integration. When setting up 
   the required webhook paste the generated `Payload URL` and the `Secret`. 
   
   Select the **push events** trigger and click on the **Add webhook** button. The integration is completed. 
   Every time a user pushes commits in the repository, your project will receive updates on the latest commits on your 
   cards and tasks.
   
   ![GitLab - Add new webhook](/assets/tutorial/gitlab/gitlab.webhook.png)

---

## Commit Message
### Card & Tasks
Once you have linked the Flying Donut project with a GitLab repository you will get updates on the latest commits
on your cards and tasks. When clicking on the git hash, you will be redirected to the GitLab commit page.

![GitLab - Task with commit hover](/assets/tutorial/gitlab/task.with.commit.hover.png)
![GitLab - Task with commit list](/assets/tutorial/gitlab/task.with.commit.list.png)

### Commit Message
You just tag your commits with Card/Task IDs, and GitLab automatically comments on your card or task with the
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

For a detailed description on how to configure your commit email in `GitLab`,
read *Setting your email* in the [user account](https://docs.gitlab.com/ee/user/profile/){:target="_blank"} page.

### Add your email to your account
In case the git email is not added to your Flying Donut account then add it in the  **account settings** and verify it.
Then you will be able to apply the Flying Donut workflow via the commit messages.