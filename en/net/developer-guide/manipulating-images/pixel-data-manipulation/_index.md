---
title: Pixel Data Manipulation using Aspose.PSD for C#
weight: 100
type: docs
description: Example of how to directly and rapidly fast update raw pixel data using PSD C# API
keywords: [edit pixels, edit psd, edit layer, raw data manipulation, edit psd data, psd api, C#, csharp, code sample]
url: net/pixel-data-manipulation/
---

## Introduction

Aspose.PSD is a powerful library that allows you to work with Adobe Photoshop files (PSD) in C#. In this article, we will explore how to manipulate pixel data in a PSD file using Aspose.PSD for C#.

## Overview

The provided code demonstrates how to create a PSD file, add a new layer, manipulate the pixel data directly, and save the modified image.

### Steps to Manipulate Pixel Data

1. **Importing Required Modules**:
   Import the necessary modules. You need to import the `PsdImage` and `Layer` classes from the Aspose.PSD library.

2. **Define Input and Output File Paths**:
   Specify the input and output file paths.

3. **Open the Input File as a Stream**:
   Open the input file as a stream using the `FileStream` class in read mode. Create a `PsdImage` object by loading the stream.

4. **Create a New PSD Image**:
   Create a new PSD image using the `PsdImage` constructor and provide the width and height of the layer as arguments.

5. **Assign the Layer to the PSD Image**:
   Assign the layer to the `Layers` property of the PSD image.

6. **Manipulate the Pixel Data**:
   Load the ARGB32 pixels from the layer using the `LoadArgb32Pixels` method. Define a range of indices based on the length of the pixels array and modify the pixel values as needed.

7. **Save the Modified Pixel Data**:
   Save the modified pixel data back to the layer using the `SaveArgb32Pixels` method.

8. **Save the PSD Image**:
   Save the PSD image to the output file using the `Save` method.

### Example

Here’s a code sample demonstrating how to manipulate pixel data using Aspose.PSD for C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### Summary

Aspose.PSD for C# provides a powerful set of features for manipulating pixel data in PSD files. Whether you need to modify pixels based on specific conditions or create complex patterns, Aspose.PSD makes these tasks straightforward and efficient.

For more detailed information and examples, please visit the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).

