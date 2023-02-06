---
title: What is the process for displaying commits since a particular commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To list commits since a certain commit, use the command `git log <commit-hash>..HEAD`.
---

**Contents**

[TOC]

## Listing Commits
1. Open the terminal or command prompt window. 
2. Change the current working directory to the local repository. 
3. Type `git log <commit-hash>..HEAD` and press enter.

## Viewing Commits
1. Type `git log --oneline` and press enter.
2. Type `git log --oneline --graph` and press enter to view a graph of commits.

## Filtering Commits
1. Type `git log --author=<name>` and press enter to view commits from a certain author. 
2. Type `git log --grep=<string>` and press enter to view commits with a certain string in the commit message.
