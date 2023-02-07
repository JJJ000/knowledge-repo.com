---
title: Turning on window.alert in chrome
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The window.alert function can be re-enabled in Chrome by setting the dom.disable\_beforeunload preference to false in the chrome//flags page.
---

**Contents**

[TOC]

### Step 1: Access Chrome Flags
1. Open a new tab in Chrome and type `chrome://flags` into the address bar.

### Step 2: Disable the "Enable Native Notifications" Flag
2. Find the flag labeled **"Enable native notifications"** and select **"Disabled"** from the dropdown menu.

### Step 3: Relaunch Chrome
3. Click the **Relaunch Now** button at the bottom of the page.

### Step 4: Re-enable Window.alert
4. Open your Javascript file and re-enable the `window.alert` command.
