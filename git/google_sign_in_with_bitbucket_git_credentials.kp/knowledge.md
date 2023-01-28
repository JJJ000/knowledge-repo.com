---
title: Credentials for a bitbucket account created using a google sign-up
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Bitbucket does not support signing in with Google credentials.
---

**Contents**

[TOC]

### Google OAuth

If you've signed up for Bitbucket using your Google account, you can use Google OAuth to authenticate with Bitbucket. This allows you to use your existing Google credentials to sign in to Bitbucket.

### Generating an Access Token

In order to authenticate with Bitbucket using Google OAuth, you must generate an access token. You can do this by going to the Google Developer Console, selecting your project, and then selecting the Credentials tab. From there, you'll need to create an OAuth Client ID, which will generate an access token.

### Setting Up Git

Once you have your access token, you can set up Git to use it for authentication. To do this, you'll need to set the `GIT_AUTHORIZATION_TOKEN` environment variable to the access token you just generated.

### Using Git

Once you've set up your environment variable, you can use Git as usual. When authenticating with Bitbucket, you'll be prompted for your Google credentials. Once you've entered them, you'll be able to access your repositories.
