---
title: You need to provide your username and password to perform a git push
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Yes, git push requires a username and password for authentication.
---

**Contents**

[TOC]

### Yes

Git push requires a username and password in order to authenticate and push the changes to the remote repository. Without authentication, the push will fail.

### No

Git push does not always require a username and password. If you are using SSH authentication, you can use SSH keys instead of a username and password. Additionally, if you are using a hosted repository service, such as GitHub or Bitbucket, you can set up an access token to authenticate the push.
