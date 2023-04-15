---
title: What is the process for deleting a gitlab project?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To remove a Gitlab project, use the `Remove Project` button in the project`s settings page.
---

**Contents**

[TOC]

### Remove Project from Gitlab
1. Log into your Gitlab account.
2. Go to the project you would like to remove.
3. Click on the Settings tab at the top.
4. Select the Advanced tab on the left side.
5. Scroll down to the bottom and click on the "Remove project" button.

### Remove Project from Repository
1. Open the terminal window and navigate to the project directory.
2. Run the command `git remote rm origin` to remove the project from the repository.

### Remove Project from Local Machine
1. Open the terminal window and navigate to the project directory.
2. Run the command `rm -rf <project-name>` to delete the project from your local machine.

### Clean Up
1. Open the terminal window and navigate to the project directory.
2. Run the command `git gc` to clean up any loose objects and optimize the repository.
