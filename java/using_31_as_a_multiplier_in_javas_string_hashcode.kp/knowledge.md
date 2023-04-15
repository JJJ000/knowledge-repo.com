---
title: What is the purpose of using 31 as a multiplier in java's hashcode() method for strings?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: 31 is used as a multiplier because it is an odd prime number, which helps to reduce the occurrence of collisions when calculating hash codes.
---

**Contents**

[TOC]

### History

The use of 31 as a multiplier in Java's hashCode() for Strings originates from a paper by Dr. Daniel J. Bernstein, published in 1991. In the paper, Bernstein describes an algorithm for computing the hash of a string in constant time. The algorithm uses a polynomial of degree 31, and the multiplier 31 is used to ensure that the hash values are well distributed.

### Benefits

Using 31 as a multiplier has several benefits. First, it ensures that the hash values are well distributed, which is important for efficient lookups in hash tables. Second, it allows for the calculation of the hash value to be done in constant time, which is important for performance. Finally, it helps to ensure that the hash values are unique, which is important for avoiding collisions in hash tables.

### Drawbacks

One potential drawback of using 31 as a multiplier is that it is not optimal for all strings. For some strings, using a different multiplier may result in a more efficient hash calculation. Additionally, using 31 as a multiplier may not be suitable for all applications, as it may not be optimal for certain types of strings.

### Conclusion

Overall, using 31 as a multiplier for Java's hashCode() for Strings is a good choice for many applications. It ensures that the hash values are well distributed, allows for the calculation of the hash value to be done in constant time, and helps to ensure that the hash values are unique. However, it is not optimal for all strings, and may not be suitable for all applications.
