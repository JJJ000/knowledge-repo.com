---
title: How to resolve the error message 'invalid active developer path (/library/developer/commandlinetools)' on Mac
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Run `xcode-select --install` in the terminal to install the Command Line Tools.
---

**Contents**

[TOC]

### Check Xcode Version

First, check the version of Xcode installed on your system. To do this, open the Terminal application and enter `xcode-select --version`. If the version is not the latest, update Xcode to the latest version.

### Uninstall Xcode

If updating Xcode does not resolve the issue, try uninstalling and reinstalling Xcode. To uninstall Xcode, open the Terminal application and enter `sudo /Library/Developer/Library/uninstall-devtools --mode=all`.

### Reinstall Xcode

Once Xcode has been uninstalled, reinstall the latest version of Xcode. To do this, open the App Store on your Mac and search for Xcode. Download and install the latest version of Xcode.

### Re-enable Command Line Tools

Finally, re-enable the Command Line Tools. To do this, open the Terminal application and enter `xcode-select --install`. This will reinstall the Command Line Tools and should resolve the issue.
