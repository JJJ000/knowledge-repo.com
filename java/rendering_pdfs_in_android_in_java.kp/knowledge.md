---
title: What is the process for displaying a pdf file on an Android device?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use a PDF renderer library such as PdfiumAndroid or MuPDF to render a PDF file in Android in Java.
---

**Contents**

[TOC]

# Section 1: Prepare the PDF File

Before attempting to render a PDF file in Android, the file must be prepared for use. This includes making sure the file is in a supported format, such as Adobe Acrobat Reader (PDF) or Portable Document Format (PDF). Additionally, the file should be optimized for mobile devices, such as reducing the file size and resolution.

# Section 2: Add the Library Dependency

In order to render the PDF file, a library dependency is required. The most popular library for this purpose is the AndroidPdfViewer library. This library is available as an open-source project and can be added to the project with the following Gradle dependency:

```
implementation 'com.github.barteksc:android-pdf-viewer:3.2.0-beta.1'
```

# Section 3: Render the PDF File

Once the library is added, the PDF file can be rendered in the application. This is done by creating a PDFView instance and setting the PDF file to the view. The following example code shows how this is done:

```
PDFView pdfView = findViewById(R.id.pdfView);
pdfView.fromUri(Uri.parse("path/to/pdf/file.pdf"))
      .load();
```

# Section 4: Additional Features

In addition to rendering the PDF file, the AndroidPdfViewer library also provides several additional features. These include the ability to zoom in and out of the PDF, search for text, and navigate to specific pages. These features can be enabled by setting the appropriate flags when creating the PDFView instance. For example, the following code enables the zoom and search features:

```
PDFView pdfView = findViewById(R.id.pdfView);
pdfView.fromUri(Uri.parse("path/to/pdf/file.pdf"))
      .enableSwipe(true)
      .swipeHorizontal(true)
      .enableDoubletap(true)
      .enableAntialiasing(true)
      .load();
```
