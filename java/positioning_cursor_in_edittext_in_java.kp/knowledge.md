---
title: Move the cursor to the end of the text in the edittext box
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Call the setSelection() method on the EditText object, passing in the length of the text as an argument.
---

**Contents**

[TOC]

### Solution

### Using append()
The `append()` method can be used to add text to the end of an `EditText` widget. This method adds the specified text to the end of the existing text in the `EditText` widget.

Syntax:
```
editText.append(String text);
```

Example:
```
editText.append("This text will be added to the end of the existing text.");
```

### Using setText()
The `setText()` method can be used to set the text of an `EditText` widget. This method sets the text of the `EditText` widget to the specified text.

Syntax:
```
editText.setText(String text);
```

Example:
```
editText.setText("This text will replace the existing text.");
```
