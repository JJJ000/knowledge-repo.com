---
title: What is the process for completely uninstalling Node.js from mac os x and reinstalling it from the start?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Run `brew uninstall node` followed by `brew install node` to completely uninstall and reinstall Node.js on Mac OS X.
---

**Contents**

[TOC]

### Uninstalling Node.js
1. Open up the Terminal application.
2. Enter the following command: `sudo rm -rf /usr/local/bin/node /usr/local/include/node /usr/local/lib/node_modules /var/db/receipts/org.nodejs.*`
3. Enter the following command to remove npm: `sudo rm -rf /usr/local/share/man/man1/node.1 /usr/local/lib/dtrace/node.d ~/.npm ~/.node_repl_history`
4. Enter the following command to uninstall Homebrew: `brew uninstall node`

### Reinstalling Node.js
1. Download the latest version of Node.js from the official website.
2. Open the downloaded file.
3. Follow the on-screen instructions to install Node.js.
4. Once the installation is complete, open up the Terminal application and enter the following command to verify that Node.js is installed correctly: `node -v`
5. If the version number is displayed, Node.js is installed correctly.
