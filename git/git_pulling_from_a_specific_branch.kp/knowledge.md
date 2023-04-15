---
title: What is the command to ensure git will always pull from a specific branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can set the default branch to pull from in the Git configuration file.
---

**Contents**

[TOC]

### Configure Default Branch
1. Navigate to the repository in the GitHub web interface and select the desired default branch.
2. Click the "Settings" tab at the top of the page.
3. Scroll down to the "Danger Zone" section and select the "Default branch" dropdown menu.
4. Select the desired branch and click the "Update" button.

### Configure Git Client
1. Open a terminal window and navigate to the local repository.
2. Run the command `git config --local branch.autosetupmerge always`
3. Run the command `git config --local branch.autosetuprebase always`

This will configure the local git repository to always pull from the default branch specified in the GitHub web interface.
