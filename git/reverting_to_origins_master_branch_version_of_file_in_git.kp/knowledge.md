---
title: What is the process for reverting to the original version of a file in the master branch of the repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Checkout the file from the master branch, or reset the file to the master branch`s version.
---

**Contents**

[TOC]

### Step 1: Checkout the Master Branch

First, you need to checkout the master branch. This will ensure that you are on the correct branch and have the most up-to-date version of the file. To do this, run the following command:

`git checkout master`

### Step 2: Reset the File

Next, you need to reset the file to the version that is in the master branch. To do this, run the following command:

`git reset --hard origin/master <file>`

### Step 3: Commit the Reset

Finally, you need to commit the reset. This will ensure that the changes are saved to the repository. To do this, run the following command:

`git commit -m "Reverted to master branch's version of <file>"`
