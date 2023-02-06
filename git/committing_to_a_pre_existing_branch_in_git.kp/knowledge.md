---
title: How to push changes to an existing branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Checkout the branch you want to commit changes to and then commit your changes as usual.
---

**Contents**

[TOC]

### Step 1: Checkout the Branch

Checkout the branch to which you would like to commit changes. This can be done using the following command:

`git checkout <branch_name>`

### Step 2: Make Changes

Make the necessary changes to the project. This can be done using any text editor.

### Step 3: Add Changes to the Stage

Add the changes to the stage by using the following command:

`git add <file_name>`

### Step 4: Commit Changes

Commit the changes to the branch by using the following command:

`git commit -m "<your_commit_message>"`
