---
title: What is the procedure for locating a commit in a git repository using its message?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can search a Git repository by commit message using the `git log --grep` command.
---

**Contents**

[TOC]

### Using the Command Line 
1. Navigate to the directory of the repository you want to search. 
2. Use the command `git log --grep="<commit message>"` to search the repository for the commit message. 

### Using GitHub
1. Navigate to the repository page on GitHub. 
2. Click on the "Commits" tab. 
3. Enter the commit message in the search bar. 

### Using a GUI
1. Download and install a Git GUI client (e.g. SourceTree). 
2. Open the repository in the GUI. 
3. Use the search bar to search the repository for the commit message. 

### Using the GitHub API
1. Make a GET request to the `/search/commits` endpoint of the GitHub API. 
2. Pass the commit message as a query parameter. 
3. Parse the response to get the commit history.
