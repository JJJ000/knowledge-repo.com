---
title: How can I add a private github repository as a dependency in npm?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Add the private repo`s URL to the `dependencies` field in your package.json file.
---

**Contents**

[TOC]

### Setting Up

1. Create a personal access token with the appropriate permissions for the repo you want to use in your project.
2. Add the token to your `.npmrc` file with the following syntax: `//<github-username>:<token>@github.com/<github-username>/<repo-name>.git`.

### Installing

1. Add the private repo as a dependency to your `package.json` file.
2. Run `npm install` to install the dependency.

### Updating

1. Update the version number in your `package.json` file.
2. Run `npm update` to update the dependency.
