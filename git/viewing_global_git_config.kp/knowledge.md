---
title: What is the command to display my global git configuration?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run the command `git config --list --show-origin` to show your global Git configuration.
---

**Contents**

[TOC]

1. Check Local Configuration

```
git config --list
```

2. Check Global Configuration

```
git config --global --list
```

3. Set Global Configuration

```
git config --global user.name "Your Name"
git config --global user.email "Your Email"
```

4. Display Global Configuration

```
git config --global --edit
```
