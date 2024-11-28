---
title: Smart Object Update and Export using Aspose.PSD for Java
weight: 100
type: docs
description: Examples of how to use Smart Objects in PSD File
keywords: [smart object, smart layer, export smart object, expport smart layer, update smart object, update smart layer, psd api, java, code sample]
url: java/smart-object-update/
---

## **Overview**

**Updating and Exporting Smart Object Layers in PSD Files using Aspose.PSD for Java**

Smart Object Layers in PSD files enable you to embed and manipulate external images within your Photoshop designs. Leveraging Aspose.PSD for Java, you can seamlessly update and export Smart Object Layers, empowering you with robust functionalities for image editing and manipulation.

This guide will walk you through a detailed tutorial on how to update and export Smart Object Layers using Aspose.PSD for Java.

Shape Layers represent a crucial feature in Aspose.PSD for Java, facilitating the creation and manipulation of layers within a PSD image in a non-destructive manner.

**Example Scenario**
Let's consider a PSD file named "new_panama-papers-8-trans4.psd" containing a Smart Object Layer. Our objective is to update the content of the Smart Object Layer by inverting the image and subsequently export the modified PSD file.

1. Load the PSD File
Begin by loading the PSD file using the Image.load() method from the Aspose.PSD library. This grants access to the layers embedded within the PSD file.

2. Export the Content of the Smart Object Layer
To export the content of the Smart Object Layer, utilize the exportContents method of the SmartObjectLayer class. This method facilitates saving the embedded image as a distinct file.

3. Manipulate the Smart Object Layer
Proceed to manipulate the content of the Smart Object Layer. For instance, you can invert the image using the invertImage function.

4. Update the Modified Content
Upon manipulating the Smart Object Layer content, update the modified content using the updateAllModifiedContent method of the SmartObjectProvider class. This ensures the application of changes to the corresponding layers.

5. Save the Modified PSD File
Finally, save the modified PSD file with the updated Smart Object Layer using the save method and specifying the PsdOptions for the desired format and options.

** Conclusion **
This tutorial elucidated the process of updating and exporting Smart Object Layers in PSD files using Aspose.PSD for Java. By adhering to the outlined steps, you can effortlessly manipulate and export the content of Smart Object Layers, unveiling a plethora of possibilities for image editing and customization.

Aspose.PSD for Java offers a comprehensive suite of features and APIs for PSD file manipulation, rendering it an indispensable tool for any Java developer working with Photoshop designs.

To delve deeper into Aspose.PSD for Java and explore its functionalities, kindly consult the official documentation and API reference.

Please find the full example below.

## **Example**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-object-update.java" >}}