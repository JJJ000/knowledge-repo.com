---
title: What is the process for granting permission for an oauth app to create or update a workflow when pushing to git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Grant the OAuth App the necessary permissions to create or update workflows.
---

**Contents**

[TOC]

## Step 1: Create a Personal Access Token
1. Log into your GitHub account.
2. In the top right corner, click your profile photo and select **Settings**.
3. In the left sidebar, click **Developer settings**.
4. In the left sidebar, click **Personal access tokens**.
5. Click **Generate new token**.
6. Enter a token description.
7. Select the scopes for the token.
8. Click **Generate token**.

## Step 2: Configure Git to Use the Token
1. In the terminal, enter `git config --global user.name "Your Name"`.
2. In the terminal, enter `git config --global user.email "your_email@example.com"`.
3. In the terminal, enter `git config --global github.token "your_token_here"`.

## Step 3: Push the Changes
1. In the terminal, enter `git push origin master`.
2. The changes should now be pushed to GitHub without the OAuth App error.
