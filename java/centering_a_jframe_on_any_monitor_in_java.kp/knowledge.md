---
title: What is the best way to make a jframe appear in the center of the screen, regardless of the monitor resolution?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Set the JFrame`s location to the center of the screen using the setLocationRelativeTo(null) method.
---

**Contents**

[TOC]

### Section 1: Setting the Default Look and Feel

The first step to setting a JFrame to appear centered, regardless of monitor resolution, is to set the default look and feel. This can be done by calling the `UIManager.setLookAndFeel` method, passing in the desired look and feel class.

For example, to set the default look and feel to the Windows look and feel, the following code can be used:

```java
UIManager.setLookAndFeel(UIManager.getSystemLookAndFeelClassName());
```

### Section 2: Creating the JFrame

Once the default look and feel has been set, the JFrame can be created and set to appear centered, regardless of monitor resolution. This can be done by calling the `setLocationRelativeTo` method on the JFrame instance, passing in `null` as the argument.

For example:

```java
JFrame frame = new JFrame("My Frame");
frame.setLocationRelativeTo(null);
```

### Section 3: Setting the Size of the JFrame

Once the JFrame has been created and set to appear centered, the size of the JFrame can be set. This can be done by calling the `setSize` method on the JFrame instance, passing in the desired width and height as arguments.

For example:

```java
frame.setSize(500, 500);
```

### Section 4: Displaying the JFrame

Finally, the JFrame can be displayed by calling the `setVisible` method on the JFrame instance, passing in `true` as the argument.

For example:

```java
frame.setVisible(true);
```
