---
title: Clone a github repository using an oauth access token
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: GitHub Clone with OAuth Access Token allows a user to securely clone a repository from GitHub using an OAuth Access Token.
---

**Contents**

[TOC]

# Introduction
GitHub provides a feature to clone a repository using an OAuth Access Token. This feature allows users to securely clone a repository without having to store their GitHub username and password. This guide will explain how to clone a repository with an OAuth Access Token. 

# Requirements
In order to clone a repository with an OAuth Access Token, the user must have:
- A GitHub account
- An OAuth Access Token
- Git installed on their machine

# Step by Step Instructions
1. Log in to your GitHub account.
2. Go to Settings -> Developer Settings -> Personal Access Tokens.
3. Generate a new token with the “repo” scope.
4. Copy the token to your clipboard.
5. Open a terminal window and navigate to the directory where you want to clone the repository.
6. Type `git clone https://<token>@github.com/<username>/<repository>.git`
7. Enter the token when prompted.
8. The repository will be cloned to your local machine.

# Conclusion
Cloning a repository with an OAuth Access Token is a secure way to clone a repository without having to store your GitHub username and password. By following the steps outlined in this guide, you will be able to clone a repository with an OAuth Access Token.
