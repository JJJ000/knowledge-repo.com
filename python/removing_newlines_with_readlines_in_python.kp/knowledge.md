---
title: Removing newline characters when using .readlines()
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the .strip() method on each line read in to get rid of the \n.
---

**Contents**

[TOC]

**Using rstrip() to Remove \n**

One way to remove the \n when using .readlines() in Python is to use the rstrip() method. This method removes any trailing characters, including the \n character. 

For example:

```
f = open("myfile.txt", "r")
lines = f.readlines()

for line in lines: 
    line = line.rstrip()
    print(line)

f.close()
```

**Using List Comprehension**

Another way to remove \n when using .readlines() in Python is to use a list comprehension. This method allows you to create a new list of lines from the old one, without the \n character. 

For example: 

```
f = open("myfile.txt", "r")
lines = f.readlines()

lines = [line.rstrip() for line in lines]

for line in lines: 
    print(line)

f.close()
```

**Using strip() to Remove \n**

Another way to remove the \n when using .readlines() in Python is to use the strip() method. This method removes any leading or trailing characters, including the \n character. 

For example:

```
f = open("myfile.txt", "r")
lines = f.readlines()

for line in lines: 
    line = line.strip()
    print(line)

f.close()
```

**Using splitlines() to Remove \n**

Finally, another way to remove the \n when using .readlines() in Python is to use the splitlines() method. This method splits the string on the \n character and returns a list of lines. 

For example:

```
f = open("myfile.txt", "r")
lines = f.readlines()

lines = "".join(lines).splitlines()

for line in lines: 
    print(line)

f.close()
```
