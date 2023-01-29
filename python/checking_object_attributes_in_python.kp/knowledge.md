---
title: What is the process for determining if an object has a particular attribute?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can check if an object has an attribute by using the hasattr() function.
---

**Contents**

[TOC]

### Using the hasattr() Function
The hasattr() function can be used to check if an object has an attribute. The syntax is as follows:
```
hasattr(object, attribute)
```

The function returns a boolean value, True if the object has the attribute and False if it does not. 

For example, if we have an object named "myObject" that has an attribute named "myAttribute", we can check if it has the attribute using the following code:

```
hasattr(myObject, 'myAttribute')
```

### Using the getattr() Function
The getattr() function can also be used to check if an object has an attribute. The syntax is as follows:
```
getattr(object, attribute, default)
```

The function returns the value of the attribute if it exists, or the default value if it does not.

For example, if we have an object named "myObject" that has an attribute named "myAttribute", we can check if it has the attribute using the following code:

```
getattr(myObject, 'myAttribute', None)
```

If the attribute exists, the function will return its value. If the attribute does not exist, the function will return None.
