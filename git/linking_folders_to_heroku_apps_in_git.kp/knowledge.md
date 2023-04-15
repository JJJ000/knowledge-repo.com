---
title: What is the process for connecting a folder to an existing heroku app?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run the command `git remote add heroku <heroku-git-url>` to link the folder with the existing Heroku app.
---

**Contents**

[TOC]

1. Setup Git
----------------
* Create a new Git repository in the folder you want to link to your Heroku app
* Initialize the repository with `git init`

2. Link the Repository to Heroku
----------------
* Add the Heroku remote to the repository with `git remote add heroku <app-git-url>`
* Push the repository to the Heroku remote with `git push heroku master`

3. Verify the Link
----------------
* Check the Heroku logs with `heroku logs --tail` to verify the link was successful

4. Deploy Changes
----------------
* To deploy changes to your Heroku app, simply commit your changes and push them to the Heroku remote with `git push heroku master`
