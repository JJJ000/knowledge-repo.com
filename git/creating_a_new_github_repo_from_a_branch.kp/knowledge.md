---
title: How can I make a new github repository from a branch in an existing repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a new branch from the existing repo, then push the branch to a new GitHub repository.
---

**Contents**

[TOC]

# 1. Create a New Branch
1. Open the existing repository in GitHub. 
2. Select the branch you want to create the new repository from. 
3. Click the "branch" button in the top right corner of the page. 
4. Enter a name for the new branch. 
5. Click the "Create branch" button. 

# 2. Push the New Branch to GitHub
1. Open the command line and navigate to the directory of the existing repository. 
2. Run the command `git push origin <branch_name>` to push the new branch to GitHub.

# 3. Create a New Repository
1. Navigate to the GitHub homepage. 
2. Click the "+" icon in the top right corner of the page. 
3. Select "New repository" from the dropdown menu. 
4. Enter a name for the new repository. 
5. Select the branch you created in Step 1 as the default branch. 
6. Click the "Create repository" button. 

# 4. Push the Existing Repository to the New Repo
1. Open the command line and navigate to the directory of the existing repository. 
2. Run the command `git remote set-url origin <new_repo_url>` to set the new repository as the remote repository. 
3. Run the command `git push -u origin master` to push the existing repository to the new repository.
