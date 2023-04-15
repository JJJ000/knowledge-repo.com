---
title: What is the new name of the folder when cloning from github?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The name of the folder can be changed by using the `--directory` option when cloning from GitHub.
---

**Contents**

[TOC]

### Cloning a Repository

When you clone a repository from GitHub, you are creating a local copy of the project on your computer. This allows you to make changes and commits to the project without affecting the original repository.

### Renaming a Folder

Once you have cloned the repository, you can rename the folder if you wish. This can be done by right-clicking on the folder and selecting “Rename”. You can then enter the new name for the folder.

### Updating the Local Repository

After you have renamed the folder, you will need to update the local repository to reflect the new name. This can be done by opening the terminal and navigating to the folder. Then, run the command “git remote set-url origin <new repository URL>”. This will update the local repository to the new folder name.

### Committing Changes

Once you have updated the local repository, you can commit the changes to the original repository. This can be done by running the command “git push origin master”. This will push the changes to the original repository and the folder name will be updated.
