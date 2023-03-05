---
title: Retrieve JSON representation of an object in intellij idea using debugger
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Right-click on the variable in the debugger and select `Copy Value` -> `Copy JSON` and then paste it into a JSON file.
---

**Contents**

[TOC]

### Section 1: Installing the JSON Viewer plugin
1. Open IntelliJ IDEA.
2. Go to **File > Settings > Plugins**.
3. Click on **Marketplace** and search for **JSON Viewer**.
4. Click on **Install** and restart IntelliJ IDEA when prompted.

### Section 2: Debugging and accessing JSON
1. Set a breakpoint in your code where the JSON object is available.
2. Run the code in debugging mode.
3. When the breakpoint is hit, open the debugger by going to **Run > Debug**.
4. Expand the variables section in the debugger and find the JSON object.
5. Right-click on the JSON object and select **View as JSON**.

### Section 3: Copying JSON as text
1. Follow steps 1-5 in Section 2.
2. Right-click on the JSON object and select **Copy as JSON**.
3. Open a text editor of your choice (e.g., Notepad, Sublime Text).
4. Paste the JSON object into the text editor.

### Section 4: Saving JSON as a file
1. Follow steps 1-5 in Section 2.
2. Right-click on the JSON object and select **Save as JSON**.
3. Choose a location on your computer where you want to save the file.
4. Give the file a name and click **Save**.
