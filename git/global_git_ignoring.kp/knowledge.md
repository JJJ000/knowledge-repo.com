---
title: Global git exclusion
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: A global Git ignore is a file that can be used to ignore certain files or patterns across all local repositories.
---

**Contents**

[TOC]

### Introduction 
Gitignore files are used to tell Git which files or folders to ignore when committing code to a repository. Global Gitignore files are used to define rules that apply across multiple repositories and users.

### Purpose
The purpose of global Gitignore files is to help maintain consistency across repositories and users. This is especially helpful in multi-user and multi-repository environments, such as open source projects. By having a single global Gitignore file, developers can ensure that the same files are ignored across all repositories and users.

### How to Use 
To use a global Gitignore file, it must first be created and stored in the user’s home directory. The file should be named .gitignore_global and should contain the rules for which files should be ignored. Once the file is created, it must be configured in Git. This can be done by running the git config --global core.excludesfile command.

### Conclusion
Global Gitignore files are a useful tool for maintaining consistency across repositories and users. They can help ensure that the same files are ignored across all repositories and users, making it easier to manage projects in multi-user and multi-repository environments.
