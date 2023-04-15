---
title: Git extensions encountered an error (win32 error 487) when attempting to allocate memory space for the cygwin heap, and then encountered a further error (win32 error 0)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: This error is caused by a lack of available memory in the system.
---

**Contents**

[TOC]

### Resolution

1. Increase the amount of memory available to the Windows operating system.
2. Increase the amount of space available to the Cygwin heap.

### Increasing Memory Available to Windows

1. Right-click on the start menu and select “System”.
2. Select “Advanced system settings” from the left-hand menu.
3. Select the “Advanced” tab in the System Properties window.
4. Select “Settings” in the Performance section.
5. Select the “Advanced” tab in the Performance Options window.
6. Increase the amount of memory available to the Windows operating system by adjusting the “Virtual memory” settings.

### Increasing Space Available to Cygwin Heap

1. Open the Cygwin terminal.
2. Type “rebaseall -v” and press enter.
3. This will increase the amount of space available to the Cygwin heap.
