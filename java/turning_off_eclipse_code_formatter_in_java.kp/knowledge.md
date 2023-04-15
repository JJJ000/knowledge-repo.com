---
title: What is the process for disabling the eclipse code formatter for specific parts of Java code?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can turn off the Eclipse code formatter for certain sections of Java code by using the @formatteroff tag.
---

**Contents**

[TOC]

1. Using Comments 
2. Using @formatter Off Tag 
3. Using Eclipse Formatter Profile 
4. Using Eclipse Custom Code Template 

### 1. Using Comments 
Adding comments around the code you don't want to be formatted is the simplest way to turn off the Eclipse code formatter for certain sections of Java code. This is done by adding a comment at the beginning and end of the code block you want to exclude from formatting. 

For example, if you want to turn off the Eclipse code formatter for a specific line of code, you can add a comment before and after the line. 

```java
// @formatter:off
// Your code here
// @formatter:on
```

### 2. Using @formatter Off Tag
The @formatter off tag is a special tag that can be used to disable the Eclipse code formatter for a specific section of code. This tag must be placed at the beginning and end of the code block you want to exclude from formatting. 

For example, if you want to turn off the Eclipse code formatter for a specific line of code, you can add the @formatter off tag before and after the line. 

```java
@formatter:off
// Your code here
@formatter:on
```

### 3. Using Eclipse Formatter Profile
Eclipse allows you to create custom formatting profiles, which can be used to turn off the code formatter for certain sections of code. To create a new formatting profile, open the Eclipse Preferences window, select the Java > Code Style > Formatter option, and click the New button. 

Once you have created a new formatting profile, you can select it from the Formatter drop-down list in the Java editor. This will allow you to turn off the Eclipse code formatter for certain sections of code. 

### 4. Using Eclipse Custom Code Template
Eclipse also allows you to create custom code templates, which can be used to turn off the code formatter for certain sections of code. To create a new code template, open the Eclipse Preferences window, select the Java > Code Style > Code Templates option, and click the New button. 

Once you have created a new code template, you can select it from the Code Template drop-down list in the Java editor. This will allow you to turn off the Eclipse code formatter for certain sections of code.
