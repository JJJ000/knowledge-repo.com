---
title: Creating aliases in git to execute multiple commands and parameters
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git aliases allow users to define multiple commands and parameters in one line.
---

**Contents**

[TOC]

##### Section 1 - Multiple Commands

Git aliases allow the user to create a shortcut for a git command. This can be used for multiple commands, such as `git commit -m "message" && git push origin master`. This command would be shortened to `git alias push-commit "!git commit -m "message" && git push origin master"` and can be used by typing `git push-commit` in the command line. 

##### Section 2 - Parameters

Parameters can also be used in git aliases. For example, `git alias push-commit "!git commit -m $1 && git push origin master"` can be used to commit a message specified by the user. The user would type `git push-commit "message"` in the command line to commit the specified message. 

##### Section 3 - Multiple Parameters

Multiple parameters can also be used in git aliases. For example, `git alias push-commit "!git commit -m $1 && git push origin $2"` can be used to commit a message and push to a specified branch. The user would type `git push-commit "message" branch-name` in the command line to commit the specified message and push to the specified branch. 

##### Section 4 - Custom Aliases

Git aliases can be used to create custom commands to simplify complex git commands. For example, `git alias deploy "!git commit -m $1 && git push origin master && git push heroku master"` can be used to commit a message, push to the master branch, and deploy to Heroku. The user would type `git deploy "message"` in the command line to commit the specified message, push to the master branch, and deploy to Heroku.
