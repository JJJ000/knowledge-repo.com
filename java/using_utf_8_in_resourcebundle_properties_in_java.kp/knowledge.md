---
title: Using utf-8 encoding with resourcebundle properties files
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a UTF-8-encoded .properties file when constructing a ResourceBundle.
---

**Contents**

[TOC]

#### Section 1: Setting UTF-8

The first step to using UTF-8 in resource properties with ResourceBundle in Java is to set the encoding of your resource bundle file to UTF-8. This can be done by adding a comment to the top of the file that specifies the encoding. For example, the following line should be added to the top of your resource bundle file: 

```
# encoding: UTF-8
```

#### Section 2: Creating the ResourceBundle

The next step is to create the ResourceBundle object. This can be done by using the ResourceBundle.getBundle() method. This method takes two arguments: the base name of the resource bundle and the Locale. For example, if the resource bundle file is named "myResourceBundle" and the locale is English, the following code can be used to create the ResourceBundle:

```
ResourceBundle myResourceBundle = ResourceBundle.getBundle("myResourceBundle", Locale.ENGLISH);
```

#### Section 3: Accessing the Properties

Once the ResourceBundle has been created, you can access the properties by using the getString() method. This method takes the key of the property as an argument and returns the value of the property as a String. For example, if the key of the property is "hello", the following code can be used to access the property:

```
String hello = myResourceBundle.getString("hello");
```

#### Section 4: Outputting the Properties

Finally, the properties can be outputted using the System.out.println() method. For example, if the value of the property is "Hello World", the following code can be used to output the property:

```
System.out.println(hello); // Outputs "Hello World"
```
