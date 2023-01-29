---
title: Adding git hooks to a repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git hooks can be added to a repository by adding them to the repository`s .git/hooks directory.
---

**Contents**

[TOC]

### Step 1: Create a Folder for the Hooks

In the root of the repository, create a folder named `.git/hooks/`.

### Step 2: Add Hook Scripts

Add the hook scripts to the newly created `.git/hooks/` folder. The scripts should be named according to the particular hook they are associated with. For example, a pre-commit hook should be named `pre-commit`.

### Step 3: Make Scripts Executable

Make sure the scripts are executable by running the `chmod +x` command on each script.

### Step 4: Test Hooks

Test the hooks by making a commit and verifying that the hooks are running correctly.
