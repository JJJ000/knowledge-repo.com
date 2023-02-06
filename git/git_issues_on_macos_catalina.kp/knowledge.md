---
title: Git is not compatible with macos catalina as the active developer path (/library/developer/commandlinetools) is missing, resulting in an 'xcrun error invalid active developer path' message
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The active developer path needs to be updated to the latest version of Xcode.
---

**Contents**

[TOC]

# Overview
Git is a version control system used to track changes in computer files and coordinate work on those files among multiple people. It is a popular tool used by developers and software teams to manage their projects. However, some users have reported issues with using Git on MacOS Catalina, such as the "xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing" error.

# Causes
The "xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing" error is caused by a mismatch between the version of Xcode installed on the user's computer and the version of Git installed. The error occurs when the user attempts to run a command that requires Xcode, but Xcode is not installed or not installed correctly.

# Solutions
The best solution for this issue is to ensure that the user has the correct version of Xcode installed. The user can check the version of Xcode installed by opening the App Store and selecting "Updates" from the top menu. If the user does not have the correct version of Xcode installed, they can download it from the App Store. 

Once the correct version of Xcode is installed, the user should also make sure that the version of Git installed is compatible with the version of Xcode installed. The user can check the version of Git installed by running the command "git --version" in the terminal. If the version of Git installed is not compatible with the version of Xcode installed, the user can download the appropriate version of Git from the official Git website. 

# Conclusion
The "xcrun: error: invalid active developer path (/Library/Developer/CommandLineTools), missing" error is caused by a mismatch between the version of Xcode installed and the version of Git installed. The best solution for this issue is to ensure that the correct version of Xcode and Git are installed. Once the correct versions are installed, the user should be able to use Git without any further issues.
