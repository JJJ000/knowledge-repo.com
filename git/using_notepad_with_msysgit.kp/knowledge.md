---
title: What is the process for integrating notepad++ (or another text editor) with msysgit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In Notepad++, go to Settings > Preferences > MISC > Shell Integration and check the box for `Git Bash`.
---

**Contents**

[TOC]

# Section 1: Installation

1. Download and install [Notepad++](https://notepad-plus-plus.org/downloads/).
2. Download and install [msysgit](https://msysgit.github.io/).

# Section 2: Configuring Notepad++

1. Open Notepad++ and go to Settings > Preferences.
2. Under the "Language" menu, select "Define your language…"
3. Click the "Import…" button and select the "git.xml" file located in the msysgit installation directory.
4. Click "OK" to save the changes.

# Section 3: Configuring msysgit

1. Open the Git Bash shell and run the following command:

```
git config --global core.editor "'C:/Program Files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
```

# Section 4: Testing

1. Create a new file using Notepad++ and save it to the Git repository.
2. Run the following command in the Git Bash shell:

```
git add <filename>
```

3. Check that the file is correctly added to the repository.
