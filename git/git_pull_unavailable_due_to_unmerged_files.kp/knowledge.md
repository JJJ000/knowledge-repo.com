---
title: Why does git indicate that a pull cannot be performed due to unresolved changes?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git requires all files to be merged before a pull can be performed in order to prevent data loss or conflicts.
---

**Contents**

[TOC]

### Overview 
When running a git pull command, git may throw an error that reads "Pull is not possible because you have unmerged files". This error occurs when there are conflicts between local and remote versions of a file, which can happen when multiple people are working on the same file. 

### Conflict Resolution
In order to fix this error, users must resolve the conflicts between the local and remote versions of the file. This can be done by manually editing the file, using a merge tool, or using the git mergetool command. Once the conflicts have been resolved and the file has been saved, the user can run the git add command to add the file to the staging area.

### Final Steps
After the file has been added to the staging area, the user can run the git commit command to commit the changes. Finally, the user can run the git pull command again to pull the changes from the remote repository. 

### Conclusion
Pulling is not possible when there are unmerged files because the conflicts must be resolved before the pull can be completed. By manually editing the file, using a merge tool, or using the git mergetool command, users can resolve the conflicts and pull the changes from the remote repository.
