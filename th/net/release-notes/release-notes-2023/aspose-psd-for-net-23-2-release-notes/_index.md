---
title: Aspose.PSD for .NET 23.2 - บันทึกการเปลี่ยนแปลง
type: docs
weight: 110
url: /th/net/aspose-psd-for-net-23-2-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการเปลี่ยนแปลงสำหรับ [Aspose.PSD for .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-1359|ปรับแต่งการเรนเดอร์ข้อความเพื่อปรับปริมาณข้อความ การเรนเดอร์ และรองรับได้ดีขึ้น|ปรับปรุง|
|PSDNET-1270|เพิ่มความสามารถในการประมวลผลเอฟเฟค Warp ผ่าน API สาธารณะ|คุณลักษณะ|
|PSDNET-1391|เพิ่มการสนับสนุนการนำไปใช้ตามโหมดชนะสุขและชนะแล้วที่มีจากการตั้งค่าย่อหน้า|คุณลักษณะ|
|PSDNET-912|เปลี่ยนฟอนต์และสีสำหรับ TextLayer PSD|ข้อบกพร่อง|
|PSDNET-1022|การส่งออกข้อความไม่ถูกต้องที่ทดสอบ TextUpdateTests ข้อความหายไป|ข้อบกพร่อง|
|PSDNET-1221|ข้อความขนาดเล็กเพิ่มขาดหายหลังจากการปรับขนาดภาพ PSD ขนาดใหญ่|ข้อบกพร่อง|
|PSDNET-1301|Aspose.Psd for .NET textLayer.UpdateText() พิมพ์ '-' (ขีดล่าง) เป็น underscore อย่างสุ่มๆ สำหรับชุดข้อมูลที่แตกต่างกัน|ข้อบกพร่อง|
|PSDNET-1379|การตั้งค่าความละเอียดไม่ได้ใช้การส่งออกจาก PSD ไปยัง PDF|ข้อบกพร่อง|


## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **API ที่ถูกนำออก:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **ตัวอย่างการใช้:**

**PSDNET-912. เปลี่ยนฟอนต์และสีสำหรับ TextLayer PSD**

{{< highlight csharp >}}
string fontsFolder = "Fonts";
string srcFile = "M1PDTT26052021001.psd";
string outputPsd = "result.psd";
string outputPng = "result.png";

FontSettings.SetFontsFolder(fontsFolder);

using (var image = (PsdImage)Image.Load(srcFile))
{
    TextLayer nameLayer = (TextLayer)image.Layers[9];
    var textPortion = nameLayer.TextData.Items[0];

    textPortion.Text = "MODESTO SR";
    textPortion.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    textPortion.Style.FillColor = Color.Red;

    nameLayer.TextData.UpdateLayerData();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. การส่งออกข้อความไม่ถูกต้องที่ทดสอบ TextUpdateTests ข้อความหายไป**

{{< highlight csharp >}}
string srcFile = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample_.psd";
string outputPng = "TextUpdateComplexKerningExample_.png";

using (var image = (PsdImage)Image.Load(srcFile))
{
    for (int i = 0; i < image.Layers.Length; i++)
    {
        var layer = image.Layers[i] as TextLayer;

        if (layer != null)
        {
            layer.UpdateText("Text is updated");
        }
    }

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. ข้อความขนาดเล็กเพิ่มขาดหายหลังจากการปรับขนาดภาพ PSD ขนาดใหญ่**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. เพิ่มความสามารถในการประมวลผลเอฟเฟค Warp ผ่าน API สาธารณะ**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string pngWarpedExport = "warped.png";
string psdWarpedExport = "warpFile.psd";

var warpLoadOptions = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var image = (PsdImage)Image.Load(sourceFile, warpLoadOptions))
{
    image.Save(pngWarpedExport, new PngOptions());
    image.Save(psdWarpedExport, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd for .NET textLayer.UpdateText() พิมพ์ '-' (ขีดล่าง) เป็น underscore อย่างสุ่มๆ สำหรับชุดข้อมูลที่แตกต่างกัน**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "OUTPUTIMAGE.jpg";

using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers.Where(x => x.IsVisible))
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            switch (layer.Name.Trim().ToUpper())
            {
                case "NAME":
                    textLayer.UpdateText("MR. JACK SMITH");
                    break;
                case "IDNO":
                    textLayer.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNATION":
                    textLayer.UpdateText("OFFICER-001");
                    break;
                case "BLOODGROUP":
                    textLayer.UpdateText("AB-");
                    break;
                case "ADDRESS":
                    textLayer.UpdateText("BLOCK-A, STREET-7, APPT NO - 047, SECTOR-024");
                    break;
                case "PERMADDRESS":
                    textLayer.UpdateText("HOUSE NO - 42, LANE -025, PALM GREENS VIEW HOUSING SOCIETY, SECTOR - 45");
                    break;
            }
        }
    }

    psdImage.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. ResolutionSettings do not apply on export from PSD to PDF**

{{< highlight csharp >}}
string input = "Datensatz 1.psd";
string output = "Datensatz 1.pdf";

using (var image = Image.Load(input, new PsdLoadOptions()))
{
    ResolutionSetting resolutionSetting = new ResolutionSetting(300, 300);

    image.Save(output, new PdfOptions()
    {
        ResolutionSettings = resolutionSetting
    });
}
{{< /highlight >}}

**PSDNET-1391. เพิ่มการสนับสนุนการนำไปใช้ตามโหมดชนะสุขและชนะแล้วที่มีจากการตั้งค่าย่อหน้า**

{{< highlight csharp >}}
string input = "leadingMode.psd";
string output = "output_leadingMode.png";

using (var psdImage = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText text1 = ((TextLayer)psdImage.Layers[1]).TextData;
    foreach (var textPortion in text1.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.TopToTop; // เปลี่ยนค่า LeadingType  
    }
    text1.Items[8].Text = "TopToTop";
    text1.Items[8].Style.FillColor = Color.ForestGreen;
    text1.UpdateLayerData();

    IText text2 = ((TextLayer)psdImage.Layers[2]).TextData;
    foreach (var textPortion in text2.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.BottomToBottom; // เปลี่ยนค่า LeadingType  
    }
    text2.Items[8].Text = "BottomToBottom";
    text2.Items[8].Style.FillColor = Color.ForestGreen;
    text2.UpdateLayerData();

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}
