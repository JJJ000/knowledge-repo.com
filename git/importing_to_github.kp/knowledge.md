---
title: Upload existing source code to github
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Clone the source code repository to your local machine and push it to a new GitHub repository.
---

**Contents**

[TOC]

### Step 1: Create a Repository
1. Log in to GitHub and navigate to the main page.
2. Click on the "+" icon in the top right corner and select "New repository".
3. Enter a name for your repository and click "Create repository".

### Step 2: Upload the Source Code
1. On the repository page, click on the "Upload files" button.
2. Drag and drop the source code files into the upload window or click "Choose your files" to select them from your computer.
3. Add a commit message and click "Commit changes".

### Step 3: Push the Code to GitHub
1. Open your terminal and navigate to the local project directory.
2. Initialize a Git repository in the project directory by running the command `git init`.
3. Run the command `git remote add origin <url-of-your-github-repository>` to add the repository to your local project.
4. Run the command `git add .` to add all of the files in the project directory to the Git staging area.
5. Run the command `git commit -m "<your-commit-message>"` to commit the files to the repository.
6. Finally, run the command `git push origin master` to push the code to GitHub.
