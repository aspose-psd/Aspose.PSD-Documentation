---
title: Smart Object Update and Export using Aspose.PSD for Python
weight: 100
type: docs
description: Examples of how to use Smart Objects in PSD File
keywords: [smart object, smart layer, export smart object, expport smart layer, update smart object, update smart layer, psd api, python, code sample]
url: python-net/smart-object-update/
---

## **Overview**


**Updating and Exporting Smart Object Layers in PSD Files using Aspose.PSD for Python**

Smart Object Layers in PSD files allow you to embed and manipulate external images within your Photoshop designs. With Aspose.PSD for Python, you can easily update and export Smart Object Layers, providing you with powerful capabilities for image editing and manipulation.

In this article, we will walk through a step-by-step guide on how to update and export Smart Object Layers using Aspose.PSD for Python.

Shape Layers are an important feature in Aspose.PSD for Python that allow you to create and manipulate layers in non-destructive way within a PSD image. 

**Example Scenario**
Let's assume we have a PSD file named "new_panama-papers-8-trans4.psd" that contains a Smart Object Layer. We want to update the content of the Smart Object Layer by inverting the image and then export the modified PSD file.

1. Load the PSD File
First, we need to load the PSD file using the Image.load method from the Aspose.PSD library. This will give us access to the layers within the PSD file.

2. Export the Content of the Smart Object Layer
To export the content of the Smart Object Layer, we can use the export_contents method of the SmartObjectLayer class. This method allows us to save the embedded image as a separate file.

3. Manipulate the Smart Object Layer
Next, let's manipulate the content of the Smart Object Layer. For example, we can invert the image by using the invert_image function.

4. Update the Modified Content
After manipulating the Smart Object Layer, we need to update the modified content using the update_all_modified_content method of the smart_object_provider class. This ensures that the changes are applied to the respective layers.

5. Save the Modified PSD File
Finally, we can save the modified PSD file with the updated Smart Object Layer using the save method and specifying the PsdOptions for the desired format and options.

** Conclusion **
In this article, we learned how to update and export Smart Object Layers in PSD files using Aspose.PSD for Python. By following the provided steps, you can easily manipulate and export the content of Smart Object Layers, opening up a wide range of possibilities for image editing and customization.

Aspose.PSD for Python provides a comprehensive set of features and APIs for working with PSD files, making it a powerful tool for any Python developer working with Photoshop designs.

To learn more about Aspose.PSD for Python and explore its capabilities, please refer to the official documentation and API reference.

Please check full example.

## **Example**
{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-psd-smart-object-update.py" >}}