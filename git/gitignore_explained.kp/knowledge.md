---
title: What does .gitignore do?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: .gitignore is a file that tells Git which files or directories to ignore when committing changes.
---

**Contents**

[TOC]

# What is .gitignore?

## Definition

`.gitignore` is a file in a Git repository that specifies which files and directories should be ignored when committing changes. It is useful for preventing certain files from being committed to the repository, such as configuration files, compiled binaries, and sensitive information.

## Purpose

The purpose of `.gitignore` is to ensure that certain files and directories are not committed to the repository. This is especially useful for preventing sensitive information from being accidentally committed. It also allows developers to keep certain files and directories out of version control, such as compiled binaries and configuration files.

## Syntax

`.gitignore` files use a simple syntax for specifying which files and directories should be ignored. Each line in the file specifies a pattern for files to ignore, and Git will ignore any files or directories that match the specified patterns.
