---
title: How to install bower using only https?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `bower install --allow-root --config.interactive=false -o -H https//` in Git to bower install using only https.
---

**Contents**

[TOC]

# Section 1: Install Bower

1. Download and install Node.js from [https://nodejs.org/en/download/](https://nodejs.org/en/download/).

2. Install Bower using the command `npm install -g bower`.

# Section 2: Setup Git

1. Initialize a Git repository in the folder where you want to store your project files by running the command `git init`.

2. Add the remote repository URL to your local repository using the command `git remote add origin <url>`.

# Section 3: Install Packages

1. Install packages using the command `bower install --save <package-name>`.

2. Checkout the packages from the remote repository using the command `git checkout <package-name>`.

# Section 4: Push to Remote Repository

1. Commit the changes to the local repository using the command `git commit -m "message"`.

2. Push the changes to the remote repository using the command `git push origin master`.
