---
title: What is the best way to credit multiple developers for a single commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `--author` flag when committing to attribute multiple developers to a single commit.
---

**Contents**

[TOC]

# Section 1: Understanding the Concept

When working in a collaborative environment, it is often necessary to attribute a single commit to multiple developers. This can be done using a feature of Git called “multi-author commits”. This allows developers to specify multiple authors for a single commit.

# Section 2: Setting Up Git

In order to use multi-author commits, the Git configuration must be set up correctly. This can be done by running the following command:

`git config --global user.name "Your Name"`

`git config --global user.email "your_email@example.com"`

This will set the user name and email for the Git repository.

# Section 3: Adding Multiple Authors

Once the configuration is set up, multiple authors can be added to a commit. This is done by using the “--author” flag when committing a change. This flag takes a string in the following format:

`--author="Name <email@example.com>"`

This flag can be used multiple times to add multiple authors to a single commit.

# Section 4: Committing the Change

Once the authors have been added, the change can be committed using the “git commit” command. The authors will be listed in the commit message, allowing the contribution of multiple developers to be acknowledged.
