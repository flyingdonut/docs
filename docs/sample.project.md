---
layout: page
title: A Sample Project
nav_order: 3
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# A Sample Project
{: .no_toc .fs-9 }

We are going to use Flying Donut to track our house move on May 19th.
{: .fs-6 .fw-300 }

There are things that need to be taken care of regarding the old house and the new house. 
There are also some Kid's related tasks, so these are the categories we will use. In Flying Donut, 
the categories can be represented with backlog buckets or labels.

In terms of deadlines, there are things to do before the move, the day of the move, and after the move, 
so these will be our phases, or sprints.

We are now ready to start entering all this information into Flying Donut:

Log in to your account to create a project. Locate the `+` button in the upper right corner, in the projects,
or dashboard page:

![Project Tutorial - Projects List - Create Project Button](/assets/moving/sc.2021-05-08.23-25-27.png)

Specify the project name, its visibility, and the project type. By default, the project will be created as a private project. 
You can change the visibility to `public` to make it visible to everybody including search engines.

The supported project types are:
- **Kanban:** In `KANBAN` you don't have time boxes or sprints. The board is used to see and change the state of the cards,
  in user defined columns.  
- **Simple Scrum:** In plain old `SCRUM` the accompanying task board is used to see and change the state of the tasks
  of the cards in the current sprint. The columns of the tasks are fixed to  `To Do`, `Doing` and `Done` states.
  Cards with all their tasks `done` are considered as done.
- **Scrumban:** In `SCRUMBAN` the accompanying kanban board is used on top of the scrum framework, supporting 
  all functionality of scrum and kanban. Nowadays, it is considered as the modern way of doing scrum.

![Project Tutorial - Create Project Modal](/assets/moving/sc.2021-05-08.13-46-15.png)

Locate the project from the projects list, and click on the project name to navigate to the project's page. 

![Project Tutorial - Projects List](/assets/moving/sc.2021-05-08.23-25-14.png)

At this point there is very limited information in the project page, but you see that you have more options in the 
left-hand side menu. This part of the menu is enabled when you are in a project context:

![Project Tutorial - Project Overview](/assets/moving/sc.2021-05-08.13-48-12.png)

## Defining the Card Categories, or Backlog Buckets

Select Backlog from the left-side menu. When a project is created, a Default backlog bucket is created:

Select the Default bucket and click on the `edit` button located on the top right-hand side.

![Project Tutorial - Backlog - Default bucket](/assets/moving/sc.2021-05-08.13-55-09.png)

Rename it to Old House.

![Project Tutorial - Backlog - Rename Default bucket](/assets/moving/sc.2021-05-08.13-55-26.png)

Locate the `+` button in the backlog bucket navigation list to add a new bucket. 

![Project Tutorial - Backlog - Create bucket button](/assets/moving/sc.2021-05-08.13-55-43.png)

An input text field appears. Specify a name for the new bucket, New House:

![Project Tutorial - Backlog - Create bucket](/assets/moving/sc.2021-05-08.13-55-52.png)

Similarly create the Kid's Stuff bucket:

![Project Tutorial - Backlog - buckets](/assets/moving/sc.2021-05-08.13-56-45.png)

## Adding Cards to Backlog

Each backlog bucket has an `+` button at the toolbar. 

![Project Tutorial - Backlog - Add card](/assets/moving/sc.2021-05-08.18-05-03.png)

When you click on the button, an input field appears. Simply type the name of the card in the input text box, 
and hit `Enter` or click on the `Add Card` button.

![Project Tutorial - Backlog - Add card input](/assets/moving/sc.2021-05-08.18-05-14.png)

You can add as many items as you can think of. Remember that these are higher level work items, that we 
can break down into smaller tasks later.

![Project Tutorial - Backlog - Add card input](/assets/moving/sc.2021-05-08.18-06-01.png)

Do not worry about thinking of everything up front. You can come back and add more items to your list at
any point.

![Project Tutorial - Backlog - Cards](/assets/moving/sc.2021-05-08.18-16-36.png)

