---
title: What is the syntax for creating a JavaScript breakpoint in chrome using code?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `debugger;` statement to set a JavaScript breakpoint from code in Chrome.
---

**Contents**

[TOC]

1. Open Developer Tools
  - Open the Chrome browser and go to the page where you want to set the breakpoint.
  - Right-click on the page and select "Inspect" from the dropdown menu. This will open the Developer Tools panel.

2. Set the Breakpoint
  - In the Developer Tools panel, select the "Sources" tab.
  - In the Sources tab, find the file containing the JavaScript code you want to debug.
  - Click on the line number where you want to set the breakpoint. This will add a blue breakpoint marker to the line.

3. Execute the Code
  - Refresh the page or execute the code to trigger the breakpoint.

4. Debug the Code
  - When the breakpoint is triggered, the code will pause and the Developer Tools panel will open.
  - You can now step through the code line-by-line and debug as needed.
