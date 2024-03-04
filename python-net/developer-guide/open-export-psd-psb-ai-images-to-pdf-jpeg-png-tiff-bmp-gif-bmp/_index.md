---
title: Open PSD, PSB and AI files and export them to PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Example PSD, PSB and AI file export to other formats
keywords: [open psd, open ai, open psb, export to png, export to pdf, export to jpeg, export to tiff, psd api, python, code sample]
url: python-net/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Overview**
To convert PSD, PSB, and AI files to different formats, you can use the Aspose.PSD library in Python. This library provides various options and settings to customize the conversion process.

First, you need to import the necessary classes and modules from the Aspose.PSD library. Make sure you have installed the library before running the code.

In this code, we define various options for different formats, such as PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB, and PSD. These options allow you to customize the output file according to your requirements.

Next, we define a dictionary formats that maps file extensions to their respective save options.

To convert a PSD file to other formats, you need to load the PSD file using PsdImage.load() and then iterate through the formats dictionary. For each format, specify the output file name and save the image using the image.save() method.

Similarly, to convert an AI file to other formats, load the AI file using AiImage.load() and iterate through the formats dictionary. Specify the output file name and save the image using the image.save() method.

Make sure to provide the correct file paths for the source PSD and AI files.

That's it! You can now use this code to convert PSD, PSB, and AI files to various formats using Aspose.PSD for Python.

Please check full example.

## **Example**
{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}