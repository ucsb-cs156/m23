---
title: team02a
desc: "Team Project: Spring Boot Backend, part 2 (authenticated CRUD, Liquibase)"
assigned: 2023-07-21 09:00
due: 2023-08-21 11:59
github_org: ucsb-cs156-m23
layout: lab
layout: default
parent: lab
num: team02
nav_order: 202
ready: true
num_issues: 35
starter: https://github.com/ucsb-cs156-m23/STARTER-team02
---

# NOTICE
# NOTICE
# NOTICE
# NOTICE
# NOTICE
# NOTICE
# NOTICE
# NOTICE

This file is for an independent study by Matt Prison who is revising team02 to incorporate Liquibase database migrations.

This is not the assignment that was given in M23, but rather a prototype for a future version of this assignment.

{% include drop_down_style.html %}

## Your Project Boards

Here are your project boards for team02.  

For team02, the Kanban board is populated by the staff before you start using the Github Actions workflow [`99-team02.yml`](
{{page.starter}}/blob/main/.github/workflows/99-team02.yml); if your Kanban is not yet populated,
please check in with the staff.  You should see around {{page.num_issues}} issues on the board in the ToDo column when you start.

<!-- 
| Team | Project Board|
|------|--------------|
| f22-5pm-1 | <https://github.com/orgs/ucsb-cs156-f22/projects/13> |
| f22-5pm-2 | <https://github.com/orgs/ucsb-cs156-f22/projects/14> |
| f22-5pm-3 | <https://github.com/orgs/ucsb-cs156-f22/projects/15> |
| f22-5pm-4 | <https://github.com/orgs/ucsb-cs156-f22/projects/16> |
| f22-6pm-1 | <https://github.com/orgs/ucsb-cs156-f22/projects/17> |
| f22-6pm-2 | <https://github.com/orgs/ucsb-cs156-f22/projects/18> |
| f22-6pm-3 | <https://github.com/orgs/ucsb-cs156-f22/projects/19> |
| f22-6pm-4 | <https://github.com/orgs/ucsb-cs156-f22/projects/20> |
| f22-7pm-1 | <https://github.com/orgs/ucsb-cs156-f22/projects/21> |
| f22-7pm-2 | <https://github.com/orgs/ucsb-cs156-f22/projects/22> |
| f22-7pm-3 | <https://github.com/orgs/ucsb-cs156-f22/projects/23> |
| f22-7pm-4 | <https://github.com/orgs/ucsb-cs156-f22/projects/24> |
-->

| Team | Project Board|
|------|--------------|
| m23-9am-1 | <https://github.com/orgs/{{page.github_org}}/projects/9> |
| m23-9am-2 | <https://github.com/orgs/{{page.github_org}}/projects/10> |
| m23-9am-3 | <https://github.com/orgs/{{page.github_org}}/projects/11> |
| m23-10am-1 | <https://github.com/orgs/{{page.github_org}}/projects/12> |
| m23-10am-2 | <https://github.com/orgs/{{page.github_org}}/projects/13> |
| m23-10am-3 | <https://github.com/orgs/{{page.github_org}}/projects/14> |
| m23-10am-4 | <https://github.com/orgs/{{page.github_org}}/projects/15> |


## Big Picture: what is team02 all about?

From a high-level standpoint, you'll be resolving these issues:

Set up Tasks (once per team):

* Setting up a Repo with prod deployment on Dokku
* Setting up a Repo with qa deployment on Dokku

Coding Tasks: 
* Adding 4 to 5 database tables (one per team member)
* Adding database migration files for each of the new tables
* Setting up CRUD (Create, Read, Update, Destroy) operations for each of those tables
* Adding backend test coverage for all of that

For this assignment, we are still dealing directly with the backend via Swagger.

In the next assignment, we'll start looking how how to build a proper front end for the types of things we did in both team01 and team02.

# More details on team02

In this team project, our starter code has a frontend and backend, however we are still focusing only on the backend part.  The front end provides only a place for us to login with our Google account so that we
can authenticate before doing CRUD operations.

We are focusing on learning these new Spring Boot backend concepts:

