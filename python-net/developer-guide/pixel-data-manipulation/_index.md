---
title: Pixel Data Manipulation using Aspose.PSD for Python
weight: 100
type: docs
description: Example of how to directly and rapidly fast update raw pixel data using PSD Python API
keywords: [edit pixels, edit psd, edit layer, raw data manipulation, edit psd data, psd api, python, code sample]
url: python-net/pixel-data-manipulation/
---

## **Introduction**
Aspose.PSD is a powerful library that allows you to work with Adobe Photoshop files (PSD) in Python. In this article, we will explore how to manipulate pixel data in a PSD file using Aspose.PSD.

## **Overview**
The provided code demonstrates how to create a PSD file, add the new layer for it and then manipulate the pixel data directly, and save the modified image.

Importing Required Modules: The first step is to import the necessary modules. We import the BytesIO module from the io library, as well as the PsdImage and Layer classes from the aspose.psd.fileformats.psd and aspose.psd.fileformats.psd.layers modules respectively.

Next, we define the input and output file paths. 

Opening the Input File as a Stream: We open the input file as a stream using the open function and the "rb" mode. The buffering argument is set to 0 to disable buffering. The file content is read into a BytesIO stream and the stream is set to the beginning using stream.seek(0).

We create a PSD layer object by passing the stream to the Layer class constructor.

We create a new PSD image using the PsdImage class constructor and provide the width and height of the layer as arguments.

We assign the layer to the layers property of the PSD image using the assignment operator (=).

To manipulate the pixel data, we first load the ARGB32 pixels from the layer using the load_argb_32_pixels method. We store the result in the pixels variable.

Next, we define a range of indices (pixelsRange) based on the length of the pixels array. We iterate over the indices and check if an index is divisible by 5. If it is, we set the pixel value at that index to 500000. So, we just want to create some repeating pattern. You can change pixels data as you want.

Then we save the modified pixel data back to the layer using the save_argb_32_pixels method.

Finally, we save the PSD image to the output file using the save method.

In this article, we have explored how to manipulate pixel data in a PSD file using Aspose.PSD for Python. By understanding the provided code, you can perform various pixel-level operations, such as modifying pixels based on certain conditions. Aspose.PSD provides a comprehensive set of features for working with PSD files programmatically, making it a valuable tool for image manipulation tasks in Python.

Please note that the provided code assumes that you have already installed the Aspose.PSD library and its dependencies. You can find more information on how to install and use Aspose.PSD for Python in the official documentation.

Please check full example.

## **Example**
	{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-pixel-data-manipulation.py" >}}