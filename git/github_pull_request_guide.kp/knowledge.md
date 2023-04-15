---
title: What is the process for submitting a github pull request?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To do a GitHub pull request, you must create a branch off of the base branch, make your changes, commit them, and then open a pull request to have your changes reviewed and merged.
---

**Contents**

[TOC]

### Step 1: Fork the Repository

If you do not have access to push to the repository, you will need to fork the repository. To do this, go to the repository you would like to contribute to and click the "Fork" button in the top right corner. This will create a copy of the repository under your own username.

### Step 2: Clone the Repository

Once you have forked the repository, you will need to clone it to your local machine. To do this, select the "Clone or download" button on the repository page and copy the URL. Then, open a terminal window and type `git clone <url>` where `<url>` is the URL you copied.

### Step 3: Create a New Branch

Once you have cloned the repository, you will need to create a new branch to make your changes on. To do this, type `git checkout -b <branch_name>` in the terminal window. This will create a new branch with the name you specified and switch to it.

### Step 4: Make Your Changes

Now that you have created a new branch, you can make your changes to the code. When you are done, you will need to add, commit, and push your changes. To do this, type `git add <files>` to add the files you have changed, `git commit -m <message>` to commit your changes with a message, and `git push origin <branch_name>` to push your changes to the branch.

### Step 5: Create the Pull Request

Once your changes have been pushed to the branch, you can create a pull request. To do this, go to the repository page and click the "Compare and pull request" button. This will open a new page where you can review your changes and submit the pull request.
