---
title: Export Layer Group to image
type: docs
weight: 30
url: /net/export-layer-group-to-image/
---

## **Export Layer Group to image**
Aspose.PSD supports exporting layer groups to images.  For this, the API provides the [LayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) class.

## Example

The following code snippet demonstrates exporting layer groups to images.

```csharp
string outputPsd = "LayerGroup.psd";
string outputPng = "LayerGroup.psd_folder.png";

using (PsdImage psdImage = new PsdImage(100, 100))
{
    // Init background layer
    var bgLayer = FillLayer.CreateInstance(FillType.Color);
    ((IColorFillSettings)bgLayer.FillSettings).Color = Color.Blue;

    // Init regular layers
    byte[] tempBytes = new byte[10 * 10];
    Layer layer1 = new Layer(
    new Rectangle(50, 50, 10, 10), tempBytes, tempBytes, tempBytes, "Layer 1");
    Layer layer2 = new Layer(
        new Rectangle(50, 50, 10, 10), tempBytes, tempBytes, tempBytes, "Layer 2");
    
    // Init and add folder
    LayerGroup layerGroup = psdImage.AddLayerGroup("Folder", 0, true);
    
    // add background to PsdImage
    psdImage.AddLayer(bgLayer);
    
    // add regular layers to folder
    layerGroup.AddLayer(layer1);
    layerGroup.AddLayer(layer2);
    
    // Validate that the layers were added correctly
    System.Diagnostics.Debug.Assert(layerGroup.Layers[0].DisplayName == "Layer 1");
    System.Diagnostics.Debug.Assert(layerGroup.Layers[1].DisplayName == "Layer 2");

    psdImage.Save(outputPsd);
    layerGroup.Save(outputPng, new PngOptions());
}
```

For more detailed information and examples, please visit the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).