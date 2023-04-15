---
title: What is the process for relocating an existing git submodule within a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run the command `git mv <old path> <new path>` to move an existing Git submodule within a Git repository.
---

**Contents**

[TOC]

### 1. Remove the Submodule

1. Change the current working directory to the top-level directory of the Git repository.

2. Run the following command to remove the submodule: 
    ```
    git submodule deinit <path_to_submodule>
    ```
3. Run the following command to delete the submodule from the .git/config file:
    ```
    git rm --cached <path_to_submodule>
    ```

### 2. Move the Submodule

1. Move the submodule directory to the desired location within the repository.

2. Change the current working directory to the top-level directory of the Git repository.

3. Run the following command to add the submodule to the .git/config file:
    ```
    git submodule add <url_of_submodule> <new_path_to_submodule>
    ```

### 3. Update the Working Tree

1. Change the current working directory to the top-level directory of the Git repository.

2. Run the following command to update the working tree:
    ```
    git submodule update --init --recursive
    ```

### 4. Commit the Changes

1. Change the current working directory to the top-level directory of the Git repository.

2. Run the following command to commit the changes:
    ```
    git commit -m "Moved submodule to new location"
    ```
