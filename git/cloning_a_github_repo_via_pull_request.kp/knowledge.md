---
title: What is the process for cloning a repository from a pull request on github?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Cloning a repository from a pull request allows you to create a local copy of the repository and review the changes proposed in the pull request.
---

**Contents**

[TOC]

# Cloning from a Pull Request

## Overview
Cloning from a pull request allows users to create a local copy of a repository that contains the changes proposed in a pull request. This allows users to test the changes and provide feedback without making any changes to the original repository.

## Steps
1. Find the pull request you want to clone and click the "Clone or download" button.
2. Select the "Clone with SSH" option and copy the URL.
3. Open a terminal and use the `git clone` command to clone the pull request repository.
4. Check out the pull request branch by running `git checkout <branch-name>`.
5. Test the changes and provide feedback on the pull request.
