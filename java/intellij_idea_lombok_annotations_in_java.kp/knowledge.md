---
title: Intellij idea does not recognize lombok annotations during compilation
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Intellij IDEA requires the annotation processor to be enabled in order for Lombok annotations to compile.
---

**Contents**

[TOC]

## Intellij Idea
Intellij Idea is an integrated development environment (IDE) for Java development. It provides users with a comprehensive set of tools to develop and debug Java applications.

## Lombok Annotations
Lombok is a library which provides a set of annotations to reduce boilerplate code in Java. It provides features such as automatic generation of getters, setters, equals, hashCode, and toString methods.

## Problem
When using Lombok annotations in Intellij Idea, the annotations do not compile. This is because Intellij Idea does not recognize the Lombok annotations and thus does not generate the corresponding code.

## Solution
In order to make Lombok annotations work in Intellij Idea, the Lombok plugin must be installed. The plugin will enable Intellij Idea to recognize the Lombok annotations and generate the corresponding code.
