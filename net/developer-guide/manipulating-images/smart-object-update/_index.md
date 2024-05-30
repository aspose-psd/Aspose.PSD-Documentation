---
title: Smart Object Update and Export using Aspose.PSD for С#
weight: 100
type: docs
description: Examples of how to use Smart Objects in PSD File
keywords: [smart object, smart layer, export smart object, expport smart layer, update smart object, update smart layer, psd api, C#, csharp, code sample]
url: net/smart-object-update/
---

## Overview

**Updating and Exporting Smart Object Layers in PSD Files using Aspose.PSD for C#**

Smart Object Layers in PSD files allow you to embed and manipulate external images within your Photoshop designs. With Aspose.PSD for C#, you can easily update and export Smart Object Layers, providing powerful capabilities for image editing and manipulation.

This article walks through a step-by-step guide on how to update and export Smart Object Layers using Aspose.PSD for C#.

**Example Scenario**: Let's assume we have a PSD file named "new_panama-papers-8-trans4.psd" that contains a Smart Object Layer. We want to update the content of the Smart Object Layer by inverting the image and then export the modified PSD file.

### Steps:

1. **Load the PSD File**:
   Load the PSD file using the `Image.Load` method from the Aspose.PSD library. This gives access to the layers within the PSD file.

2. **Export the Content of the Smart Object Layer**:
   Use the `ExportContents` method of the `SmartObjectLayer` class to save the embedded image as a separate file.

3. **Manipulate the Smart Object Layer**:
   Manipulate the content of the Smart Object Layer. For example, invert the image using an appropriate function.

4. **Update the Modified Content**:
   After manipulating the Smart Object Layer, update the modified content using the `UpdateAllModifiedContent` method of the `SmartObjectProvider` class. This ensures the changes are applied to the respective layers.

5. **Save the Modified PSD File**:
   Save the modified PSD file with the updated Smart Object Layer using the `Save` method and specifying the `PsdOptions` for the desired format and options.

### Conclusion

This article explained how to update and export Smart Object Layers in PSD files using Aspose.PSD for C#. By following these steps, you can easily manipulate and export the content of Smart Object Layers, enabling a wide range of possibilities for image editing and customization.

Aspose.PSD for C# provides a comprehensive set of features and APIs for working with PSD files, making it a powerful tool for any C# developer working with Photoshop designs.

To learn more about Aspose.PSD for C# and explore its capabilities, please refer to the [official documentation and API reference](https://docs.aspose.com/psd/net/).

## Example

```csharp
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.SmartObjects;
using Aspose.PSD.ImageOptions;

class Program
{
    static void Main()
    {
         string source = "new_panama-papers-8-trans4.psd";
         string exportContentPath = "export_content.jpg";
         string outputUpdated = "smart_object.psd";

         using (PsdImage im = (PsdImage)Image.Load(source))
         {
             SmartObjectLayer smartLayer = (SmartObjectLayer)im.Layers[0];

             // How to export content of Smart Object
             smartLayer.ExportContents(exportContentPath);

             // Creating Smart Object as a Copy
             SmartObjectLayer newLayer = smartLayer.NewSmartObjectViaCopy();
             newLayer.IsVisible = false;
             newLayer.DisplayName = "Duplicate";

             // Get the content of Smart Object for manipulation
             using (RasterImage innerImage = (RasterImage)smartLayer.LoadContents(null))
             {
                 InvertImage(innerImage);
                 smartLayer.ReplaceContents(innerImage);
             }

             im.SmartObjectProvider.UpdateAllModifiedContent();

             PsdOptions psdOptions = new PsdOptions(im);
             im.Save(outputUpdated, psdOptions);
         }
         
         void InvertImage(RasterImage image)
         {
             int[] pixels = image.LoadArgb32Pixels(image.Bounds);
             for (int i = 0; i < pixels.Length; i++)
             {
                 int pixel = pixels[i];
                 int alpha = pixel & unchecked((int)0xff000000);
                 pixels[i] = (~(pixel & 0x00ffffff)) | alpha;
             }
             image.SaveArgb32Pixels(image.Bounds, pixels);
         }
    }
}
```

For more detailed information and examples, please visit the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).

