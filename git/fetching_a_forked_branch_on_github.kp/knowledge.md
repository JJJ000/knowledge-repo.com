---
title: What is the process for retrieving a branch from someone else's fork on github?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Fetch a branch from someone else`s fork on GitHub by using the `git fetch` command.
---

**Contents**

[TOC]

### Step 1: Clone the Forked Repository
In order to fetch a branch from someone else's fork, the first step is to clone the forked repository. This can be done by copying the clone URL from the forked repository and running the `git clone` command in the terminal.

### Step 2: Add the Upstream Repository
The next step is to add the upstream repository, which is the original repository from which the fork was created. This can be done by running the `git remote add upstream` command in the terminal and specifying the URL of the original repository.

### Step 3: Fetch the Upstream Repository
Once the upstream repository has been added, the next step is to fetch the upstream repository. This can be done by running the `git fetch upstream` command in the terminal.

### Step 4: Checkout the Desired Branch
Finally, the desired branch can be checked out by running the `git checkout` command in the terminal and specifying the name of the branch.
