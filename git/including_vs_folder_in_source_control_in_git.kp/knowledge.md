---
title: Should I include the visual studio 2015 .vs folder in my version control system?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: No, the Visual Studio 2015 .vs folder should not be added to source control in Git.
---

**Contents**

[TOC]

####No 

The .vs folder contains Visual Studio specific configuration files and should not be added to source control. This folder is usually excluded from source control by default.

####Why

The .vs folder contains files that are specific to the local environment, such as the user's settings, which can vary from machine to machine. Adding this folder to source control can lead to conflicts and errors when other developers attempt to pull the changes.

####Solution

The best solution is to exclude the .vs folder from source control by adding it to the .gitignore file. This will ensure that the folder is not added to the repository, and any changes made to the folder will not be tracked.
