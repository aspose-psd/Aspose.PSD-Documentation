---
title: Example of using group layers in Aspose.PSD for C#
weight: 100
type: docs
description: Using of Group Layer of PSD File via C#
keywords: [layer group, group layer, add layer to group, psd api, C#, csharp, code sample]
url: net/psd-group-layer/
---

## Overview

Group layers in Aspose.PSD for C# allow for efficient organization and manipulation of layers in a PSD file. By using folder layers, you can group multiple layers together and apply transformations or effects to the entire group.

This example demonstrates creating a new PSD image with `PsdImage.Create`. Then, a new `LayerGroup` object is created using `AddLayerGroup` from the `PsdImage` object. The group layer is named "Folder," inserted at index 0, and set to visible.

Next, two `Layer` objects are created with their `DisplayName` properties set. These layers are added to the group layer using `AddLayer`.

Layers within the group can be accessed via the `Layers` property of the `LayerGroup` object. The example asserts that the first and second layers' display names in the group are "Layer 1" and "Layer 2".

After modifying the group layers, the updated PSD image is saved with the `Save` method of the `PsdImage` object.

This basic example introduces working with group layers using Aspose.PSD for C#. The library offers advanced features for manipulating and transforming layers in PSD files. Refer to the Aspose.PSD for C# documentation for more detailed examples and features.

Here’s a sample code demonstrating group layer usage in Aspose.PSD for C#:

## Example

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

For more detailed information and examples, please visit the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).
