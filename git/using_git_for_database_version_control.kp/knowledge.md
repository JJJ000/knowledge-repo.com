---
title: What steps do I need to take to version control a database with git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can put a database under version control by using a database version control system such as Flyway, Liquibase, or Redgate`s SQL Source Control.
---

**Contents**

[TOC]

### Step 1 - Export Database

First, you need to export the database into a file format that can be tracked by git. This can be done using a database management tool such as MySQL Workbench or by using a command line tool such as mysqldump.

### Step 2 - Initialize Git Repository

Next, you need to create a local git repository and commit the exported database file to it. This can be done by running the following commands:

```git
git init
git add database.sql
git commit -m "Initial commit"
```

### Step 3 - Push to Remote Repository

Finally, you need to push the local repository to a remote repository such as GitHub. This can be done by running the following commands:

```git
git remote add origin <remote repository URL>
git push -u origin master
```

### Step 4 - Update Database

As you make changes to the database, you can commit them to the git repository using the same commands as before. This will allow you to keep track of all changes to the database over time.
