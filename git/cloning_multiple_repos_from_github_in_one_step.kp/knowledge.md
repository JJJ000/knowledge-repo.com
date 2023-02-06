---
title: What is the most efficient way to clone multiple repositories from github at once?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Using the GitHub API, you can clone all repos at once by making a GET request to the /user/repos endpoint.
---

**Contents**

[TOC]

# Cloning all repositories from GitHub

## Step 1: Install the hub command-line tool
The first step is to install the `hub` command-line tool. This tool is a wrapper for the git command-line tool, and it provides additional commands for interacting with GitHub. To install hub, follow the instructions on the official GitHub page: https://github.com/github/hub.

## Step 2: Get a list of all your repositories
Once you have installed the hub command-line tool, you can use it to get a list of all your repositories on GitHub. To do this, run the following command:

`hub api user/repos`

This will return a list of all your repositories in JSON format.

## Step 3: Clone all your repositories
Once you have a list of all your repositories, you can use the `hub clone` command to clone them all at once. To do this, run the following command:

`hub clone <repository-list>`

where `<repository-list>` is the list of repositories returned by the `hub api user/repos` command.

## Step 4: Update all your repositories
Finally, you can use the `hub pull-all` command to update all your repositories at once. To do this, run the following command:

`hub pull-all`

This will pull any new changes from all your repositories.
