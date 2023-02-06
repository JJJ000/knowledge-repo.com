---
title: What is the distinction between a bare and non-bare repository in terms of practical application?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A non-Bare repository contains a working directory, whereas a Bare repository does not.
---

**Contents**

[TOC]

**Bare Repository**

A bare repository is a repository that is used to store the version history of a project without the accompanying working files. It is used to share the project between multiple developers and is not meant to be used as a working copy.

**Non-Bare Repository**

A non-bare repository is a repository that contains both the version history of a project and the accompanying working files. It is used as a working copy and is meant to be used by developers to edit, commit, and push changes to the repository.

**Differences**

The main difference between a bare and non-bare repository is that a bare repository does not contain the working files, while a non-bare repository does. This means that a bare repository is not meant to be used as a working copy, while a non-bare repository is. Additionally, a bare repository is used to share the project between multiple developers, while a non-bare repository is used as a working copy.
