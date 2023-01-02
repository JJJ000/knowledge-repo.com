---
title: Is it possible to include comments in JSON? 
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/thumbnail.png
created_at: 2022-12-30 00:00:00
updated_at: 2022-12-31 00:00:00
tldr: No, it is not possible to include comments in a JSON file or document. If you want to include comments in your data, you can use another format that does support comments, such as XML or YAML.
---

**Contents**

[TOC]

### Is it possible to include comments in JSON?

No, it is not possible to include comments in a JSON file or document. JSON (JavaScript Object Notation) is a lightweight data interchange format that is designed to be easy for humans to read and write and easy for machines to parse and generate. It is based on a subset of the JavaScript programming language, but it is a language-independent data format. JSON does not support comments, because comments are not necessary for the JSON data to be interpreted correctly and they add extra characters that take up space and increase the size of the file. Instead of using comments, you can use white space, indentation, and line breaks to make the structure of your JSON data more readable for humans.

### Are there any good work-arounds?

If you want to include comments in your data, you can use another format that does support comments, such as XML or YAML. XML (Extensible Markup Language) is a markup language that is commonly used for storing and transporting data. It allows you to add comments using the `<!-- -->` syntax. For example:

```XML
<!-- This is a comment in XML -->
<root>
  <element>Some data</element>
</root>
```

YAML (YAML Ain't Markup Language) is a human-readable data serialization language that is commonly used for configuration files, log files, and in applications where data is being stored or transmitted. You can add comments in YAML by starting the line with a `#` character. For example:

```YAML
# This is a comment in YAML
root:
  element: Some data
```

### Is there a work-around based on JSON?

If you are working with a JSON file and you want to include comments for your own reference or to make the structure of the data easier to understand, you can consider using a text editor or an integrated development environment (IDE) that has support for syntax highlighting and code folding. Many text editors and IDEs allow you to add annotations or notes to your code using special symbols or keywords, such as `TODO`, `FIXME`, or `NOTE`. This can help you to organize and document your code without actually modifying the JSON data.

Another approach is to use a preprocessor or a transpiler that can transform your JSON data into another format that supports comments, such as XML or YAML, and then transform it back into JSON before it is used in your application. For example, you can use a tool like JsonML (JSON Markup Language) to transform your JSON data into an XML-like syntax that supports comments, and then use a tool like xml2json to transform it back into JSON. This can allow you to add comments to your JSON data and keep them separate from the actual data, while still being able to use the JSON data in your application.

Keep in mind, however, that using a preprocessor or a transpiler can add an extra step to your workflow and increase the complexity of your codebase. It is important to weigh the benefits and drawbacks of using a workaround like this before deciding whether it is the right solution for your needs.
