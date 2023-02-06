---
title: Password verification has been temporarily suspended due to a brownout. please use a personal access token instead
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can use a personal access token instead of a password to authenticate in Git during a brownout.
---

**Contents**

[TOC]

# Setting Up a Personal Access Token
1. Log into your Git account and select **Settings** from the drop-down menu.
2. Select **Developer Settings** from the left-hand menu.
3. Select **Personal Access Tokens** from the left-hand menu.
4. Select **Generate New Token**.
5. Enter a token description and select the appropriate scopes.
6. Select **Generate Token**.

# Using the Personal Access Token
1. Open the Git command line.
2. Enter the following command to set the username and personal access token: 
`git config --global user.name "your_username"`
`git config --global user.token "your_personal_access_token"`
3. Enter the following command to authenticate the personal access token: 
`git credential-osxkeychain get`
4. Enter the personal access token when prompted.
5. Your personal access token should now be authenticated and you can use it to access your Git repositories.
