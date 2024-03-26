---
title: Open PSD, PSB and AI files and export them to PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Example PSD, PSB and AI file export to other formats
keywords: [open psd, open ai, open psb, export to png, export to pdf, export to jpeg, export to tiff, psd api, java, code sample]
url: java/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Overview**
To convert PSD, PSB, and AI files to different formats using Java, you can utilize the Aspose.PSD library. Here's an overview of the steps involved:

- Import the necessary classes and modules from the Aspose.PSD library.

- Define various options for different formats such as PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB, and PSD.

- Create a dictionary that maps file extensions to their respective save options.

- Load the PSD file using PsdImage.load() and iterate through the formats dictionary to save the image in each desired format.

- Similarly, load the AI file using AiImage.load() and iterate through the formats dictionary to save the image in each desired format.

Ensure to provide correct file paths for the source PSD and AI files.
That's the general procedure for converting PSD, PSB, and AI files to various formats using Aspose.PSD for Java.

Please check full example.

## **Example**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.java" >}}