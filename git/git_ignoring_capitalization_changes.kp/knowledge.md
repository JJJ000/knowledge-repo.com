---
title: I altered the capitalization of a folder and git does not appear to recognize the change
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git does not recognize changes in capitalization when tracking files.
---

**Contents**

[TOC]

##Cause

Git is case sensitive and will not recognize the directory as the same if the capitalization is changed. 

##Solution

1. Rename the directory back to its original name.
2. Add the renamed directory to the Git repository.
3. Commit the changes to the repository.
4. Push the changes to the remote repository.
