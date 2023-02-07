---
title: What is the best way to disable JavaScript validation in my eclipse project?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Remove any JavaScript validation code from the project`s source files.
---

**Contents**

[TOC]

#1 Removing Javascript Validation from a Project

##Step 1: Disable Javascript Validation in Eclipse

1. Go to the Eclipse menu bar and select Window > Preferences.
2. Expand the Validation folder and select JavaScript Validator.
3. Uncheck the Enable JavaScript Validator checkbox.
4. Click OK to save the changes.

##Step 2: Remove Javascript Validation from Project Properties

1. Right-click on the project and select Properties.
2. Select Validation in the left pane.
3. Uncheck the Enable project specific settings checkbox.
4. Uncheck the Enable JavaScript Validator checkbox.
5. Click OK to save the changes.

##Step 3: Delete Validation Markers

1. Open the Problems view in Eclipse.
2. Select the Errors tab.
3. Select any validation markers that appear in the list.
4. Right-click and select Delete.
5. Click OK to confirm.

##Step 4: Clean Project

1. Right-click on the project and select Clean.
2. Select the Clean all projects option.
3. Click OK to confirm.