### Edit Card details
You can edit the card details by clicking on the `name` of the card, or via the card menu that is located in the top
right corner of each card. Once you click on the `name`, a modal with the card details will be visible. Start editing
the card with the details and tasks you want.

Add more details for each item, in the item's details. By clicking on the name of the card, the card details
modal will appear, where you can add description, attachments, tasks, comments, and topics.

![Project Tutorial - Backlog - Add card input](/assets/moving/sc.2021-05-08.18-07-04.png)

Let's add tasks on another card that we already know what we will do. We will estimate the tasks as well.

![Project Tutorial - Sprints - Planning - Card Details](/assets/moving/sc.2021-05-08.18-30-58.png)

## Moving the Cards around in the Backlog

The cards can be moved around in backlog via drag 'n drop. The order from top to bottom is used to order the priority
of each card. There are times that you need to move a card from one bucket to another one, though. 

Locate the `Move Cards to Buckets` button and click on it. 

![Project Tutorial - Backlog - Move Cards to Bucket button](/assets/moving/sc.2021-05-08.18-15-24.png)

Once you click on the button, you will see a slightly different view that makes it easier to move the cards to another
backlog bucket. 

![Project Tutorial - Backlog - Move Cards to Bucket](/assets/moving/sc.2021-05-08.18-15-27.png)

Just drag 'n drop the card you want to the bucket you want. We will move the cards to the proper bucket after a some 
extra thoughts in our project.

![Project Tutorial - Backlog - Move Card to Bucket](/assets/moving/sc.2021-05-08.18-15-46.png)

![Project Tutorial - Backlog - Move Card 2 to Bucket](/assets/moving/sc.2021-05-08.18-16-27.png)

Click on the `Move Cards to Buckets` button again to return to normal view to continue working as usual.

![Project Tutorial - Backlog - Normal view](/assets/moving/sc.2021-05-08.18-16-36.png)

