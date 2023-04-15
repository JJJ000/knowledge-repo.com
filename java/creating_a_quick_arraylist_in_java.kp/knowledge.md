---
title: Creating a one-element arraylist quickly and conveniently
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Create a one element arraylist in Java by calling the constructor with a single element as an argument.
---

**Contents**

[TOC]

### Import ArrayList

The first step to creating a one element arraylist in Java is to import the ArrayList class. This can be done by adding the following line of code to the top of the program:

```java
import java.util.ArrayList;
```

### Create ArrayList

The next step is to create the ArrayList. This can be done by declaring a new ArrayList object and assigning it to a variable, like so:

```java
ArrayList<String> myList = new ArrayList<String>();
```

### Add Element

The third step is to add the desired element to the ArrayList. This can be done by using the `add()` method, like so:

```java
myList.add("Element");
```

### Verify Contents

Finally, the contents of the ArrayList can be verified by using the `size()` method, like so:

```java
int size = myList.size();
```

The `size` variable should now contain the value `1`, indicating that the ArrayList contains one element.
