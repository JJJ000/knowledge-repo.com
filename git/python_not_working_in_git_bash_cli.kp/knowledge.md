---
title: Python is not functioning in the git bash command line
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Python may not be added to the system PATH variable in the git bash command line.
---

**Contents**

[TOC]

### Step 1: Install Python

In order to use Python in the command line of Git Bash, it must first be installed on your computer. Windows users can download and install Python from the official [Python website](https://www.python.org/downloads/).

### Step 2: Add Python to Path

Once Python has been installed, it must be added to the system path. This allows the command line of Git Bash to recognize and use Python. To do this, open the System Properties window and select the Advanced tab. Click the Environment Variables button and add the path to the Python directory in the System Variables section.

### Step 3: Verify Installation

Once Python has been added to the system path, it can be verified by typing `python` into the command line of Git Bash. If Python is installed correctly, a Python prompt will appear.

### Step 4: Execute Python Scripts

Once Python has been verified, Python scripts can be executed in the command line of Git Bash. To do this, type `python <scriptname>.py` into the command line, where `<scriptname>` is the name of the Python script.
