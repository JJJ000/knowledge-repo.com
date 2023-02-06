---
title: Clone a repository from github using https and two-factor authentication
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To clone a repository from GitHub over https with two-factor authentication, use the command `git clone https//<username>@github.com/<username>/<repository>.git` with your GitHub username and the repository name.
---

**Contents**

[TOC]

# Section 1: Generating a Personal Access Token

In order to clone a repository from GitHub with two-factor authentication, you will need to generate a [Personal Access Token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line).

# Section 2: Cloning the Repository

Once the Personal Access Token has been generated, you can use it to clone the repository from GitHub over HTTPS. 

The command to use is:

```
git clone https://<username>:<personal_access_token>@github.com/<username>/<repository>.git
```

# Section 3: Storing the Token

It is important to store the Personal Access Token in a safe place, as it is the only way to access the repository.

# Section 4: Updating the Token

It is also important to keep the token up-to-date, as it may expire or be revoked. To update the token, simply generate a new one and use it in the command to clone the repository.
