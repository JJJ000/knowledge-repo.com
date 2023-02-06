---
title: What is the best way to save a printstacktrace to a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The printStackTrace() method can be used to store the stack trace into a StringWriter and then the toString() method can be used to convert it into a String.
---

**Contents**

[TOC]

### Section 1: Create PrintWriter

The first step is to create a PrintWriter object. This object is used to write a stack trace to a character-output stream.

```
PrintWriter pw = new PrintWriter(new StringWriter());
```

### Section 2: Call printStackTrace

The next step is to call the printStackTrace method on the Throwable object. This will print out the stack trace to the PrintWriter object.

```
throwable.printStackTrace(pw);
```

### Section 3: Get Output

The last step is to get the output from the PrintWriter object. This can be done by calling the toString method.

```
String stackTrace = pw.toString();
```

### Section 4: Close PrintWriter

Finally, it is important to close the PrintWriter object to avoid memory leaks.

```
pw.close();
```
