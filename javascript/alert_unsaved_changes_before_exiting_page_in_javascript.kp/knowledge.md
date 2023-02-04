---
title: Prompt user before exiting the webpage with unsaved modifications
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the window.onbeforeunload event to prompt the user to confirm they want to leave the page with unsaved changes.
---

**Contents**

[TOC]

1. #Check for Unsaved Changes
Before leaving the page, check if there are any unsaved changes. This can be done by comparing the current data with the initial data when the page was first loaded.

2. #Display Warning
If there are unsaved changes, display a warning to the user. This can be done with a modal window, alert, or confirm dialog.

3. #Listen for Leaving Events
Listen for events that indicate the user is leaving the page, such as the window.onbeforeunload or window.onunload events.

4. #Handle Leaving Events
When a leaving event is detected, check if there are any unsaved changes. If so, prompt the user to confirm that they want to leave the page without saving.
