---
title: Example of using group layers in Aspose.PSD for Java
weight: 100
type: docs
description: Using of Group Layer of PSD File via Java
keywords: [layer group, group layer, add layer to group, psd api, java, code sample]
url: java/psd-group-layer/
---

## **Overview**

Utilizing group layers in Aspose.PSD for Java enhances your ability to manage and organize layers within a PSD image effectively. Group layers, also referred to as folder layers, enable you to consolidate multiple layers and apply transformations or effects collectively.

To begin, create a new PSD image using the PsdImage.create() method. Then, initialize a new LayerGroup object via the addLayerGroup method of the PsdImage object. Provide the desired name for the group layer ("Folder"), specify the insertion index (0), and set a boolean flag indicating its visibility (True).

Subsequently, create two Layer objects and set their display names using the setDisplayName method. Add these layers to the group layer using the addLayer method.

To access the layers within the group, utilize the layers property of the LayerGroup object. Confirm that the display names of the first and second layers in the group are "Layer 1" and "Layer 2" respectively.

Once you've manipulated the group layers, save the modified PSD image utilizing the save method of the PsdImage object.

This serves as a fundamental example to help you get acquainted with working with group layers using Aspose.PSD for Java. The library offers a plethora of advanced features for layer manipulation and transformation within PSD images. For further details and examples on leveraging group layers and other functionalities of the library, refer to the Aspose.PSD for Java documentation.

To work with group layers in Aspose.PSD for Java, utilize the LayerGroup class. Below is a code snippet illustrating how to create a group layer, add layers to it, and save the modified PSD image.

Please refer to the complete example provided.

## **Example**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}