## Sprints (Scrum based projects)
As described in the [Scrum Guide](https://www.scrumguides.org){:target="_blank"}, 
`Sprints` are the heartbeat of Scrum, where ideas are turned into value. Sprints are time-boxed iterations, 
no longer than one month and most commonly two weeks.  

A sprint in Flying Donut has the following states:
1. **Pending**: A sprint is not started, thus is in pending state, even if the start date is past.
1. **Started**: A sprint has been started, thus is active. Active sprints show up in the dashboard.
1. **Completed**: A sprint has been completed, thus is done.

![Project Tutorial - Sprints List](/assets/moving/sc.2021-05-08.18-32-41.png)

### Creating a Sprint
In our case, we will create a sprint for each of the project's phases:
- Before the move
- Move days
- After the move

Locate the `+` button in the upper right corner,
in the sprints page. Add a name, a description (with your sprint goal), and start and end dates. Don't worry if you 
don't know the dates yet. You can change them later on.

![Project Tutorial - Create Sprint](/assets/moving/sc.2021-05-08.18-19-04.png)

Once we are done creating the sprints, we see a timeline with our sprints, according to the start and end dates.

![Project Tutorial - Sprints](/assets/moving/sc.2021-05-08.18-22-56.png)

We used May 22nd to 29th as the move dates, so the sprints before and after the move are marked accordingly.
Notice that when you are setting up your own project, you do not have to specify the dates if you are not
sure of them. Dates are used to order the sprints in the sprints page. They are also used in the project
summary pages and charts, to provide information whether the project is on track or behind schedule.

In the Sprint List, you will see among other things, depending on the start and end dates,
and if the sprint has started, is completed or not:

1. The sprint has started and have a number of days left.
1. The sprint is overdue.
1. The sprint is done.
1. The sprint will start in number of days.

### Adding Cards to the Sprint

Now that we have a list of cards (work items), we can add them to our sprints. What needs to be done 
before the move? What should we remember to do during the moving day? What can wait until after the move?

Click on the `Plan` button in the "Before the Move" sprint, to see this sprint's planning view.

![Project Tutorial - Sprints - Plan button](/assets/moving/sc.2021-05-08.18-23-11.png)

In the sprint planning view, you see two distinct areas:
- Backlog
- Sprint Board

Drag 'n drop the cards from the selected backlog bucket into the sprint. 
  
![Project Tutorial - Sprints - Plan](/assets/moving/sc.2021-05-08.18-23-23.png)

Once you drop the card, the view will be updated with the counters.

![Project Tutorial - Sprints - Plan](/assets/moving/sc.2021-05-08.18-23-29.png)

Of course the burndown chart will also be updated after a few seconds, when you add cards with estimated tasks. 
When you add tasks and estimate them in the cards, the burndown chart will also be updated in real-time.

![Project Tutorial - Sprints - Plan](/assets/moving/sc.2021-05-08.18-23-34.png)

Let's add the rest of the cards that we need in this sprint.

![Project Tutorial - Sprints - Plan](/assets/moving/sc.2021-05-08.18-24-16.png)

![Project Tutorial - Sprints - Plan](/assets/moving/sc.2021-05-08.18-25-21.png)

We have cards on multiple backlog buckets, therefore to add cards from a different backlog bucket we need to click 
on the `Select Bucket` button, to pick the bucket we want. Let's select the "New House" bucket to pick the cards that
we will work on in this sprint. 

![Project Tutorial - Sprints - Plan](/assets/moving/sc.2021-05-08.18-25-53.png)

Let's add the cards we need in this sprint.

![Project Tutorial - Sprints - Plan](/assets/moving/sc.2021-05-08.18-26-05.png)

Let's see if we need to bring something else form the "Kids Stuff" bucket.

![Project Tutorial - Sprints - Plan](/assets/moving/sc.2021-05-08.18-27-03.png)

Let's bring the last card to the sprint.

![Project Tutorial - Sprints - Plan](/assets/moving/sc.2021-05-08.18-27-18.png)

### Starting a Sprint

When you are done adding the cards to the sprint, you `Start` it (when the time comes). Locate the `Start` button 
at the toolbar of the sprint.

![Project Tutorial - Sprints List - start button](/assets/moving/sc.2021-05-08.18-19-44.png)

You will be presented with the start sprint modal. You need to provide the start and end dates to start the sprint.
Then just click on the `Start Sprint` button, to start it.

![Project Tutorial - Start sprint modal](/assets/moving/sc.2021-05-08.18-19-55.png)

Once you start the sprint you will se an indication with the `Days Left` and the sprint will be visible in the dashboard.

![Project Tutorial - Sprints](/assets/moving/sc.2021-05-08.18-21-41.png)

### Completing a Sprint
When the sprint has been completed, you need to `Complete` it (when the time comes). Locate the `Complete` button
at the toolbar of the sprint. You will be presented with the start sprint modal. Uncompleted cards will be moved
to a sprint (pending or active) or a backlog bucket. Once selected, just click on the `Comlete Sprint` button. 

![Project Tutorial - Sprints](/assets/moving/sc.2021-05-08.18-58-32.png)

![Project Tutorial - Sprints](/assets/moving/sc.2021-05-08.18-58-49.png)


## Sprints and Boards
To navigate to the sprint board click on the `name` of the sprint, or find the `Board` button located at the toolbar
of each sprint and click it.

![Project Tutorial - Sprints - Name Hover](/assets/moving/sc.2021-05-08.18-32-41.png)

## SCRUM Sprint Board
There are cases where you don't want or need a modern kanban board to run sprints in. In simple traditional scrum,
you prioritize your cards vertically, and you only move the tasks of a card in the task board. When all tasks are done, 
then the card is considered done.

### Add Card
To add a card find the `+` button located at the toolbar, and click on it. 

![Project Tutorial - SCRUM Board - Add Card](/assets/moving/sc.2021-05-08.18-32-56.png)

When you click on the button, an input field appears. Simply type the name of the card in the input text box, 
and hit `Enter` or click on the `Add Card` button.  

![Project Tutorial - SCRUM Board - Add Card typing](/assets/moving/sc.2021-05-08.18-33-06.png)

You can add as many items as you can think of. Remember that these are higher level work items, that we can break 
down into smaller tasks later.

![Project Tutorial - SCRUM Board - Card Created](/assets/moving/sc.2021-05-08.18-33-16.png)

### Prioritize

The cards can be moved around in board via drag ‘n drop. The order from top to bottom is used to order the priority 
of each card. 

Click on the card and start dragging until you find the position you want.

![Project Tutorial - SCRUM Board - Card Reorder](/assets/moving/sc.2021-05-08.18-33-53.png)

Then release the drag and leave it at the desired position.

![Project Tutorial - SCRUM Board - Card Reordered](/assets/moving/sc.2021-05-08.18-34-04.png)

### Task Board - Expanded Card
In the simple SCRUM board we can expand the cards to reveal some details of the card. Among the 
details is the task board.

Click on the `Expand Card` icon located in the left corner of the card.

![Project Tutorial - SCRUM Board - Expand Hover](/assets/moving/sc.2021-05-08.18-34-13.png)

The task board, and the description is visible in the board.

![Project Tutorial - SCRUM Board - Expanded](/assets/moving/sc.2021-05-08.18-34-08.png)

The only columns available for the tasks are `To Do`, `Doing`, `Done`. You will be able to drag the tasks and drop
them in the proper column. Once all tasks are done the card will be considered as done.

![Project Tutorial - SCRUM Board - Move Task](/assets/moving/sc.2021-05-08.18-34-58.png)

### Add Tasks - Expanded Card
To add a task find the `+` button located at the top of the column in the task board, and click on it.

![Project Tutorial - SCRUM Board - Tasks - Hover](/assets/moving/sc.2021-05-08.18-39-54.png)

When you click on the button, an input field appears. Simply type the name of the task in the input text box, 
and hit `Enter` or click on the `Add Task` button.

![Project Tutorial - SCRUM Board - Tasks - Add](/assets/moving/sc.2021-05-08.18-40-09.png)

Reorder the tasks based on priority order. We will start working with tasks at the top, and since we want to talk to
Suzan first, we will move it at the top.

![Project Tutorial - SCRUM Board - Tasks - Reorder](/assets/moving/sc.2021-05-08.18-40-24.png)

### Add Labels - Card
To add clarity to your boards, add labels to the cards. With the use of labels, you get an extra layer of information 
at a glance.

From the dropdown menu of the card locate and click on the `Labels` action.

![Project Tutorial - SCRUM Board - Expanded - Select Labels](/assets/moving/sc.2021-05-08.18-35-20.png)

The labels menu is visible. Select the labels of the card and close the menu with a click anywhere outside the menu 
or the `x` button at the right upper corner of the menu.

![Project Tutorial - SCRUM Board - Expanded - Show Labels](/assets/moving/sc.2021-05-08.18-35-30.png)

The menu stays open until you chose to close it.

![Project Tutorial - SCRUM Board - Expanded - Show Labels - Select](/assets/moving/sc.2021-05-08.18-35-36.png)

The labels are visible in the expanded card, to give clarity to your boards.

![Project Tutorial - SCRUM Board - Expanded - Label Added](/assets/moving/sc.2021-05-08.18-35-44.png)

The labels are visible in the collapsed card, to give clarity to your boards.

![Project Tutorial - SCRUM Board - Collapsed](/assets/moving/sc.2021-05-08.18-35-56.png)

### Edit Card Description
We can edit the card description with more details when expanded. Locate the `Pencil` button when hover over 
the description. The markdown editor will be visible. Click on the `Save Changes` button or press `Ctrl+Enter` to 
save the changes.

![Project Tutorial - SCRUM Board - Expanded - Next - Edit description](/assets/moving/sc.2021-05-08.18-37-15.png)

The description is visible in when the card is expanded.

![Project Tutorial - SCRUM Board - Expanded - Next - Saved description](/assets/moving/sc.2021-05-08.18-37-26.png)

### View the Burndown Chart
Let's check the burndown chart now that we added a few tasks to see how it looks like now. Locate the `Burndown Chart`
button at the board toolbar located in the top right-hand side of the board, and click on it.

![Project Tutorial - SCRUM Board - Tasks - Reorder](/assets/moving/sc.2021-05-08.18-40-48.png)

The burndown chart view is visible now.

![Project Tutorial - SCRUM Board - Tasks - Reorder](/assets/moving/sc.2021-05-08.18-40-52.png)

## SCRUMBAN Sprint Board

Let say that we changed our mind, and we want to use `SCUMBAN` instead. We need to chang the project type. 

### Change Project Board Type
Locate the project `Settings` button at the left-side menu and click on it. Then select the `Admin` tab.
The `Admin` tab is only available to project administrators or the project owner. 

Locate the change board type option and click on the `Change` button.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-01-35.png)

