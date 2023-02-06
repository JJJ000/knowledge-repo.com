---
title: What is the best way to prevent .class files from appearing in the open resource dialog in eclipse?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the `Filters...` button in the Open Resource dialog to hide .class files.
---

**Contents**

[TOC]

# Section 1: Exclude Files

1. In the Package Explorer view, right-click on the project you want to hide the .class files from.
2. Select "Properties" from the menu.
3. In the Properties window, select "Resource" from the list on the left.
4. Check the "Exclude all" checkbox.
5. Click the "Add Pattern" button and enter "*.class" as the pattern.
6. Click "OK" to save the changes.

# Section 2: Refresh Project

1. Right-click on the project in the Package Explorer view.
2. Select "Refresh" from the menu.

# Section 3: Verify Changes

1. Open the Open Resource dialog by pressing Ctrl+Shift+R.
2. Enter the name of the file you want to open.
3. Verify that the .class files are not listed in the search results.
