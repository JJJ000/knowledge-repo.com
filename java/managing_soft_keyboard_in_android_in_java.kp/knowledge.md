---
title: Programmatically hiding and showing the Android soft keyboard
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the InputMethodManager`s hideSoftInputFromWindow and showSoftInput methods.
---

**Contents**

[TOC]

**Section 1: Show Soft Keyboard**

To show the soft keyboard, use the `showSoftInput` method of the `InputMethodManager` class. This method takes two parameters:

1. The `View` to which the keyboard should be attached.
2. The `int` flag for the type of keyboard that should be shown.

The following code snippet shows how to use `showSoftInput` to show the soft keyboard:

```java
InputMethodManager inputMethodManager = (InputMethodManager) getSystemService(Context.INPUT_METHOD_SERVICE);
inputMethodManager.showSoftInput(view, InputMethodManager.SHOW_IMPLICIT);
```

**Section 2: Hide Soft Keyboard**

To hide the soft keyboard, use the `hideSoftInputFromWindow` method of the `InputMethodManager` class. This method takes two parameters:

1. The `IBinder` token of the window that is making the request.
2. The `int` flag for the type of keyboard that should be hidden.

The following code snippet shows how to use `hideSoftInputFromWindow` to hide the soft keyboard:

```java
InputMethodManager inputMethodManager = (InputMethodManager) getSystemService(Context.INPUT_METHOD_SERVICE);
inputMethodManager.hideSoftInputFromWindow(view.getWindowToken(), 0);
```

**Section 3: Get Current Input Method**

To get the current input method, use the `getCurrentInputMethodSubtype` method of the `InputMethodManager` class. This method takes no parameters and returns the current input method subtype.

The following code snippet shows how to use `getCurrentInputMethodSubtype` to get the current input method:

```java
InputMethodManager inputMethodManager = (InputMethodManager) getSystemService(Context.INPUT_METHOD_SERVICE);
InputMethodSubtype currentInputMethodSubtype = inputMethodManager.getCurrentInputMethodSubtype();
```

**Section 4: Set Input Method**

To set the input method, use the `setInputMethod` method of the `InputMethodManager` class. This method takes two parameters:

1. The `IBinder` token of the window that is making the request.
2. The `String` id of the input method that should be set.

The following code snippet shows how to use `setInputMethod` to set the input method:

```java
InputMethodManager inputMethodManager = (InputMethodManager) getSystemService(Context.INPUT_METHOD_SERVICE);
inputMethodManager.setInputMethod(view.getWindowToken(), "com.android.inputmethod.latin");
```
