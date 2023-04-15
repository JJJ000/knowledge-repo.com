---
title: Fetch the most recent updates for all git submodules
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git submodule update --remote --merge` to pull the latest changes for all git submodules.
---

**Contents**

[TOC]

### Step 1: Navigate to the Root Directory

Change your working directory to the root directory of your project. This is the directory that contains all the submodules.

### Step 2: Pull Latest Changes

Run the following command to pull the latest changes for all submodules:

`git submodule foreach git pull origin master`

### Step 3: Commit the Changes

Once all the changes have been pulled, you need to commit the changes to the root repository. To do this, run the following command:

`git commit -am "Updated all submodules"`

### Step 4: Push the Changes

Finally, push the changes to the remote repository by running the following command:

`git push origin master`
