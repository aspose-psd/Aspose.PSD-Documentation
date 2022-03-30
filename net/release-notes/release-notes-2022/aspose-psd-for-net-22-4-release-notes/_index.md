---
title: Aspose.PSD for .NET 22.4 - Release Notes
type: docs
weight: 90
url: /net/aspose-psd-for-net-22-4-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for .NET 22.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-1123|Add support of Sha256 License|Enhancement|
|PSDNET-1107|Positioning multi-line text does not match the result in Photoshop|Bug|
|PSDNET-1113|The issue with loading PSD file on text resource data parsing|Bug|
|PSDNET-1129|Incorrect position of the custom pattern after saving as PSD|Bug|


## **Public API Changes**
# **Added APIs:**
- T:Aspose.PSD.FileFormats.Psd.JustificationMode
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Left
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Right
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Center


# **Removed APIs:**
- None


## **Usage examples:**

**PSDNET-1107. Positioning multi-line text does not match the result in Photoshop**

{{< highlight csharp >}}
string src = "source1107.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var image = (PsdImage)Image.Load(src))
{ 
   var txtLayer = image.AddTextLayer("Text line1\rText line2\rText line3", new Rectangle(200, 200, 500, 500));
   var portions = txtLayer.TextData.Items;

   portions[0].Paragraph.Justification = JustificationMode.Left;
   portions[1].Paragraph.Justification = JustificationMode.Right;
   portions[2].Paragraph.Justification = JustificationMode.Center;

   txtLayer.TextData.UpdateLayerData();

   image.Save(outputPsd);
   image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1113. The issue with loading PSD file on text resource data parsing**

{{< highlight csharp >}}
string sourceFile = "input.psd";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    // Loaded successfully.
}
{{< /highlight >}}

**PSDNET-1129. Incorrect position of the custom pattern after saving as PSD**

{{< highlight csharp >}}
string sourceFile = "input_1129.psd";
string outputPsd = "out_psdnet1129.psd";
string outputPng = "out_psdnet1129.png";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
