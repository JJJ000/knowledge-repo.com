---
title: Text change listener for android
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Text Change Listener in Java is an interface that is used to detect changes in an EditText view.
---

**Contents**

[TOC]

### Overview
Text Change Listener is an interface in Java used to detect changes in text fields. It is implemented by classes that want to be notified when the text of a text field changes.

### Syntax
The syntax for implementing a Text Change Listener is as follows:

```java
textField.addTextChangedListener(new TextWatcher() {
    @Override
    public void onTextChanged(CharSequence s, int start, int before, int count) {
        // Your code here
    }

    @Override
    public void beforeTextChanged(CharSequence s, int start, int count, int after) {
        // Your code here
    }

    @Override
    public void afterTextChanged(Editable s) {
        // Your code here
    }
});
```

### Methods
Text Change Listener has three methods that must be implemented:

1. onTextChanged(): This method is called when the text of a text field changes. It takes four parameters: the CharSequence of the text, the start index of the text, the number of characters before the text change, and the number of characters after the text change.

2. beforeTextChanged(): This method is called before the text of a text field changes. It takes four parameters: the CharSequence of the text, the start index of the text, the number of characters before the text change, and the number of characters after the text change.

3. afterTextChanged(): This method is called after the text of a text field changes. It takes one parameter: the Editable of the text.

### Example
Let's look at an example of how to use Text Change Listener.

```java
EditText editText = findViewById(R.id.editText);
editText.addTextChangedListener(new TextWatcher() {
    @Override
    public void onTextChanged(CharSequence s, int start, int before, int count) {
        // Your code here
    }

    @Override
    public void beforeTextChanged(CharSequence s, int start, int count, int after) {
        // Your code here
    }

    @Override
    public void afterTextChanged(Editable s) {
        // Your code here
    }
});
```

In this example, we are using Text Change Listener to detect changes in the text of an EditText. We use the addTextChangedListener() method to register a TextWatcher, which is an implementation of the Text Change Listener interface. We then implement the three methods of the Text Change Listener interface. The onTextChanged() method is called when the text of the EditText changes, the beforeTextChanged() method is called before the text of the EditText changes, and the afterTextChanged() method is called after the text of the EditText changes.
