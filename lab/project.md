---
title: project
desc: "Legacy Code Project instructions"
assigned: 2023-08-15 14:00
due: 2023-08-25 11:59
github_org: ucsb-cs156-m23
layout: lab
layout: default
parent: lab
num: project
nav_order: 300
m23_9am_1: https://github.com/orgs/ucsb-cs156-m23/projects/55
m23_9am_2: https://github.com/orgs/ucsb-cs156-m23/projects/52
m23_9am_3: https://github.com/orgs/ucsb-cs156-m23/projects/54
m23_10am_1: https://github.com/orgs/ucsb-cs156-m23/projects/57
m23_10am_2: https://github.com/orgs/ucsb-cs156-m23/projects/53
m23_10am_3: https://github.com/orgs/ucsb-cs156-m23/projects/56
m23_10am_4: https://github.com/orgs/ucsb-cs156-m23/projects/51
proj_courses_slack_url: tbd
proj_happycows_slack_url: https://ucsb-cs156-s23.slack.com/archives/C058QUC16QP
proj_gauchoride_slack_url: https://ucsb-cs156-s23.slack.com/archives/C0595EWELLA
---

# The Assignment, Briefly.

In this project:

* You will be assigned a legacy code base, and a set of issues 
  (new features, refactorings, bug fixes)
* The list of issues contains more work than we expect you will need to complete
  in order to get a perfect score on the project, so don't worry that you have
  to finish them all; *you do not have to finish them all*.
* Each issue you complete earns points for your team after it is:
  * code reviewed and approved by a member of your team that didn't work on it
  * code reviewed and approved by a member of the course staff (instructor, TA, LA)
  * merged into the main branch of your repo.
* Issues earn different numbers of points: typically, 5, 10 or 20 depending on 
  the complexity of the issue (more on this below).
* There may be a few issues that are marked as "must do".  You *must
  complete these* or their point values will be subtracted from the points you
  earn. These are assigned point values in advance.  
* For other issues,
  points are assigned after completion. If you want to ask for a point
  estimate, you may do so, but keep in mind that actual points can differ
  from estimated points.
* Unlike in previous team projects, where your Issues list and 
  Kanban board may have been
  pre-populated with issues by the staff,
  in the legacy code phase, populating the Kanban board
  is the responsibility of the team.  More on that below.
* The aim of the team is to earn 100 points before the deadline.  This forms the 
  most important part of you project grade, which is 25% of your course grade.
* Another part of your project grade is your "CATME multiplier", which is a number
  based on your peer evaluations.  This number is typically 100 unless your team
  has rated you significantly below the team average
* Points beyond 100 can count as extra credit as explained below.

# Points beyond 100


If you accumulate more than 100 project points, the additional points may count as extra credit, at a rate of 1 extra credit point for each 10 points over 100 earned, up to a maximum project grade of 110.  For example:

| Points Earned | Project Grade |
|---------------|---------------|
|    80         |    80         |
|    90         |    90         |
|   100         |  100          |
|   105         |  100.5        |
|   110         |  101          |
|   115         |  101.5        |
|   150         |  105          |
|   180         |  108          |
|   ≥200        |  110          |

