---
title: What is the process for creating a git patch for a certain commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run the command `git format-patch <commit-hash>`.
---

**Contents**

[TOC]

### Generating a Patch for a Specific Commit

### Using the Git Command Line
1. Checkout the commit you want to generate a patch for: 
   `git checkout <commit-hash>`
2. Generate the patch: 
   `git format-patch -1`

### Using a GUI
1. Open the commit you want to generate a patch for in the GUI.
2. Select the "Generate Patch" option from the menu.
