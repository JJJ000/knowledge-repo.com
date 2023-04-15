---
title: What is the most efficient way to format xml using java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the javax.xml.transform.Transformer class to pretty print XML from Java.
---

**Contents**

[TOC]

### Using JAXP

JAXP (Java API for XML Processing) is an interface which provides a standard way to process XML documents. It provides an API for parsing, transforming, validating and querying XML documents. To pretty print XML using JAXP, the following steps should be taken:

1. Create a `javax.xml.transform.TransformerFactory` object.
2. Create a `javax.xml.transform.Transformer` object from the factory.
3. Set the output properties of the transformer to indent the XML.
4. Create a `javax.xml.transform.Source` object from the XML document.
5. Create a `javax.xml.transform.Result` object to write the output.
6. Use the `transformer.transform()` method to transform the source to the result.

### Using XMLUnit

XMLUnit is a Java library which provides a set of assertions to verify the structure and content of an XML document. It also provides a `PrettyPrinter` class which can be used to pretty print XML. To pretty print XML using XMLUnit, the following steps should be taken:

1. Create an instance of `org.xmlunit.util.PrettyPrinter` with the desired output settings.
2. Create a `org.xmlunit.builder.Input` object from the XML document.
3. Use the `PrettyPrinter.getResult()` method to get a `javax.xml.transform.Result` object.
4. Use the `PrettyPrinter.transform()` method to pretty print the XML.

### Using DOM

DOM (Document Object Model) is an interface which provides a standard way to access and manipulate XML documents. To pretty print XML using DOM, the following steps should be taken:

1. Create a `org.w3c.dom.Document` object from the XML document.
2. Create a `javax.xml.transform.TransformerFactory` object.
3. Create a `javax.xml.transform.Transformer` object from the factory.
4. Set the output properties of the transformer to indent the XML.
5. Create a `javax.xml.transform.dom.DOMSource` object from the document.
6. Create a `javax.xml.transform.stream.StreamResult` object to write the output.
7. Use the `transformer.transform()` method to transform the source to the result.

### Using StAX

StAX (Streaming API for XML) is an interface which provides a standard way to read and write XML documents. To pretty print XML using StAX, the following steps should be taken:

1. Create a `javax.xml.stream.XMLOutputFactory` object.
2. Create a `javax.xml.stream.XMLStreamWriter` object from the factory.
3. Set the output properties of the writer to indent the XML.
4. Create a `javax.xml.stream.XMLStreamReader` object from the XML document.
5. Use the `writer.write()` method to write the XML.
6. Use the `writer.flush()` method to flush the output.