We see what is selected, and the available options we can choose of.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-01-41.png)

Let's select the `SCRUMBAN` option to change the project board type.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-01-47.png)

Once the project type is changed, we have the option to edit and modify the columns of our board. 
Locate the `Columns` section, just bellow the `Board Type`, and click on the `Edit` button.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-02-03.png)

The edit board columns modal will be visible to do all necessary changes. As we see, we have by default 4 columns:
- To Do
- Doing
- Testing
- Done

Each column has the following properties:
- **Name**: The name of the column.
- **WIP**: Limiting Work In Progress in a kanban board encourages higher quality and more excellent 
  performance. The act of restricting WIP helps you optimize work capacity by allowing you to pull new work only 
  if capacity is available. 
- **Type**: The type of the column. A column can be a `to do`, `doing`, or `done` column. Cards in a column will get
  the status of the column, that is taken into account in the available counters and reports. 

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-02-09.png)

In our project we don't have a `Testing` column so let's delete it.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-02-20.png)

Until we hit the `Save Changes` button, the changes will not be applied to the project. Let's save the changes to apply
them to our board.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-02-46.png)

### Scrumban Board

From the sprint list navigate to the sprint board. Now the board has the columns as modified.

![Project Tutorial - Project Settings - Scrumban Board](/assets/moving/sc.2021-05-08.19-03-06.png)

