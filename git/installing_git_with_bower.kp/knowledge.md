---
title: Git is either not installed or not in the path according to bower
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git needs to be installed and added to the PATH environment variable in order to be used with Bower.
---

**Contents**

[TOC]

## Installing Git

Git is a version control system used for tracking changes in computer files and coordinating work on those files among multiple people. To install Git, you will need to download the appropriate installer for your operating system from the [Git website](https://git-scm.com/downloads). Once you have downloaded the installer, double-click it to launch the installation process. Follow the on-screen instructions to complete the installation.

## Adding Git to the PATH

Once Git is installed, you will need to add it to your PATH (a list of directories where the system will look for executable files). To do this, open the Control Panel and go to System and Security > System > Advanced System Settings. Select the Advanced tab and then click the Environment Variables button. Under the System Variables section, select the Path variable and then click the Edit button. Add the path of the Git executable to the end of the list.

## Verifying Installation

Once you have installed and added Git to your PATH, you can verify that it is working properly by opening a command prompt and typing `git --version`. This should return the version number of the installed Git.

## Troubleshooting

If you encounter any issues during the installation or configuration of Git, you can check the [Git website](https://git-scm.com/downloads) for troubleshooting tips. You can also search online for help with specific issues.
