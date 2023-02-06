---
title: What is the process for creating shallow git submodules?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create shallow submodules by cloning with the --depth parameter.
---

**Contents**

[TOC]

## Section 1: Create the Submodule
1. Create a new repository for the submodule and push it to a remote repository. 
2. Add the submodule to the main repository with `git submodule add <url_to_submodule_repo>`

## Section 2: Make the Submodule Shallow
1. Change directory into the submodule with `cd <path_to_submodule>`
2. Make the submodule shallow with `git fetch --depth=1`

## Section 3: Push Changes
1. Add and commit the changes to the submodule with `git add` and `git commit`
2. Push the changes to the remote repository with `git push`

## Section 4: Update the Main Repository
1. Change directory back to the main repository with `cd ..`
2. Add and commit the changes to the main repository with `git add` and `git commit`
3. Push the changes to the remote repository with `git push`