We start working on the "Moving Budget" card, so let's add the card to the doing column. Now we have 2 cards 
in the `Doing` column.

![Project Tutorial - Project Settings - Scrumban Board](/assets/moving/sc.2021-05-08.19-03-06.png)

Let's filter the board to show only the cards that I'm working on.

![Project Tutorial - Project Settings - Scrumban Board](/assets/moving/sc.2021-05-08.19-03-51.png)

![Project Tutorial - Project Settings - Scrumban Board](/assets/moving/sc.2021-05-08.19-03-56.png)

![Project Tutorial - Project Settings - Scrumban Board](/assets/moving/sc.2021-05-08.19-04-08.png)

![Project Tutorial - Project Settings - Scrumban Board](/assets/moving/sc.2021-05-08.19-04-54.png)

![Project Tutorial - Project Settings - Scrumban Board](/assets/moving/sc.2021-05-08.19-05-01.png)


## KANBAN Board

Let say that we changed our mind, and we want to use `KANBAN` instead. We need to chang the project type.

### Change Project Board Type
Locate the project `Settings` button at the left-side menu and click on it. Then select the `Admin` tab.
The `Admin` tab is only available to project administrators or the project owner.

Locate the change board type option and click on the `Change` button.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-01-35.png)

We see what is selected, and the available options we can choose of.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-24-59.png)

Let's select the `KANBAN` option to change the project board type.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-25-21.png)

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-25-50.png)
![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-25-55.png)
![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-26-50.png)


Once the project type is changed, we have the option to edit and modify the columns of our board.
Locate the `Columns` section, just bellow the `Board Type`, and click on the `Edit` button.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-02-03.png)

