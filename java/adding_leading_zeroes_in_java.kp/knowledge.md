---
title: How can I add leading zeroes to a number in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use String.format() to format the number and add the desired number of leading zeroes.
---

**Contents**

[TOC]

### Using String.format()

String.format() can be used to add leading zeroes to a number. The following example adds leading zeroes to a number until it is 10 digits long:

```java
int number = 12345;
String result = String.format("%010d", number);
System.out.println(result);
```

The output of this code will be:
```
0000012345
```

### Using DecimalFormat

DecimalFormat can also be used to add leading zeroes to a number. The following example adds leading zeroes to a number until it is 10 digits long:

```java
int number = 12345;
DecimalFormat df = new DecimalFormat("0000000000");
String result = df.format(number);
System.out.println(result);
```

The output of this code will be:
```
0000012345
```

### Using StringBuilder

StringBuilder can be used to add leading zeroes to a number. The following example adds leading zeroes to a number until it is 10 digits long:

```java
int number = 12345;
StringBuilder sb = new StringBuilder(10);
sb.append(String.valueOf(number));
while (sb.length() < 10) {
    sb.insert(0, "0");
}
String result = sb.toString();
System.out.println(result);
```

The output of this code will be:
```
0000012345
```

### Using StringUtils

StringUtils can also be used to add leading zeroes to a number. The following example adds leading zeroes to a number until it is 10 digits long:

```java
int number = 12345;
String result = StringUtils.leftPad(String.valueOf(number), 10, '0');
System.out.println(result);
```

The output of this code will be:
```
0000012345
```
