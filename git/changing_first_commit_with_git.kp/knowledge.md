---
title: How can I modify the initial commit of my project using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: It is not possible to change the first commit of a project with Git.
---

**Contents**

[TOC]

### Introduction
Git is an open-source version control system that allows you to track changes to your project over time. It is the most popular version control system in the world and is used by millions of developers and teams.

### How to Change a Commit
When using Git, you can easily change the first commit of your project. This is done by using the "git rebase" command. This command allows you to move, edit, or delete commits in your project’s history. 

### Steps
1. Checkout the branch you want to change the first commit of.
2. Run the command `git rebase -i HEAD~<number of commits you want to change>`
3. The editor will open and you will see a list of commits
4. Change the first commit to "edit"
5. Save and close the editor
6. Make the changes you want to the first commit
7. Run the command `git commit --amend --no-edit`
8. Run the command `git rebase --continue`

### Conclusion
By following these steps, you can easily change the first commit of your project with Git. It is important to remember to always make sure to commit your changes before running the rebase command. This will ensure that your changes are properly tracked in the project history.
