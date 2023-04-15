---
title: Organize an arraylist of custom objects according to a specified property
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Collections.sort() method, passing a Comparator that compares the desired property of the custom objects.
---

**Contents**

[TOC]

### Implement Comparable Interface

The most common way to sort an ArrayList of custom objects is to implement the Comparable interface and override the compareTo() method. 

In the compareTo() method, you can define the sorting logic by comparing the property of the objects. For example, if you want to sort the ArrayList based on the name property, you can do something like this:

```java
public class Person implements Comparable<Person> {
    private String name;
    private int age;

    // getters and setters

    @Override
    public int compareTo(Person o) {
        return this.name.compareTo(o.getName());
    }
}
```

### Use Comparator

Alternatively, you can use the Comparator interface to sort the ArrayList of custom objects.

The Comparator interface provides a compare() method that takes two objects and compares their properties. For example, if you want to sort the ArrayList based on the age property, you can do something like this:

```java
public class PersonComparator implements Comparator<Person> {
    @Override
    public int compare(Person o1, Person o2) {
        return o1.getAge() - o2.getAge();
    }
}
```

### Sort the ArrayList

Once you have implemented the Comparable or Comparator interface, you can sort the ArrayList of custom objects using the Collections.sort() method.

For example, if you want to sort the ArrayList based on the name property, you can do something like this:

```java
Collections.sort(personList);
```

If you want to sort the ArrayList based on the age property, you can do something like this:

```java
Collections.sort(personList, new PersonComparator());
```

### Conclusion

In conclusion, to sort an ArrayList of custom objects, you can either implement the Comparable interface and override the compareTo() method, or use the Comparator interface to define the sorting logic. Once you have implemented the Comparable or Comparator interface, you can sort the ArrayList using the Collections.sort() method.