* Creating SQL database tables using `@Entity` and `@Repository`
* Utilizing Changelog files to describe changes to the database
* Using the Lombok annotations: `@Data`, `@NoArgsConstructor`, `@Builder`, etc.
* Implementing controller routes for CRUD operations (Created, Read, Update, Destroy)
* Writing unit tests for controller CRUD operations, including the use of:
  - Spring `MockMvc`
  - Mockito methods for creating mocks of repositories and services (`when`, `verify)
  - the idea of "dependency injection"

In addition, we'll practice further with a few concepts that we touched on in `jpa03`, but may not have fully fleshed out:
- Set up of the documentation via Github Pages
- Working with feature branches, issues, a Kanban board, pull requests, and GitHub actions scripts
- Working with code coverage and mutation testing

## The starting code

Your starter code at <{{page.starter}}> provides Spring Boot code with the ability to do CRUD operations on two database tables:

* UCSBDates
* UCSBDiningCommons

These tables are set up to match the data that is available through two public APIs that are provided by UCSB and documented at
<https://developer.ucsb.edu>.

The `UCSBDates` tables has three columns, and is intended to store data like that shown here:


The `UCSBDiningCommons` table has six columns, and is intended to store data like that shown here:


## Your task: add CRUD for additional database tables


You'll be adding CRUD operations for six additional database tables; one per team member:

Here are the six tables you'll be adding (one per person).

On the Kanban board, you'll find five issues for each of these tables:

* Add database table (the `@Entity` and `@Repository` classes, no test classes)
* Add GET endpoint to list all database records, and a POST  endpoint to create new database records, plus tests (this, and all of the rest, are done in the Controller and Controller test classes)
* Add GET endpoint to get a single database row by its id. (plus tests)
* Add PUT endpoint to update a single database row by its id. (plus tests) 
* Add DELETE endpoint to delete a single database row by its id. (plus tests)

You should choose one of these database tables, and then assign yourself the five issues that pertain to that database table.

As you look over these, note that some of them use an *autogenerated `Long`* as the `@Id` field, while others use a different field
already in the data.  That may not make any sense to you right now, but there is an explanation immediately following the list of database tables.  
We'll also go over this in lecture.
   
### (1) UCSB Dining Commons Menu 

<details>
  
<summary>
For details on the UCSB Dining Commons Menu database table, click the triangle
</summary>

The `UCSBDiningCommonsMenuItem` will use an autogenerated `Long` as its `id` field, and will have these additional columns:

* `String diningCommonsCode`
* `String name`
* `String station`

Here are some sample values:

| id | diningCommonsCode | name | station |
|----|-------------------|------|---------|
| 1  | ortega            | Baked Pesto Pasta with Chicken | Entree Specials |
| 2  | ortega            | Tofu Banh Mi Sandwich (v)  | Entree Specials |
| 3  | ortega            | Chicken Caesar Salad  | Entrees |
| 5  | portola            | Cream of Broccoli Soup (v) | Greens & Grains |

</details>  
  
### (2) UCSB Organization

<details>
<summary>
For details on the UCSB Organization database table click the triangle
</summary>


The `UCSBOrganization` table will use the `orgCode` field (a String) as its `@Id` field, and will have these columns:

* String orgCode
* String orgTranslationShort
* String orgTranslation
* boolean inactive

Here are some sample values:

| orgCode | orgTranslationShort | orgTranslation | inactive |
|----|-------------------|------|---------|
| ZPR | ZETA PHI RHO | ZETA PHI RHO | false |
| SKY | SKYDIVING CLUB | SKYDIVING CLUB AT UCSB | false |
| OSLI | STUDENT LIFE | OFFICE OF STUDENT LIFE | false |
| KRC | KOREAN RADIO CL | KOREAN RADIO CLUB | false |

</details>


### (3) Recommendation Request

<details>
<summary>
For details on the Recommendation request database table click the triangle
</summary>


The `RecommendationRequest` table will use an autogenerated  `Long` as its `@Id` field, and will have these additional fields:

* String requesterEmail
* String professorEmail
* String explanation
* LocalDateTime dateRequested
* LocalDateTime dateNeeded
* boolean done
  

Here are some sample values:
  
| id | requesterEmail | professorEmail | explanation | dateRequested | dateNeeded | done |
|-|-|-|-|-|-|-|
| 1 | cgaucho@ucsb.edu | phtcon@ucsb.edu | BS/MS program | 2022-04-20 | 2022-05-01 | false |
| 2 | ldelplaya@ucsb.edu | richert@ucsb.edu | PhD CS Stanford | 2022-05-20 | 2022-11-15 | false |
| 3 | ldelplaya@ucsb.edu | phtcon@ucsb.edu | PhD CS Stanford | 2022-05-20 | 2022-11-15 | false |
| 4 | alu@ucsb.edu | phtcon@ucsb.edu | PhD CE Cal Tech | 2022-05-20 | 2022-11-15 | false |

</details>


### (4) Menu Item Review

<details>
<summary>
For details on the Menu Item Review database table click the triangle
</summary>


The `MenuItemReview` table will use an autogenerated  `Long` as its `@Id` field, and will have these additional fields:

* Long itemId (the id in the UCSBDiningCommonsMenuItem table of a menu item)
* String reviewerEmail (the email of the reviewer)
* int stars (0 to 5 stars)
* LocalDateTime dateReviewed
* String comments  

Here are some sample values:
  
| id | itemId | reviewerEmail | stars | dateReviewed | comments | 
|-|-|-|-|-|-|-|
| 1 | 27 | cgaucho@ucsb.edu | 3 | 2022-04-20 | bland af |
| 2 | 29 | cgaucho@ucsb.edu | 5 | 2022-04-20 | best apple pie ever |
| 3 | 29 | ldelplaya@ucsb.edu | 0 | 2022-04-21 | not tryna get food poisoning, but if I were this would do it|

</details>


### (5) Help Request

<details>
<summary>
For details on the Help Request database table click the triangle
</summary>


The `HelpRequest` table will use an autogenerated `Long` as its `@Id` field, and will have these additional fields:

* String requesterEmail
* String teamId
* String tableOrBreakoutRoom
* LocalDateTime requestTime
* String explanation
* boolean solved
  
  
Here are some sample values:
  
| id |  requesterEmail | teamId | tableOrBreakoutRoom | requestTime | explanation | solved  |
|-|-|-|-|-|-|-|
| 1 | cgaucho@ucsb.edu | s22-5pm-3 | 7 | 2022-04-20T17:35 | Need help with Swagger-ui | false | 
| 2 | ldelplaya@ucsb.edu | s22-6pm-3 | 11 | 2022-04-20T18:31 | Dokku problems | false | 
| 3 | pdg@ucsb.edu | s22-6pm-4 | 13 | 2022-04-21T14:15 | Merge conflict  | false | 
  
</details>


### (6)  Articles

<details>
<summary>
For details on the Articles database table click the triangle
</summary>


The `Articles` table will use an autogenerated `Long` as its `@Id` field, and will have these additional fields:

* String title 
* String url 
* String explanation
* String email (of person that submitted it)
* LocalDateTime dateAdded
  
  
Here are some sample values:
  
| id | title | url | explanation | email | dateAdded | 
|-|-|-|-|-|-|
| 1 | Using testing-playground with React Testing Library | https://dev.to/katieraby/using-testing-playground-with-react-testing-library-26j7 | Helpful when we get to front end development | phtcon@ucsb.edu | 2022-04-20 |
| 2 | Handy Spring Utility Classes | https://twitter.com/maciejwalkowiak/status/1511736828369719300?t=gGXpmBH4y4eY9OBSUInZEg&s=09 | A lot of really useful classes are built into Spring | phtcon@ucsb.edu | 2022-04-19|
  
</details>

### Two types of id values

Every database table has a *primary key* marked in a Spring Boot `@Entity` class with the annotation `@Id`.

This value must be unique in the database table; no two rows can have the same primary key.

There are two strategies for dealing with this requirement:

1. Autogenerated ids, which start at `1` and then increment automatically.   The `UCSBDate` entity in the starter code is an example.  The code looks liek this:

   ```
   @Id
   @GeneratedValue(strategy = GenerationType.IDENTITY)
   private long id;
   ```
   
   As an aside: you may wonder what happens when we run out of numbers.  Since these `id` numbers are typically stored in a 64-bit Java `Long`, the maximum number is: `9,223,372,036,854,775,807L`.   
   * If you stored 1 Million records per second, 24 hours a day, 7 days a week, it would take you [292 thousand years](https://www.google.com/search?q=9%2C223%2C372%2C036%2C854%2C775%2C807+%2F+1000000+%2F+60+%2F+60+%2F+24+%2F+365&rlz=1C5CHFA_enUS888US889&sxsrf=APq-WBtGUMS1ceirZg3u9OrjxeaktzoWaw%3A1643567397963&ei=Jdn2Yen0Oc3EkPIP3du9gA4&ved=0ahUKEwipm63Xjdr1AhVNIkQIHd1tD-AQ4dUDCA4&uact=5&oq=9%2C223%2C372%2C036%2C854%2C775%2C807+%2F+1000000+%2F+60+%2F+60+%2F+24+%2F+365&gs_lcp=Cgdnd3Mtd2l6EANKBAhBGAFKBAhGGABQ4w1Y9A9gxxZoAXAAeACAAZcBiAGYA5IBAzAuM5gBAKABAcABAQ&sclient=gws-wiz) to cycle through this many id numbers.  
   * That's also over 18,000 records for every square meter on the face of the planet earth.  Not sure what database table needs that many records.

   
2. Using a value already in the data that is inherently unique.  For example, we might use perm number as an id field for a table of students.

   The `UCSBDiningCommons` entity in the sample code shows an example, where the `code` field is guaranteed to be unique; no two dining commons
   will have the same `code` value:
   
   ```
   @Id
   private String code;
   ```
   
It is important to understand that when you set up an `@Repository` class, the types that you pass to `CRUDRepository` as shown below must match the type of the `@Entity` and the type of the `@Id` field, as in these examples:

1. `UCSBDateRepository` uses `CrudRepository<UCSBDate, Long>` because the `@Id` field of `UCSBDate` is a `Long`:

    ```
    @Repository
    public interface UCSBDateRepository extends CrudRepository<UCSBDate, Long> {
    ...
    ```
   
2. `UCSBDiningCommonsRepository` uses `CrudRepository<UCSBDate, String>` because the `@Id` field of `UCSBDiningCommons` is a `String`:

    ```
    @Repository
    public interface UCSBDiningCommonsRepository extends CrudRepository<UCSBDiningCommons, String> {
    ...
    ```
   
As you look over your database table description above, take note of which of these applies to you.


## What you'll do: Process

From a process standpoint, this project works the same as team01:


Here's how that will play out in detail:
1. To start, each of you should clone your team's `team02-teamname` repo, which should already have a Kanban board set up for it.
2. On the team's Kanban board, there should be two types of issues:
   * Ones that pertain to a particular database table
   * Ones that are global to the entire team
4. First, divide up the set up tasks among the members of the team, and assign each of those to a team member.   Leave them in the "to do" column, though, until you actually start working on the issue.
5. Then, divide up the six database tables among the team members.  I suggest that you do this on your team slack channel in a single post, and then "pin" that post to your channel.
   That post might look something like this:

   ```
   Adam:  Articles
   Brianna: Menu Item Review
   Chris:  Help Request
   Danny: Recommendation Request
   Erin: UCSB Organization
   Fay: UCSB Dining Commons Menu
   ```
   
6. Now look on the Kanban board.  You should find that there are five issues on the Kanban board for your specific database table:   
   
   * create_database_table
   * add_list_all_and_post_endpoints
   * add get for single item
   * add put for single item
   * add delete for single item 

   You should find all of the stories for your database item, and assign them to yourself; but drag *only one* into the In Progress column (and if you are already assigned to one of the set up tasks, don't even drag that one yet!  
   
   Typically, you should be assigned to only one item at a time in the In Progress column.  The exception is if you drag an item to In Progress, make some progress on it, and then need to stop working on it for a while because you are blocked, or something else urgently needs your attention.  But that should be the exception, not the normal way of doing things.
   
7. Now work on your issues as you did in team01; dragging them to "In Review" once they are ready for code review, and to "Done" when they are merged.
8. Near the end of the project there are a few "clean up tasks" for your team.    Those are marked as such on the Kanban board.   One of the last of those is to submit on Gauchospace for your team to note that your team is ready for the work to be graded.



# Getting started

To get started:

* Clone your team's team02 
* Add the <{{page.starter}}> repo as a remote called starter
  <p>
  <tt>git remote add starter {{page.starter}} </tt>
  </p>
  This is in case there are updates to the starter code that you need to pull from by doing:
  ```
  git pull starter main
  git push origin main
  ```
* Then you are ready to start by making your first branch, something like `Chris-RecRequestTable`
  ```
  git checkout -b Chris-ReqRequestTable
  ```


### Implement CRUD operations for a database table


To add an SQL database table in Spring Boot, you typically add two files:

* A Java class that is annotated with `@Entity`; each instance of this class represents a single row in the database table
* A Java class that is annotated with `@Repository`; each instance of this class represents a database table.

There is more information in the issues on the Kanban board to guide you through the rest of the process.

# More Hints

We may add more hints about working with the team02 code as we discover what
problems studnets run into.

In the meantime, use the `#help-team02` channel to ask questions.

# A note about open source

Note that this assignment is open source.

The repos are public *on purpose*.
* You are encouraged to consult with one another within and across teams where it helps
  your learning.
* That does not mean that you can cheat by just copying code from another team.
* You are *not* permitted to just look at another team's code, even though you "can".
* It does mean that you should try to solve the problems as best you can, but you may 
  consult with members of other teams as you work.  In that context, you may look at 
  other team's code.

This isn't hard.   You all *know* when you are are looking at other team's work to
try to learn, versus when you are just looking at it as a shortcut to learning.

I'm trusting you to do the right thing.   This is practice for when, later on, you are
all working on different assignments.

# Understanding how to create the `@Entity` class


For example of `@Entity` classes, consult these files in the starter code:

* [UCSBDate.java](https://github.com/ucsb-cs156-s22/STARTER-team02/blob/main/src/main/java/edu/ucsb/cs156/example/entities/UCSBDate.java)
* [UCSBDiningCommons.java](https://github.com/ucsb-cs156-s22/STARTER-team02/blob/main/src/main/java/edu/ucsb/cs156/example/entities/UCSBDiningCommons.java)


You'll see that these files have a particular structure, with these annotations:

UCSBDate.java:

```
@Data
@AllArgsConstructor
@NoArgsConstructor
@Builder
@Entity(name = "ucsbdates")
public class UCSBDate {
```

UCSBDiningCommons.java:

```
@Data
@AllArgsConstructor
@NoArgsConstructor
@Builder
@Entity(name = "ucsbdiningcommons")
public class UCSBDiningCommons {
```

What do these annotations do?

* `@Data` is an annotation from a package called [Lombok](https://projectlombok.org/).  Lombok automatically generates code for some of the tedious things
   that can be automated: getters, setters, `toString`, `hashCode` and `equals`.  It also implements a constructor for all "required arguments", though that one is not always very convenient to use if we have lots of fields.
* `@AllArgsConstructor` and `@NoArgsConstructor` are additional [Lombok](https://projectlombok.org/) annotations that define additional constructors for us.  The  `@NoArgsConstructor` is particularly important, since it's a requirement of many pieces of Java Software that classes implement a no-args constructor (it's part of what it means to be a *Java Bean*.)
* `@Builder` create a class and some methods that make it easy to build objects with a syntax like this:
  ```
  UCSBDiningCommons commons = UCSBDiningCommons.builder()
        .name("Carrillo")
        .code("carrillo")
        .hasSackMeal(false)
        .hasTakeOutMeal(false)
        .hasDiningCam(true)
        .latitude(34.409953)
        .longitude(-119.85277)
        .build();
  ```
* `@Entity(name = "ucsbdiningcommons")` is the annotation that says this will be a row in a database table; the parameter sets the name of the table.

With these annotations in place, it's a simple matter of defining private fields for each of the columns in the database table.


# Details: `@Repository` class

For the repository class, see the examples:

* [UCSBDateRepository](https://github.com/ucsb-cs156-s22/STARTER-team02/blob/main/src/main/java/edu/ucsb/cs156/example/repositories/UCSBDateRepository.java)
* [UCSBDiningCommonsRepository](https://github.com/ucsb-cs156-s22/STARTER-team02/blob/main/src/main/java/edu/ucsb/cs156/example/repositories/UCSBDiningCommonsRepository.java)


Note that these are both `interface` files and not classes.

Normally, if you  create an `interface`, you also need to create a  class that implements that interface.

However, Spring Boot will *automatically generate the code for you*.  

In addition, if you need certain kinds of queries, you can specify methods in your interface to implement those queries.

The rules for translating method naming conventions into 
generated code are complicated: we will not go over all of them in lecture, and you are not expected to memorize or learn them all, and
*you probably won't need that for this assignment* (though you may need to know it later in the course.)

In any case, if/when you do need to understand that, here is some documentation is here to help get you started: <https://docs.spring.io/spring-data/jdbc/docs/current/reference/html/#jdbc.query-methods>

# Details: Liquibase Database Migrations

Using Liquibase migrations allows you to make changes to your database tables without having to restart the entire database.
Liquibase allows you to describe changes to the database schema and it uses those descriptions to apply changes to it.
The changes can be described in JSON and are stored in `src/resources/db/migration/changelog/changes`.
Each file is a description of the database changes to each of the defined entities.
The key here is consistency, always create the database changelog file after you create a new entity or modify it.

The example for the changelog files can be found in these files:

* [UCSBDates](https://github.com/MPriston/STARTER-team02/blob/main/src/main/resources/db/migration/changelog/changes/UCSBDates.json)
* [UCSBDiningCommons](https://github.com/MPriston/STARTER-team02/blob/main/src/main/resources/db/migration/changelog/changes/UCSBDiningCommons.json)

Each of the change JSON files are structured the same way:
```
{"databaseChangeLog: [
  {
    "changeSet": {
      "id": "1697389100055-2",
      "author": "author",
      "preConditions": [
            {
              "onFail": "MARK_RAN"
            },
            {
              "not": [
                {
                  "tableExists": {
                    "tableName": "MY_NEW_TABLE"
                  }
                }
              ]
            }
          ],
      "changes: [{
              "createTable": {
                "columns": [
                  {
                    "column": {
                      "constraints": {
                        "primaryKey": true,
                        "primaryKeyName": "CONSTRAINT_2"
                      },
                      "name": "CODE",
                      "type": "VARCHAR(255)"
                    }
                  },
                  {
                    "column": {
                      "constraints": {
                        "nullable": false
                      },
                      "name": "HAS_DINING_CAM",
                      "type": "BOOLEAN"
                    }
                  }]
                ,
                "tableName": "MY_NEW_TABLE"
              }]
    }
  }
]}
```
`databaseChangeLog` is the beginning of every change file, it holds a list of changeSets that will describe changes to the database

`changeSet` is one of the changes held by `databaseChangeLog` it holds 3 items:

`id`: this field holds a unique id to the change set it can be any number you want as long as it is unique across all change files not just this specific one

`author`: this field holds the author of the `changeSet`

`changes`: this field holds a list of the changes that are to be applied in this specific change set, for a complete list of possible database changes check [Liquibase](https://docs.liquibase.com/change-types/home.html)

## Commands to be used with Liquibase

### Check changes to database
```
mvn liquibase:updateSQL
```
This command will show the changes that will be applied when following the change log you described. This will not apply the changes just provide you with a way to inspect it

### Apply chnages to database
```
mvn liquibase:update
```
This command will apply the changes to the database. The changes will also be applied when you start your application so you wont need to update it before starting the app.

### Sync database to changelog
```
mvn liquibase:changelogSync
```
This command will make all the changes you currently have be marked as applied already, this is useful when working on a database that already exists, when you don't want for example to create a table that already exists.

### Tagging a version of the database
```
mvn liquibase:tag --tag=myTag
```
This can be used to mark a version of the database that can be used when doing rollbacks

### Rollback to tag
```
mvn liquibase:rollback --tag=myTag
```
This command can be used to rollback the database to a previousily marked tag

## Preconditions
```
"changeSet": {
    "preConditions": [
      {
        "onFail": "MARK_RAN"
      },
      {
        "not": [
          {
            "tableExists": {
              "tableName": "MY_NEW_TABLE"
            }
          }
        ]
      }
    ]
    "changes": etc
    }
``` 
Preconditions can be set in each of the changes that will help you determine if certain change should be ran or what to do if it fails.

The example above tells liquibase to mark a change as ran in case it fails because the table already exists, very useful when working with an already existing database.

For more information on preconditions you can see [Preconditions](https://docs.liquibase.com/concepts/changelogs/preconditions.html)
  
# Details: Controller methods and tests

The examples for the Controller Methods are tests are in these files:

* Controllers:
  - [UCSBDatesController.java](https://github.com/ucsb-cs156-s22/STARTER-team02/blob/main/src/main/java/edu/ucsb/cs156/example/controllers/UCSBDatesController.java)
  - [UCSBDiningCommonsController.java](https://github.com/ucsb-cs156-s22/STARTER-team02/blob/main/src/main/java/edu/ucsb/cs156/example/controllers/UCSBDiningCommonsController.java)
* Controller Tests:
  - [UCSBDatesControllerTests.java](https://github.com/ucsb-cs156-s22/STARTER-team02/blob/main/src/test/java/edu/ucsb/cs156/example/controllers/UCSBDatesControllerTests.java)
  - [UCSBDiningCommonsControllerTests.java](https://github.com/ucsb-cs156-s22/STARTER-team02/blob/main/src/test/java/edu/ucsb/cs156/example/controllers/UCSBDiningCommonsControllerTests.java)

You should be able to find the code you need for each of the methods, and use it as a model to create the code for your database table.

If you need additional guidance, ask on the `#help-team02` channel, and we'll try to steer you in the right direction.


# When you are done

When all branches are merged to main, all tasks on Kanban board in the done column, please submit on Canvas.

For now, there is no Gradescope autograder for team02; it will be graded manually.

If that changes, we'll let you know.
