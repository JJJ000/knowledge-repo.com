---
title: Retrieve a single folder or directory from a github repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can download a single folder or directory from a GitHub repo by using the `Clone or download` button, selecting `Download ZIP`, and then extracting the desired folder or directory from the ZIP file.
---

**Contents**

[TOC]

### Using the Command Line
1. Install [Git](https://git-scm.com/) and make sure it is added to your system `PATH`
2. Open the terminal and navigate to the directory where you want to download the folder
3. Run the following command to clone the repository: `git clone <repository-url>`
4. Navigate to the cloned repository and run the following command to download the specific folder: `git clone --depth 1 --no-checkout -- <repository-url> <folder-name>`

### Using GitHub Desktop
1. Install [GitHub Desktop](https://desktop.github.com/)
2. Open GitHub Desktop and click on the `Clone a repository` button
3. Select the repository you want to clone and click `Clone`
4. Navigate to the repository in Finder and locate the folder you want to download
5. Right-click the folder and select `GitHub Desktop > Open in Desktop`
6. Select the branch you want to download and click `Clone`
