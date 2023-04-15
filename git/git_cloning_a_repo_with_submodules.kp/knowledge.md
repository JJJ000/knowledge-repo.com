---
title: What is the process for cloning a repository, including its submodules, using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git clone --recurse-submodules <repo-url>` to clone a repo and its submodules.
---

**Contents**

[TOC]

### Step 1: Clone the Repository

To clone the repository, run the following command in your terminal:

```git
git clone <repo_url>
```

This will create a local copy of the repository on your machine.

### Step 2: Initialize Submodules

To initialize the submodules, navigate to the repository directory and run the following command:

```git
git submodule init
```

This will initialize the submodules in the repository.

### Step 3: Update Submodules

To update the submodules, run the following command:

```git
git submodule update
```

This will update the submodules to the latest commit.

### Step 4: Pull Changes

To pull any changes to the repository, run the following command:

```git
git pull
```

This will pull any changes to the repository, including changes to the submodules.