Your final project grade is maxed out at 110 total project points--any points in excess of 110 will not count towards your grade (though you'll probably learn a lot from having under taken the work to earn them.)


# Sprint Planning for Legacy Code project

Each team already has a Kanban board setup for the legacy code project (see links below).   However unlike in your team01, team02, and team03 projects, it's up to you to populate this yourself.

| 9am | 10am | 
|-----|-----|
| [m23-9am-1]({{page.m23_9am_1}}) | [m23-10am-1]({{page.m23_10am_1}}) | 
| [m23-9am-2]({{page.m23_9am_2}}) | [m23-10am-2]({{page.m23_10am_2}}) | 
| [m23-9am-3]({{page.m23_9am_3}}) | [m23-10am-3]({{page.m23_10am_3}}) | 
|                         | [m23-10am-4]({{page.m23_10am_4}}) | 


You should add the `In Review` column if it is not already present.

Then, you should populate your todo column with issues, start assigning them to your team, and start working.   I'll cover where these issues come from in a moment.

You may not get through all of the Sprint planning today, but by the end of discussion section on Wednesday:
* Each of the six team members should be assigned to an issue in the todo column
* The previous bullet point shoudl *remain true* until your team reaches 100 points

Teams accumulate points when PRs are merged into main
* That is only done by the course staff for these projects.
* Each PR requires at least one code review from a team member, and at least one code review from a staff member
* The staff estimate points. Most issues are 5 to 10 points.
  - 5 points for very straightforward issues addressing a single concern
  - 10 points for issues that require a bit more work, but are nevertheless reasonably straightforward application of skills from team01, team02, team03.
  - 20 points is rare, and is reserved for issues that may be more complex, and/or require students to go significantly beyond the skills from previous course assignments.
* Note that breaking down issues into smaller chunks works to your benefit in multiple ways:
  - Easy to code review and merge (fewer merge conflicts), so faster point accumulation
  - Three 10 points issues and three 5 points issues adds up to 45 points; combining all of those together might only get you 20.
  - But the aim here should not be to "game the points". It should be to "get the issues implemented", in incremental "right sized" pieces.
  - If you do that, the points will take care of themselves.  
  
Points belong to the whole team, not to individuals
* Work as a team, and help each other.
* We do want to see every team member contribute
* Ultimately, it's a team project and a team grade.
* Having said that, really low CATME scores might result in a grade reduction.
 
  
## Where do issues come from?

For issues, you'll need to do a bit more work that in the previous team projects.

Here is where you'll get issues from:
* The three starter code repos have issues lists (as shown in the table below).
* These have been copied to your repo
* These issues come in different sizes 
  - A handful of these may be small easy issues. 
  - However, many (most?) of these issue *may not translate one-to-one into issues for your Kanban board*.
  - Instead, you are encouraged to try to *break the larger ones down into smaller issues*, each of which could be a single PR; more on this below.
  - This Sprint Planning meeting is where you can do some of that.
  - You may even need to add "issues about issues", e.g. an issue that says: "break issue #34 from proj-happycows into multiple issues on our team's repo".  Such an issue doesn't result in a PR, but it can still be moved across the Kanban board from `To Do`, to `In Progress`, to `In Review`, to `Done`.
* Your team's own ideas for features, based on the notes your team took last Wednesday during meetings with
  - Mike Fogelsanger for proj-gauchoride
  - Prof. Mattanjah deVries for proj-happycows
  <!-- - Prof. Phill Conrad for proj-courses -->

## What are User Stories?  

A **user story** is a story about how a user (of some specified role) interacts with your application to achieve a certain goal.

It is phrased in the form:
* As a *name of role*
* I can *description of interaction with app*
* So that *description of goal*

The purpose of user stories is to constantly remind us as developers that our work should be grounded in *helping users acheive their goals*, not in 
"adding features to an app".   The features need to the serve the larger purpose of the user (e.g. being a good farmer in the cows game, getting a ride somewhere on campus, finding a course to take). 

Typically, when adding a new feature to the app, we try to ground it in a user story.

## What is "the backlog"?

The **backlog** of a team is the collection of user stories / epics that are waiting to be worked on; when we say **backlog** we are just referring to the collection
of issues waiting for your team.

When someone says "add it to the backlog", what they mean is to create an issue in the issues list, and possible to put it on the "to do" column of the Kanban board.



## What is an Epic?

An **Epic** is a group of related user stories around some theme.   Or it may be a single user story that requires a lot of individual changes to the app, changes that may be more effective and feasible to implement and introduce into the `main` branch in stages, rather than all at once.

Some of the issues in your backlog are epics.  You will need to break them down into smaller user stories, which means **creating new issues**.

It is recommended that you:
* copy all of the relevant parts of the issue description from the epic it springs from (but *only* those parts)
* make sure that the new smaller issue has acceptance criteria
* "mention" the parent epic in the smaller issue, like this: "part of #14"; this creates a hyperlink to the epic.
* You may also want to put a comment or mention of the smaller issue(s) in the Epic description saying something like "issue #26 addresses this part"

## What does it mean to "groom the backlog"

"Groom" and "grooming" have a technical definition in the context of Agile.   It is most related to this sense of these senses of the word grooming from the [Oxford English Dictionary](https://www.oed.com/dictionary/groom_v?tab=meaning_and_use)
* "To give (a person, oneself) a clean, neat, or smart appearance; to arrange or style (one's hair, nails, clothes, etc.)
* "To make ready for a particular role, objective, etc."

In Agile, to "groom the backlog" means to groom some subset of the user stories in the backlog to make each one ready for a developer to work on. It is an essential part of Sprint Planning:

Grooming a user story includes:
* Having a discussion (often at the team level) to make sure the entire team understands the user need
* To remove any ambiguities in the issue description, and perhaps even to sketch a preliminary design of the user interface, and or implementation
* To estimate the complexity/difficulty of the story
* To make a final list of acceptance criteria

You will find that the user stories in the issues tab of your starter code are in various stages of grooming; some are completely groomed, while others
may need some work.   

More on backlog grooming:
* <https://easyretro.io/blog/what-is-story-grooming-the-ultimate-guide-to-backlog-grooming/>

## Essential: Building a shared team understanding of each story

In any case, there is one important step that has not been taken for *any* of these stories, and that is **_coming to a shared team
understanding_** about the user need, and how it will be addressed by the story.  That is a step you will need to take for *every* story you work on during
the legacy code phase.

You are **not working as individuals** but **as a team**.  Everyone on the team has an investment in the outcome of every branch and PR, so please do
take an interest in what one another is working on.

## Existing issues

Staff may add to these issues over the course of the project; when we do, we'll post an announcement in the project slack channels.

| Project |  Starter Code Repo | Issues Link | Project Slack Channel |
|---------|--------------------|-------------|-----------------------|
| proj-gauchoride | [Starter Code Repo](https://github.com/ucsb-cs156/proj-gauchoride) | [Issues](https://github.com/ucsb-cs156/proj-gauchoride/issues) | [`#proj-gauchoride`]({{page.proj_gauchoride_slack_url}}) |
| proj-happycows | [Starter Code Repo](https://github.com/ucsb-cs156/proj-happycows) | [Issues](https://github.com/ucsb-cs156/proj-happycows/issues) | [`#proj-happycows`](https://ucsb-cs156-s23.slack.com/archives/C058QUC16QP) |
<!-- | proj-courses | [Starter Code Repo](https://github.com/ucsb-cs156/proj-courses) | [Issues](https://github.com/ucsb-cs156/proj-courses/issues) |  [`#proj-courses`](https://ucsb-cs156-s23.slack.com/archives/C058BPFQZ42) | -->

## You are encouraged to keep each PR small.

For example, implementing a new feature may require
* A new React Component (with tests and storybook entries, and perhaps fixtures to support those)
* A new React Page
  - This page might start out with a simple PR that establishes a placeholder with text "New feature coming soon", and a trivial set of tests and a storybook entry
  - It might later get data from the backend and display it using a component, and be linked to from the navigation bar.
* A new database table (or a new column in an existing database table, requiring modifications to an `@Entity` and/or `@Repository` class
* New API backend endpoints, which require controller methods and tests.

Each of these could (and arguably should be) a separate PR!  This helps to keep PRs small, which makes code review easier, and also helps the team to divide up work among the team members.

Still, you may need to document in the issues what the dependencies are (e.g. "do issue 12 and 13 before starting 14").

# Legacy Code Background information

For each of the teams, there is already:
* A repo, seeded with the starter code from previous quarters
* A prod and qa dokku instance
* A Kanban board

For each, I've set up Google OAuth client id and client secret.
<!-- I've also set up the `UCSB_API_KEY` and `MONGODB_URI` for the `courses` project.   -->
You are welcome to use `dokku config:show app-name` to get these values and use them for your localhost setup.

Links are provided below.

## Optional: The icebox

Some teams will keep a column on their Kanban board (or even create a separate Kanban board) with a column called "icebox". This is a place to put stories that
you might work on some day, but not in the near future.  

You could also use "tags" for this purpose.

# Links


## 9am - gauchoride

* Customers: Mike Fogelsonger (Director of Veterans and Military Services) and Student Health (who will be taking over the application.)  Drivers, and Riders of the service.

| Team | Repo | Github Pages | Prod | QA |
|--|--|--|--|--|
| m23-9am-1 | [repo](https://github.com/ucsb-cs156-s23/proj-gauchoride-m23-9am-1) | [pages](https://ucsb-cs156-s23.github.io/proj-gauchoride-m23-9am-1/) | [prod](https://proj-gauchoride.dokku-01.cs.ucsb.edu) | [qa](https://proj-gauchoride-qa.dokku-01.cs.ucsb.edu)
| m23-9am-2 | [repo](https://github.com/ucsb-cs156-s23/proj-gauchoride-m23-9am-2) | [pages](https://ucsb-cs156-s23.github.io/proj-gauchoride-m23-9am-2/) | [prod](https://proj-gauchoride.dokku-02.cs.ucsb.edu) | [qa](https://proj-gauchoride-qa.dokku-02.cs.ucsb.edu)
| m23-9am-3 | [repo](https://github.com/ucsb-cs156-s23/proj-gauchoride-m23-9am-3) | [pages](https://ucsb-cs156-s23.github.io/proj-gauchoride-m23-9am-3/) | [prod](https://proj-gauchoride.dokku-03.cs.ucsb.edu) | [qa](https://proj-gauchoride-qa.dokku-03.cs.ucsb.edu)
| m23-9am-4 | [repo](https://github.com/ucsb-cs156-s23/proj-gauchoride-m23-9am-4) | [pages](https://ucsb-cs156-s23.github.io/proj-gauchoride-m23-9am-4/) | [prod](https://proj-gauchoride.dokku-04.cs.ucsb.edu) | [qa](https://proj-gauchoride-qa.dokku-04.cs.ucsb.edu)

 
## 10am - happycows

* Customer: Prof. Mattanjah de Vries, Distinguished Prof. of Chemistry, UCSB, and students in his classes.

| Team | Repo | Github Pages | Prod | QA |
|--|--|--|--|--|
| m23-10am-1 | [repo](https://github.com/ucsb-cs156-s23/proj-happycows-m23-10am-1) | [pages](https://ucsb-cs156-s23.github.io/proj-happycows-m23-10am-1/) | [prod](https://proj-happycows.dokku-04.cs.ucsb.edu) | [qa](https://proj-happycows-qa.dokku-04.cs.ucsb.edu) |
| m23-10am-2 | [repo](https://github.com/ucsb-cs156-s23/proj-happycows-m23-10am-2) | [pages](https://ucsb-cs156-s23.github.io/proj-happycows-m23-10am-2/) |[prod](https://proj-happycows.dokku-05.cs.ucsb.edu) | [qa](https://proj-happycows-qa.dokku-05.cs.ucsb.edu) |
| m23-10am-3 | [repo](https://github.com/ucsb-cs156-s23/proj-happycows-m23-10am-3) | [pages](https://ucsb-cs156-s23.github.io/proj-happycows-m23-10am-3/) |[prod](https://proj-happycows.dokku-06.cs.ucsb.edu) | [qa](https://proj-happycows-qa.dokku-06.cs.ucsb.edu) |
| m23-10am-4 | [repo](https://github.com/ucsb-cs156-s23/proj-happycows-m23-10am-4) | [pages](https://ucsb-cs156-s23.github.io/proj-happycows-m23-10am-4/) |[prod](https://proj-happycows.dokku-07.cs.ucsb.edu) | [qa](https://proj-happycows-qa.dokku-07.cs.ucsb.edu) |
 
<!-- ## 7pm - courses

* Customer: All UCSB Students, Faculty, Staff and Admins
* Central issues collection: <https://github.com/ucsb-cs156/proj-courses/issues>
  - You can get issues from here to add to your own kanban boards

| Team | Repo | Github Pages | Prod | QA |
|--|--|--|--|--|
| s23-7pm-1 | [repo](https://github.com/ucsb-cs156-s23/proj-courses-s23-7pm-1) | [pages](https://ucsb-cs156-s23.github.io/proj-courses-s23-7pm-1/) | [prod](https://proj-courses.dokku-09.cs.ucsb.edu) | [qa](https://proj-courses-qa.dokku-09.cs.ucsb.edu) |
| s23-7pm-2 | [repo](https://github.com/ucsb-cs156-s23/proj-courses-s23-7pm-2) | [pages](https://ucsb-cs156-s23.github.io/proj-courses-s23-7pm-2/) | [prod](https://proj-courses.dokku-10.cs.ucsb.edu) | [qa](https://proj-courses-qa.dokku-10.cs.ucsb.edu) |
| s23-7pm-3 | [repo](https://github.com/ucsb-cs156-s23/proj-courses-s23-7pm-3) | [pages](https://ucsb-cs156-s23.github.io/proj-courses-s23-7pm-3/) | [prod](https://proj-courses.dokku-11.cs.ucsb.edu) | [qa](https://proj-courses-qa.dokku-11.cs.ucsb.edu) |
| s23-7pm-4 | [repo](https://github.com/ucsb-cs156-s23/proj-courses-s23-7pm-4) | [pages](https://ucsb-cs156-s23.github.io/proj-courses-s23-7pm-4/) | [prod](https://proj-courses.dokku-12.cs.ucsb.edu) | [qa](https://proj-courses-qa.dokku-12.cs.ucsb.edu) |
  -->
