---
title: Is it possible for me to set up multiple user profiles in my .gitconfig file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: No, only one user can be specified in the .gitconfig file.
---

**Contents**

[TOC]

Yes, you can specify multiple users for yourself in .gitconfig.

Steps:
1. Create a new user
    - Create a new user with the `git config --global user.name <name>` command.
2. Set the user email
    - Set the user email with the `git config --global user.email <email>` command.
3. Create a new identity
    - Create a new identity with the `git config --global --add user.name <name>` command.
4. Set the identity email
    - Set the identity email with the `git config --global --add user.email <email>` command.
