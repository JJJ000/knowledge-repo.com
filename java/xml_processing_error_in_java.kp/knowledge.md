---
title: Processing instructions with targets that match 'xml' are not permitted
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: XML processing instructions are not allowed in Java.
---

**Contents**

[TOC]

## What is a Processing Instruction?
A processing instruction (PI) is an instruction in an XML document that is not part of the document’s content. It is used to pass information to a program that is used to process the document. Processing instructions are typically used to specify the type of software that should be used to process the document.

## Why is the Processing Instruction Target Matching "[xX][mM][lL]" Not Allowed in Java?
Processing instructions are not allowed in Java because they are not part of the Java language. Java does not support XML processing instructions, so any attempt to use them will result in an error.

## What is an Alternative to Processing Instructions in Java?
An alternative to processing instructions in Java is to use annotations. Annotations are a way to provide additional information about a program element, such as a class, method, or field. Annotations are specified using the @ symbol and can be used to provide information about the program element that is not part of the actual code.
