---
layout: default
title: Bitbucket
parent: Integrations
nav_order: 2
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

# Bitbucket Integration
{: .no_toc .fs-9 }

## What is Bitbucket?
Bitbucket is a hosting service for projects that use either the Mercurial or Git revision control systems. 
Bitbucket offers free source code hosting for Git and Mercurial projects as well as project wikis and issue tracking

## What do I get?
With this integration, Bitbucket will post the commits, and the commit comments to a Flying Donut project. 
You will be able to see which commit is part of which task (or card) with a quick link to the Bitbucket commit.

You will also be able to apply the Flying Donut workflow via the commit messages. For example, you can update the 
time left of a task to 5 hours from within the commit message by typing `#1556 -left 5h`.

## Getting Started
1. Navigate to your project and locate its settings. If you have admin permissions, you will see the integrations tab. 
   Click on the enable button to enable the Bitbucket integration. Only project administrators (or owners) are allowed 
   to set up Bitbucket integration.
   
   ![Bitbucket - Enable Integration](/assets/tutorial/bitbucket/enable.bitbucket.integration.png)

1. Click on the `Details` button to see the Bitbucket configuration details. You have the option to proceed with a
   manual configuration.
   
   ![Bitbucket - Details](/assets/tutorial/bitbucket/details.start.png)

## Configuration
1. **Generate a new Payload URL**. To configure Bitbucket you click on the Generate a new Payload URL button.

   ![Bitbucket - Details](/assets/tutorial/bitbucket/details.start.png)
   
1. **Use the Key**. Once you generate the key, you will have the configuration options available to configure the Bitbucket 
   webhook. Go through the Manage webhooks on how to set up webhooks for more general details.

   ![Bitbucket - Endpoint URL](/assets/tutorial/bitbucket/endpoint.url.png)
   
1. **Add webhook in Bitbucket**. In Bitbucket, create a webhook to complete the integration. When setting up the required
   webhook, paste the generated Payload URL. Bitbucket supports HTTPS and basic authentication in the following url 
   format `https://user:password@server:port/path/`. Therefore, the generated payload url contains a combination of 
   `username:secret` and a unique project token.
   
   Select the repository push trigger and save. The integration is complete. Every time a user pushes commits in the 
   repository, your project will receive updates on the latest commits on your cards and tasks.

   ![Bitbucket - Add new webhook](/assets/tutorial/bitbucket/bitbucket.webhook.png)

## Commit Message
### Card & Tasks
Once you have linked the Flying Donut project with a Bitbucket repository you will get updates on the latest commits 
on your cards and tasks. When clicking on the git hash, you will be redirected to the Bitbucket commit page.

   ![Bitbucket - Task with commit hover](/assets/tutorial/bitbucket/task.with.commit.hover.png)
   ![Bitbucket - Task with commit list](/assets/tutorial/bitbucket/task.with.commit.list.png)

### Commit Message
You just tag your commits with Card/Task IDs, and Bitbucket automatically comments on your card or task with the 
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

## User Identification
### Make sure you have verified email
Flying Donut uses the email address you set in your local Git configuration to associate commits with your 
Flying Donut account. To see the email address you have in your local git type:
```
$ git config user.email # your_email@example.com
```

You have to have `your_email@example.com` added and verified in your Flying Donut account.

For a detailed description, on how to configure you email in `Bitbucket`, please refer to the bitbucket instructions.

### Add your email to your account
In case the git email is not added to your Flying Donut account then add it in the  *account settings* and verify it. 
Then you will be able to apply the Flying Donut workflow via the commit messages.