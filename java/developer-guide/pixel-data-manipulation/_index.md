---
title: Pixel Data Manipulation using Aspose.PSD for Java
weight: 100
type: docs
description: Example of how to directly and rapidly fast update raw pixel data using PSD Java API
keywords: [edit pixels, edit psd, edit layer, raw data manipulation, edit psd data, psd api, java, code sample]
url: java/pixel-data-manipulation/
---

## **Introduction**
Aspose.PSD is a powerful library that enables Java developers to work with Adobe Photoshop files (PSD). In this guide, we'll delve into manipulating pixel data within a PSD file using Aspose.PSD for Java.

## **Overview**
This guide outlines the steps to manipulate pixel data in a PSD file using Aspose.PSD for Java.

- Import Necessary Modules: Begin by importing the required modules. Import the necessary classes and packages to facilitate PSD file manipulation.

- Define Input and Output Paths: Define the file paths for the input PSD file and the desired output location.

- Open Input File as Stream: Open the input PSD file as a stream, ensuring to handle it appropriately for reading.

- Create PSD Layer Object: Instantiate a PSD layer object from the opened stream.

- Create New PSD Image: Create a new PSD image, specifying the dimensions of the layer.

- Assign Layer to PSD Image: Associate the layer with the PSD image.

- Load Pixel Data: Load the pixel data from the layer, enabling subsequent manipulation.

- Manipulate Pixel Data: Perform desired manipulations on the loaded pixel data. This may involve iterating through the pixels and applying transformations as necessary.

- Save Modified Pixel Data: Save the modified pixel data back to the layer.

- Save PSD Image: Save the PSD image with the updated pixel data to the specified output location.

By following these steps, you can effectively manipulate pixel data within a PSD file using Aspose.PSD for Java. This library offers comprehensive functionality for programmatically working with PSD files, empowering Java developers in image manipulation tasks.
Please ensure you have installed the Aspose.PSD library and its dependencies before proceeding. Refer to the official documentation for detailed installation instructions and usage guidelines.

Please refer to the complete example provided below.

## **Example**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-pixel-data-manipulation.java" >}}