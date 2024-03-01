---
title: Example of using group layers in Aspose.PSD for Python
weight: 100
type: docs
description: Using of Group Layer of PSD File via Python
keywords: [layer group, group layer, add layer to group, psd api, python, code sample]
url: python-net/psd-group-layer/
---

## **Overview**

Working with group layers in Aspose.PSD for Python is a powerful feature that allows you to organize and manipulate layers within a PSD image. Group layers, also known as folder layers, provide a way to group multiple layers together and apply transformations or effects to the entire group.

In this example, we first create a new PSD image using the PsdImage.create method. Then, we create a new LayerGroup object using the add_layer_group method of the PsdImage object. We provide the name of the group layer ("Folder"), the index at which it should be inserted (0), and a boolean flag indicating whether the group layer should be visible (True).

Next, we create two Layer objects and set their display names using the display_name property. We add these layers to the group layer using the add_layer method.

Finally, we can access the layers within the group using the layers property of the LayerGroup object. In the example, we assert that the display names of the first and second layers in the group are "Layer 1" and "Layer 2" respectively.

After manipulating the group layers, we can save the modified PSD image using the save method of the PsdImage object.

This is just a basic example to get you started with working with group layers using Aspose.PSD for Python. The library provides many more advanced features for manipulating and transforming layers within PSD images. You can refer to the Aspose.PSD for Python documentation for more details and examples on working with group layers and other features of the library.

To work with group layers in Aspose.PSD for Python, you can use the LayerGroup class. Here is an example code snippet that demonstrates how to create a group layer, add layers to it, and save the modified PSD image.

Please check full example.

## **Example**
	{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-psd-group-layer.py" >}}