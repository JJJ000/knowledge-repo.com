---
title: How to deploy different local git branches to heroku's master branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To push different local Git branches to Heroku/master, use the command `git push heroku branch\_namemaster`.
---

**Contents**

[TOC]

### Setting Up a Remote

1. Log into your Heroku account and create a new app.
2. In your terminal, navigate to the directory of your local Git repository.
3. Run the command `heroku git:remote -a <app name>` (replacing <app name> with the name of your Heroku app).

### Pushing a Branch

1. Checkout the branch you want to push to Heroku.
2. Run the command `git push heroku <branch name>:master` (replacing <branch name> with the name of your local branch).

### Confirming the Push

1. Run the command `git log` to view the commits on the branch.
2. Run the command `git log --oneline` to view the commits in a single line.
3. Run the command `heroku logs --tail` to view the logs of your Heroku app.

### Deploying to Heroku

1. Run the command `git push heroku master` to push the branch to Heroku.
2. Run the command `heroku open` to open the application in your browser.
3. Run the command `heroku run rake db:migrate` to migrate the database.
