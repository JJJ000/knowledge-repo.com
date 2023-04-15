---
title: What is the process for adding a git submodule to a sub-directory?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git submodule add <repo-url> <sub-directory>`.
---

**Contents**

[TOC]

### Step 1: Add the Submodule

Run the following command from the root of your project:

`git submodule add <repository> <path>`

Where `<repository>` is the URL of the repository you want to add as a submodule, and `<path>` is the path to the sub-directory where you want to add the submodule.

### Step 2: Commit the Changes

Run the following command to commit the changes:

`git commit -m "Added submodule <repository> to <path>"`

### Step 3: Push the Changes

Run the following command to push the changes to the remote repository:

`git push origin master`

### Step 4: Update the Submodule

Run the following command to update the submodule:

`git submodule update --init --recursive`
