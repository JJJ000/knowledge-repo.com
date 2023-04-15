---
title: Copy the files from a github repository (without the containing folder)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To clone the contents of a GitHub repository without the folder itself, use the command `git clone --depth=1 <repo-url>`.
---

**Contents**

[TOC]

### Download the Repository

1. Go to the repository page on GitHub.
2. Click the green "Clone or download" button.
3. Copy the URL for the repository.

### Use Git

1. Open a terminal window.
2. Change to the directory where you want to clone the repository.
3. Use the `git clone` command with the URL you copied from GitHub.

### Copy Contents

1. Change to the directory where the repository was cloned.
2. Copy the contents of the repository to the desired location.

### Remove Cloned Repository

1. Delete the cloned repository directory.
