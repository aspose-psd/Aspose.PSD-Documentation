---
title: Aspose.PSD Adapters for .NET 24.4 - Release Notes
type: docs
weight: 100
url: /net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD Adapters for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Key**     | **Summary**                                                          | **Category** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Intial publishing of Aspose.PSD.Adapters.Imaging to Nuget            | Enhancement |


## **Public API Changes**
# **Added APIs:**
- None

# **Removed APIs:**
- None

## **Usage examples:**

Please check [Aspose.PSD.Adapters documentation page](/psd/net/adapters)

**PSDNET-1985. Most complete example of using Aspose.PSD.Adapters**

{{< highlight csharp >}}
// Add enabling of adapters in your init config 
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// additionally enable Exporters
Aspose.PSD.Adapters.Imaging.EnableExporters();

// To work with adapters you need both Aspose.PSD and adaptee Licenses
// Here is how to apply Aspose.PSD License
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Here is example of how to apply Adaptee License for Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Then you can run any code of adapters or PSD or Imaging library

// After this, all these files can be opened by Aspose.PSD without any additional code just use
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // After execution of this code you'll get the PSD File created from WEBP and can apply any Aspose.PSD Filters, Layers and Adjustments including Warp Transformation
}

// You can additionally Create Export Adaptees' Images to PSD Format
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Use Aspose.Imaging API to Edit WEBP file with Imaging-specific features
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Then just use ToPsdImage() method and edit file like PSD with Photoshop-like features including layers, smart filters and smart objects.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Some text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Save the final PSD file using Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// If you don't need to use Loaders or Exporters provided by Adapters just disable them
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}