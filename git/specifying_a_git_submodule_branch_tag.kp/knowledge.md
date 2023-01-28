---
title: What is the syntax for specifying a branch or tag when adding a git submodule?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: When adding a Git submodule, specify the branch/tag with the `--branch` or `--tag` option.
---

**Contents**

[TOC]

1. Setting the Branch/Tag in the `.gitmodules` File
    - Open the `.gitmodules` file in your project's root directory
    - Add the `branch` or `tag` option to the relevant submodule entry
    - Specify the branch/tag name as the value of the option
    - Save and close the `.gitmodules` file

2. Updating the Submodule
    - Run the command `git submodule update --init --recursive`
    - This will update the submodule to the specified branch/tag

3. Committing the Changes
    - Run `git add .gitmodules` to stage the changes
    - Run `git commit -m "Updated submodule to <branch/tag name>"` to commit the changes

4. Pushing the Changes
    - Run `git push origin <branch name>` to push the changes to the remote repository
