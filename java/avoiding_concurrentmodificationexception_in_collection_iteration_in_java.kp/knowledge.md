---
title: Looping through a collection and safely removing items without causing a concurrentmodificationexception
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use an Iterator to iterate through the Collection, and use the Iterator`s remove() method to remove objects from the Collection.
---

**Contents**

[TOC]

**Using an Iterator**

The most common approach is to use an Iterator. Iterator provides a convenient way to iterate over a Collection while being able to remove elements without causing a ConcurrentModificationException.

1. Create an Iterator object for the Collection:
    ```java
    Iterator<Object> iterator = collection.iterator();
    ```
2. Iterate through the Collection using the Iterator’s hasNext() and next() methods:
    ```java
    while(iterator.hasNext()) {
        Object obj = iterator.next();
        // Do something with obj
    }
    ```
3. Remove elements from the Collection using the Iterator’s remove() method:
    ```java
    while(iterator.hasNext()) {
        Object obj = iterator.next();
        if (shouldRemove(obj)) {
            iterator.remove();
        }
    }
    ```

**Using a ListIterator**

Another way to avoid ConcurrentModificationException when removing elements in a loop is to use a ListIterator. This approach is similar to using an Iterator, but ListIterator provides additional methods that allow you to move backward and forward in the list.

1. Create a ListIterator object for the List:
    ```java
    ListIterator<Object> listIterator = list.listIterator();
    ```
2. Iterate through the List using the ListIterator’s hasNext() and next() methods:
    ```java
    while(listIterator.hasNext()) {
        Object obj = listIterator.next();
        // Do something with obj
    }
    ```
3. Remove elements from the List using the ListIterator’s remove() method:
    ```java
    while(listIterator.hasNext()) {
        Object obj = listIterator.next();
        if (shouldRemove(obj)) {
            listIterator.remove();
        }
    }
    ```

**Using a for-each loop**

Another approach is to use a for-each loop. This approach is simpler than using an Iterator or ListIterator, but it does not allow you to remove elements from the Collection.

1. Iterate through the Collection using the for-each loop:
    ```java
    for (Object obj : collection) {
        // Do something with obj
    }
    ```
2. If you need to remove elements from the Collection, create a new Collection and add the elements that should not be removed:
    ```java
    Collection<Object> newCollection = new ArrayList<>();
    for (Object obj : collection) {
        if (!shouldRemove(obj)) {
            newCollection.add(obj);
        }
    }
    ```
3. Replace the original Collection with the new Collection:
    ```java
    collection = newCollection;
    ```
