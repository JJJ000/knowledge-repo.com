---
title: What is the equivalent of a c# Java hashmap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The equivalent of a Java HashMap in C# is a Dictionary.
---

**Contents**

[TOC]

1. **Creating a HashMap**

C#: 
```
Dictionary<int, string> myDict = new Dictionary<int, string>();
```

Java:
```
HashMap<Integer, String> myMap = new HashMap<>();
```

2. **Adding Elements**

C#: 
```
myDict.Add(1, "first element");
myDict.Add(2, "second element");
```

Java:
```
myMap.put(1, "first element");
myMap.put(2, "second element");
```

3. **Retrieving Elements**

C#: 
```
string element = myDict[1];
```

Java:
```
String element = myMap.get(1);
```

4. **Removing Elements**

C#: 
```
myDict.Remove(1);
```

Java:
```
myMap.remove(1);
```
