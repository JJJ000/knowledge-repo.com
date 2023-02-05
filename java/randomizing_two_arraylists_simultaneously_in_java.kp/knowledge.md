---
title: What is the best way to shuffle two arraylists in the same order?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Using Collections.shuffle() on both ArrayLists will randomize them in the same fashion.
---

**Contents**

[TOC]

## Solution

### Step 1: Create two ArrayLists
Create two ArrayLists with the desired values to be randomized.

```
ArrayList<String> list1 = new ArrayList<>(Arrays.asList("A","B","C"));
ArrayList<String> list2 = new ArrayList<>(Arrays.asList("1","2","3"));
```

### Step 2: Create a Random Object
Create a Random object that will be used to generate random numbers.

```
Random randomGenerator = new Random();
```

### Step 3: Randomize the ArrayLists
Loop through each ArrayList, generating random numbers to use as indices for swapping elements.

```
for (int i = 0; i < list1.size(); i++) {
    int randomIndex = randomGenerator.nextInt(list1.size());
    String temp = list1.get(i);
    list1.set(i, list1.get(randomIndex));
    list1.set(randomIndex, temp);

    randomIndex = randomGenerator.nextInt(list2.size());
    temp = list2.get(i);
    list2.set(i, list2.get(randomIndex));
    list2.set(randomIndex, temp);
}
```

### Step 4: Output the Randomized ArrayLists
Output the randomized ArrayLists to the console.

```
System.out.println("Randomized List 1: " + list1);
System.out.println("Randomized List 2: " + list2);
```