The edit board columns modal will be visible to do all necessary changes. As we see, we have by default 3 columns:
- To Do
- Doing
- Done

Each column has the following properties:
- **Name**: The name of the column.
- **WIP**: Limiting Work In Progress in a kanban board encourages higher quality and more excellent
  performance. The act of restricting WIP helps you optimize work capacity by allowing you to pull new work only
  if capacity is available.
- **Type**: The type of the column. A column can be a `to do`, `doing`, or `done` column. Cards in a column will get
  the status of the column, that is taken into account in the available counters and reports.

Since we are running a kanban board, we will create the workflow of our project in our board instead of 
using sprints. Let's rename the `To Do` column into `Before the Move`.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-27-18.png)

Create a column `Move Days`.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-27-37.png)

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-27-59.png)

Move it after the `Before the Move` column. We will keep it before the `Doing` column.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-28-16.png)

Change the `Type` to `To Do`. This way we will know that every card in this column is in a *to do* state.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-28-23.png)

Create a column `After the Move`, and change the `Type` to `To Do`. 

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-28-42.png)

Move it after the `Move Days` column. We will keep it before the `Doing` column.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-28-48.png)

Now we have a board with all the phases in place to start working. Save the changes to apply the new board layout to 
the project.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-29-17.png)


### Kanban Board

From the left-hand side menu, navigate to the project board. The board has the columns as modified.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-29-30.png)

Let's bring the cards we want from the backlog in our board. Click on the `plan` button located at the right-hand side
of the top menu.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-30-00.png)

In the planning view, you see two distinct areas:
- Backlog.
- Board with all `To Do` columns available.

Drag 'n drop the cards from the selected backlog bucket into the board.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-30-29.png)

## Card is Blocked (Impediments)
Anything that stops or slows down the delivery, or acts as a hurdle can be termed as a blocker or impediment.
Blockers can manifest themselves at any time, and pretty much anything gets blocked sooner or later, especially 
in the software development life cycle.

In Flying Donut we have the option to mark a card as blocked. It’s visible in the board and therefore transparent for 
everyone involved. From the dropdown menu of the card locate and click on the `Block` action.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-30-42.png)

The card will be marked as blocked, with a red border around the card, and a special 'Blocked' label.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.19-30-47.png)

## Labels

One of the simplest ways to add structure, and clarity to your boards, is by adding labels to the cards. With the use 
of labels, you get an extra layer of information at a glance.

Locate the project `Settings` button at the left-side menu and click on it. Then select the `Labels` tab.
The `Labels` tab is available to all project members.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.13-51-31.png)

### Create Label
Click on the `Create Label` button. A label form will be available to add the new label. Type in the `name` of the label
and select the color of the label. Click on the `Save Label` button to apply the changes.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.13-51-49.png)

Let's create the labels we need for our project.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.13-53-39.png)

### Backlog Buckets as Labels
In case we want to know from which backlog bucket card was added in our board (scrum or kanban), then we have the option 
to enable it from the labels section. Locate the `Backlog Buckets` section at the top of the labels and click on 
the toggle button `Disbled` to enable it.

![Project Tutorial - Labels Disabled button](/assets/moving/sc.2021-05-08.13-53-55.png)

When enabled we see the backlog buckets in the labels list. We have the option to edit the color of these labels just 
as we would with any normal label. 

![Project Tutorial - Labels Enabled](/assets/moving/sc.2021-05-08.13-56-14.png)

--- 

## The Dashboard

After you start working on a project, and assign tasks to yourself to work on, the project Dashboard
gives you a quick glimpse into your activities, and your work in progress. The dashboard shows the active sprints, 
and the kanban boards

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.23-24-44.png)

Click on the `Show All` button that is visible, when you have more cards assigned to you. All cards you have some 
work assigned to do, will be visible to you.

![Project Tutorial - Project Settings - Board type](/assets/moving/sc.2021-05-08.23-24-48.png)