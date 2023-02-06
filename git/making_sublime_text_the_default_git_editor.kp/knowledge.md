---
title: What steps do I need to take to set sublime text as the default editor for git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Set the `core.editor` configuration option to `subl -n -w`.
---

**Contents**

[TOC]

1. **Install Sublime Text Package Control**

Sublime Text Package Control allows you to manage all your Sublime Text packages. To install it, open Sublime Text and press `Ctrl + \` to open the console. Paste the following code and press `Enter`:

```
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
```

2. **Set Sublime Text as the Default Editor for Git**

To set Sublime Text as the default editor for Git, open a terminal window and type the following command:

```
git config --global core.editor "subl -n -w"
```

3. **Enable Sublime Text to Open Git Diff Files**

To enable Sublime Text to open Git diff files, open Sublime Text and open the Command Palette (`Ctrl + Shift + P`). Type `Install Package` and press `Enter`. Type `Git Diff` and press `Enter` to install the package.

4. **Configure Sublime Text to Open Git Diff Files**

To configure Sublime Text to open Git diff files, open Sublime Text and open the Command Palette (`Ctrl + Shift + P`). Type `Preferences: Git Diff Settings` and press `Enter`. Paste the following code and press `Enter`:

```
{
    "cmd": ["git", "difftool", "-y", "--no-prompt", "${file}"],
    "path": "${file}",
    "syntax": "Packages/Git Diff/Diff.tmLanguage"
}
```
