---
title: How can I parse xml as a string in Java instead of a file?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the javax.xml.parsers.DocumentBuilder.parse(InputSource) method to parse an XML String.
---

**Contents**

[TOC]

### Using DOM Parser

DOM Parser is an API that parses an XML document into a tree-like structure in memory and provides access to the content of XML document.

To parse an XML string using DOM parser, the following steps are to be followed:

1. Create a DocumentBuilderFactory object.
2. Create a DocumentBuilder object from the DocumentBuilderFactory.
3. Create a StringReader object from the XML string.
4. Parse the XML string using the parse() method of the DocumentBuilder object, passing the StringReader object as an argument.
5. Get the root element of the document using the getDocumentElement() method of the Document object.
6. Navigate through the tree structure to access the elements and their content.

### Using SAX Parser

SAX Parser is an event-driven parser for XML documents.

To parse an XML string using SAX parser, the following steps are to be followed:

1. Create a SAXParserFactory object.
2. Create a SAXParser object from the SAXParserFactory.
3. Create an InputSource object from the XML string.
4. Parse the XML string using the parse() method of the SAXParser object, passing the InputSource object as an argument.
5. Create a DefaultHandler object to handle the SAX events.
6. Register the DefaultHandler object with the SAXParser object using the setContentHandler() method.
7. Parse the XML string using the parse() method of the SAXParser object, passing the InputSource object as an argument.
8. Handle the SAX events using the methods of the DefaultHandler object.
