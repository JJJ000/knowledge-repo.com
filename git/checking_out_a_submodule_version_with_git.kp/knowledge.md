---
title: What is the command to check out a specific version of a submodule using 'git submodule'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To check out a specific version of a submodule, run `git submodule update --init --recursive --remote <submodule path> <version>`.
---

**Contents**

[TOC]

# Checkout a Specific Version
1. Change to the root of the main project directory:
    ```
    cd <project-root>
    ```
2. Change to the submodule directory:
    ```
    cd <submodule-name>
    ```
3. Checkout the specific version:
    ```
    git checkout <version-tag>
    ```
4. Update the main project to use the specific version of the submodule:
    ```
    git submodule update --remote --merge
    ```
