---
title: Do any git hooks exist for pull requests?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, there is no git hook specifically for pull requests.
---

**Contents**

[TOC]

## Pre-Pull Hooks

Git provides two pre-pull hooks that are triggered before a git pull is executed:

1. `pre-pull`: This hook is invoked by git pull and can be used to inspect the local and remote histories prior to a pull.

2. `pre-rebase`: This hook is invoked by git pull --rebase and is used to inspect the local and remote histories prior to a rebase.

## Post-Pull Hooks

Git also provides two post-pull hooks that are triggered after a git pull is executed:

1. `post-merge`: This hook is invoked by git pull and can be used to inspect the local and remote histories after a pull.

2. `post-checkout`: This hook is invoked by git pull and can be used to inspect the local and remote histories after a checkout.
