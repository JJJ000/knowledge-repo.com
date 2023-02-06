---
title: Create a complete backup of a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To fully backup a git repo, use the `git clone --mirror` command to clone the repo and all of its branches and tags.
---

**Contents**

[TOC]

## Cloning the Repository

The first step in backing up a git repo is to clone the repository. This can be done by running the following command:

`git clone <repository-url>`

This will create a local copy of the repository on your computer.

## Storing the Repository

Once you have cloned the repository, you should store it in a safe location. This could be an external hard drive, USB drive, or cloud storage service.

## Updating the Repository

It is important to regularly update your backup of the repository. This can be done by running the following command:

`git pull`

This will fetch any new changes from the remote repository and update your local copy.

## Automating the Backup

You can also automate the backup process by setting up a cron job. This will ensure that your backup is regularly updated and you don't have to manually run the `git pull` command.
