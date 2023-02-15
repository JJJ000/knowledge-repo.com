---
title: What is the best way to prevent chrome and opera from arranging JSON objects in ascending order by index?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: You cannot stop Chrome and Opera from sorting JSON objects by Index ASC in JSON.
---

**Contents**

[TOC]

1. **Disable Sorting in Chrome**

- Open Chrome Developer Tools
- Select the Network tab
- Click the "Disable Cache" checkbox
- Refresh the page

2. **Disable Sorting in Opera**

- Open Opera Developer Tools
- Select the Network tab
- Uncheck the "Enable Cache" checkbox
- Refresh the page

3. **Prevent Sorting with JavaScript**

- Use the `Object.freeze()` method to prevent the JSON object from being sorted
- This will ensure that the JSON object remains in its original order

4. **Prevent Sorting with JSON Schema**

- Use a JSON Schema to define the order of the JSON object
- This will ensure that the JSON object remains in its original order
