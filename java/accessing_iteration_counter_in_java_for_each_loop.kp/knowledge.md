---
title: What is the method of accessing an iteration-counter in java's for-each loop?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, there is no built-in way to access an iteration counter in a for-each loop.
---

**Contents**

[TOC]

**Using a Counter Variable**

One way to access an iteration counter in Java's for-each loop is to use a counter variable. This approach involves declaring an integer variable outside the loop and incrementing it each time the loop iterates. The counter variable can then be accessed within the loop to perform any desired operations.

```java
int counter = 0;
for(String str : myStringArray) {
    //Do something with the string
    counter++;
}
```

**Using an Index Variable**

Another way to access an iteration counter in Java's for-each loop is to use an index variable. This approach involves declaring an integer variable outside the loop and assigning it the index of the current item in the loop. The index variable can then be accessed within the loop to perform any desired operations.

```java
int index = 0;
for(String str : myStringArray) {
    //Do something with the string
    index = myStringArray.indexOf(str);
}
```

**Using a for Loop**

Yet another way to access an iteration counter in Java's for-each loop is to use a for loop. This approach involves declaring an integer variable outside the loop and incrementing it each time the loop iterates. The counter variable can then be accessed within the loop to perform any desired operations.

```java
int counter = 0;
for(int i = 0; i < myStringArray.length; i++) {
    String str = myStringArray[i];
    //Do something with the string
    counter++;
}
```

**Using a While Loop**

The final way to access an iteration counter in Java's for-each loop is to use a while loop. This approach involves declaring an integer variable outside the loop and incrementing it each time the loop iterates. The counter variable can then be accessed within the loop to perform any desired operations.

```java
int counter = 0;
int i = 0;
while(i < myStringArray.length) {
    String str = myStringArray[i];
    //Do something with the string
    counter++;
    i++;
}
```
