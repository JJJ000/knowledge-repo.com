---
title: Visual studio code is unable to recognize the presence of an installed git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Visual Studio Code needs to be configured to detect an installed Git.
---

**Contents**

[TOC]

# Solution

## Step 1: Check if Git is Installed

The first step is to check if Git is installed on your machine. To do this, open the command prompt and type `git --version`. If Git is installed, it will show the version of Git installed on your machine. 

## Step 2: Configure Visual Studio Code

If Git is installed, the next step is to configure Visual Studio Code to detect the installed version. To do this, open Visual Studio Code and go to `File > Preferences > Settings` and search for `Git: Path`. Then, click `Edit in Settings.json` and add the path to the installed Git.

## Step 3: Check the Status Bar

After configuring Visual Studio Code to detect the installed Git, the last step is to check the status bar. If the status bar shows the Git version, then Visual Studio Code has successfully detected the installed Git.
