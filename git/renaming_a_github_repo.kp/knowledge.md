---
title: What is the process for changing the name of a repository on github?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To rename a repository on GitHub, go to the repository`s Settings page and change the repository name.
---

**Contents**

[TOC]

`**` Accessing the Repository**

1. Log in to your GitHub account.
2. Find the repository you want to rename.

`**` Renaming the Repository**

1. Click on the "Settings" tab of the repository.
2. Under the "Repository name" field, type the new name for the repository.
3. Click the "Rename" button.

`**` Updating Local Repository**

1. Open your terminal or command line.
2. Change the directory to the local repository.
3. Type the command `git remote set-url origin [new repository URL]`

`**` Pushing Changes to GitHub**

1. Type the command `git push -u origin master`
2. Enter your GitHub username and password when prompted.
3. You should now see the changes reflected on the GitHub repository.
