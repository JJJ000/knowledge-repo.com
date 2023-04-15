---
title: Cloning with a gitlab token instead of authentication
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, you can use a GitLab token to clone a repository without authentication.
---

**Contents**

[TOC]

### Introduction
GitLab token is a unique token that can be used to authenticate a user or a service to access the GitLab API. The token is generated for a user and can be used to clone a repository without authentication. This article explains how to use a GitLab token to clone a repository.

### Generating a Token
To generate a GitLab token, log in to your GitLab account and go to Settings > Access Tokens. Here, you can create a new token with a name and select the scope of the token. The scope defines the access level of the token.

### Using the Token
Once the token is generated, it can be used to clone a repository. To do so, use the following command in the terminal:

```git
git clone https://<token>@gitlab.com/<username>/<repository>.git
```

### Conclusion
Using a GitLab token to clone a repository without authentication is a convenient way to quickly access the repository. It is important to note that the token should be kept secure and not shared with anyone.
