---
title: คำอธิบายการจัดอันดับ Aspose.PSD for .NET 23.8
type: docs
weight: 50
url: /th/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีประวัติการอัปเดตสำหรับ [Aspose.PSD for .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **รหัส**     | **สรุป**                                                                                                  | **ประเภท** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | เพิ่มประเภทใหม่ของการโค้ง (Flag) | คุณลักษณะ |
| PSDNET-1621 | เพิ่มประเภทใหม่ของการโค้ง: โค้งขึ้น, โค้งลง, ก้อนทรงกลม | คุณลักษณะ |
| PSDNET-1682 | ดำเนินการเพิ่มเมธอดใหม่ PsdImage.AddPosterizeAdjustmentLayer เพื่อเพิ่มเลเยอร์การปรับ Posterize ใหม่ | คุณลักษณะ |
| PSDNET-913  | ข้อมูล PSD สูญหายเมื่อเปิดและบันทึกเฉพาะ | ข้อผิดพลาด     |
| PSDNET-1352 | การโหลดภาพล้มเหลว | ข้อผิดพลาด     |
| PSDNET-1553 | การโหลดภาพล้มเหลว: ไม่สามารถแปลงวัตถุประสงค์ชนิด UnknownStructure เป็นชนิด DescriptorStructure ได้ | ข้อผิดพลาด     |
| PSDNET-1631 | ไฟล์ที่เปลี่ยนแปลงในไลบรารีบุคคนที่สามทำให้ไฟล์ PSD เสียหายแต่สามารถเปิดใน Photoshop ได้ | ข้อผิดพลาด     |


## **การเปลี่ยนแปลงของ API สาธารณะ**
# **API เพิ่มเติม:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **API ที่ถูกลบ:**
- ไม่มี


## **ตัวอย่างการใช้งาน:**

**PSDNET-913. ข้อมูล PSD สูญหายเมื่อเปิดและบันทึกเฉพาะ**

{{< highlight csharp >}}
string src = "Original file.psd";
string outputPsd = "out_Original file.psd";
string outputPng = "out_Original file.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. การโหลดภาพล้มเหลว**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. การโหลดภาพล้มเหลว: ไม่สามารถแปลงวัตถุประสงค์ชนิด UnknownStructure เป็นชนิด DescriptorStructure ได้**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // ควรโหลดได้ถูกต้อง
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. ไฟล์ที่เปลี่ยนแปลงในไลบรารีบุคคนที่สามทำให้ไฟล์ PSD เสียหายแต่สามารถเปิดใน Photoshop ได้**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. เพิ่มประเภทใหม่ของการโค้ง (Flag)**

{{< highlight csharp >}}
string sourceFile = "flag_warp.psd";
string outputFile = "flag_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. เพิ่มประเภทใหม่ของการโค้ง: โค้งขึ้น, โค้งลง, ก้อนทรงกลม**

{{< highlight csharp >}}
string sourceFileArcUpper = "arc_upper_warp.psd";
string sourceFileArcLower = "arc_lower_warp.psd";
string sourceFileBulge =  "bulge_warp.psd";

string outputFileArcUpper ="ArcUpper_export.png";
string outputFileArcLower = "ArcLower_export.png";
string outputFileBulge = "Bulge_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. ดำเนินการเพิ่มเมธอดใหม่ PsdImage.AddPosterizeAdjustmentLayer เพื่อเพิ่มเลเยอร์การปรับ Posterize ใหม่**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// ตรวจสอบการบันทึกเปลี่ยนแปลง
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "วัตถุไม่เท่ากัน.");
    }
}
{{< /highlight >}}
