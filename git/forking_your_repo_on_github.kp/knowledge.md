---
title: What is the process for creating a duplicate of your own repository on github?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Click the `Fork` button in the top-right corner of the repository page.
---

**Contents**

[TOC]

# Step 1: Create a Fork
1. Log in to your GitHub account and navigate to the repository you would like to fork. 
2. Click the "Fork" button in the upper right corner of the repository page. 

# Step 2: Clone the Forked Repository
1. Open your terminal and navigate to the directory where you would like to store the repository. 
2. Run the command `git clone <url-of-your-forked-repo>` to clone the repository to your local machine. 

# Step 3: Configure the Remote
1. Navigate to the cloned repository directory. 
2. Run the command `git remote -v` to view the existing remote repository. 
3. Run the command `git remote add upstream <url-of-the-original-repo>` to add the original repository as the upstream remote. 

# Step 4: Syncing the Fork
1. Run the command `git fetch upstream` to fetch the latest changes from the original repository. 
2. Run the command `git checkout master` to switch to the master branch. 
3. Run the command `git merge upstream/master` to merge the changes from the original repository into your local repository.
