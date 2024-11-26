---
title: บันทึกการเผยแพร่ Aspose.PSD สำหรับ .NET 23.1
type: docs
weight: 120
url: /th/net/aspose-psd-for-net-23-1-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการเผยแพร่สำหรับ [Aspose.PSD สําหรับ .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-401|การสนับสนุน vstkResource|คุณลักษณะ|
|PSDNET-1346|เพิ่มคุณสมบัติ BaselineDirection/IsStandardVerticalRomanAlignmentEnabled ที่แก้ไขได้ใน IText interface|คุณลักษณะ|
|PSDNET-181|PSD ไม่ถูกแปลงเป็น JPEG อย่างเหมาะสม|ข้อบกพร่อง|
|PSDNET-958|PSB ถึง PDF ล้มเหลวสำหรับไฟล์ขนาดใหญ่|ข้อบกพร่อง|
|PSDNET-1171|เพิ่มการประมวลผลขอบเขตการตัดผ้าไหมลงในเลเยอร์การปรับปรุง|ข้อบกพร่อง|
|PSDNET-1252|หลังจากการปรับขนาดรูปภาพทั้งหมดและหลังจากการปรับขนาดเลเยอร์เฉพาะ Aspose.PSD ส่งออกข้อยกเว้นในการบันทึกเลเยอร์|ข้อบกพร่อง|


## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsStandardVerticalRomanAlignmentEnabled
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.RoundCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.SquareCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.ButtCap
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.BevelJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.RoundJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.MiterJoin
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineDashOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleMiterLimit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineJoinType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleScaleLock
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleStrokeAdjust
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleBlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleOpacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleResolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleContent
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Levels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.TypeToolKey


# **API ที่ถูกลบ:**
- ไม่มี


## **ตัวอย่างการใช้:**

**PSDNET-181. PSD ไม่ถูกแปลงเป็น JPEG**

{{< highlight csharp >}}
string srcFile = "helicopter.psd";
string outputJpg = "output.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. การสนับสนุน vstkResource**

{{< highlight csharp >}}
string srcFile = "StrokeShapeTest1.psd";
string dstFile = "StrokeShapeTest2.psd";

using (PsdImage image = (PsdImage)Image.Load(srcFile))
{
    Layer layer = image.Layers[1];
    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is VstkResource)
        {
            VstkResource vstkResource = (VstkResource)resource;
            vstkResource.StrokeStyleLineAlignment = StrokePosition.Outside;
            vstkResource.StrokeStyleLineWidth = 20;
        }
    }

    image.Save(dstFile);
}
{{< /highlight >}}

**PSDNET-958. PSB ถึง PDF ล้มเหลวสำหรับไฟล์ขนาดใหญ่**

{{< highlight csharp >}}
string inputPath = "SteveKohli-CarTOP.psb";
string outputPath ="output.pdf";

using (var image = Image.Load(inputPath))
{
    image.Save(outputPath, new PdfOptions());
}
{{< /highlight >}}

**PSDNET-1171. เพิ่มการประมวลผลขอบเขตการตัดผ้าไหมลงในเลเยอร์การปรับปรุง**

{{< highlight csharp >}}
string srcFile = "helicopter_part.psd";
string outputJpg = "output.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1252. หลังจากการปรับขนาดรูปภาพทั้งหมดและหลังจากการปรับขนาดเลเยอร์เฉพาะ Aspose.PSD ส่งออกข้อยกเว้นในการบันทึกเลเยอร์**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string imgFile1 = "img1.png";
string imgFile2 = "img2.png";

var loadOptions = new PsdLoadOptions()
{
    ReadOnlyMode = false,
    LoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // ก่อนอื่น เราจะปรับขนาดรูปภาพทั้งหมด
    image.Resize(110, 90);
    var layers = image.Layers;

    var layerOk = layers[0];
    layerOk.Resize(100, 80);

    var layerException = layers[1];
    layerException.Resize(100, 80);

    // ที่นี่ทุกอย่างจะดี
    layerOk.Save(imgFile1, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    // ตอนนี้ที่นี่ทุกอย่างจะดี
    layerException.Save(imgFile2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });                
}
{{< /highlight >}}

**PSDNET-1346. เพิ่มคุณสมบัติ BaselineDirection/IsStandardVerticalRomanAlignmentEnabled ที่แก้ไขได้ใน IText interface**

{{< highlight csharp >}}
// โค้ดต่อไปนี้แสดงถึงความสามารถในการแก้ไขคุณสมบัติใหม่ IsStandardVerticalRomanAlignmentEnabled
// สิ่งนี้ไม่มีผลต่อการแสดงผลในขณะนี้ แต่เพียงแต่คุณสามารถแก้ไขค่าคุณสมบัติ

string src = "1346test.psd";
string output = "out_1346test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    var textPortion = textLayer.TextData.Items[0];
    if (textPortion.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // อ่านอย่างถูกต้อง
    }
    else
    {
        throw new Exception("การอ่านค่าคุณสมบัติ IsStandardVerticalRomanAlignmentEnabled ไม่ถูกต้อง");
    }

    textPortion.Style.IsStandardVerticalRomanAlignmentEnabled = false;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    var textPortion = textLayer.TextData.Items[0];
    if (!textPortion.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // อ่านอย่างถูกต้อง
    }
    else
    {
        throw new Exception("การอ่านค่าคุณสมบัติ IsStandardVerticalRomanAlignmentEnabled ไม่ถูกต้อง");
    }
}
{{< /highlight >}}
