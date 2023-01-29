---
title: At what point is it acceptable to employ anonymous inner classes without compromising anonymity?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Anonymous inner classes are safe to use when the class does not have any references to enclosing class instance variables or methods.
---

**Contents**

[TOC]

1. When to Use Anonymous Inner Classes
Anonymous inner classes are useful when you need to create a short class that will only be used once and will not be needed elsewhere in your code. This could include a listener for a GUI component, a runnable for a thread, or a comparator for a sorting algorithm.

2. When Not to Use Anonymous Inner Classes
Anonymous inner classes are not recommended for use in situations where the class could be reused elsewhere in your code, or if the class is complex enough that it should be given a name. Additionally, anonymous inner classes can make the code more difficult to read, so they should be avoided when possible.

3. Considerations for Anonymous Inner Classes
When using anonymous inner classes, it is important to consider their scope. Anonymous inner classes can only access variables that are declared final, and they can only access instance variables of the enclosing class. This can limit the functionality of the anonymous inner class, so it is important to consider these limitations when deciding whether or not to use an anonymous inner class.

4. Leak Safety
Anonymous inner classes are leak safe when they are used in a non-static context. This means that the anonymous inner class will not be leaked if the enclosing class is garbage collected. If the anonymous inner class is used in a static context, there is a risk of it being leaked, so it is important to avoid using anonymous inner classes in a static context.
