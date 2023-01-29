---
title: What is the distinction between the use of <? super t> and <? extends t> in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: <? super T> allows you to pass in a supertype of T, while <? extends T> allows you to pass in a subtype of T.
---

**Contents**

[TOC]

####What is <? super T>? 
<? super T> is a type parameter that represents the supertype of a given type T. It is used to indicate that a method or constructor can accept a type that is either T or a supertype of T.

####What is <? extends T>? 
<? extends T> is a type parameter that represents the subtype of a given type T. It is used to indicate that a method or constructor can accept a type that is either T or a subtype of T.

####Difference
The main difference between <? super T> and <? extends T> is that <? super T> allows a method or constructor to accept a type that is either T or a supertype of T, while <? extends T> allows a method or constructor to accept a type that is either T or a subtype of T.
