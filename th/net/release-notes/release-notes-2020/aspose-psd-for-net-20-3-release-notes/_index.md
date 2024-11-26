---
title: บันทึกการอัปเดต Aspose.PSD for .NET 20.3
type: docs
weight: 100
url: /th/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-188|สนับสนุน .Net Core|คุณลักษณะ|
|PSDNET-523|แปลงไฟล์ Adobe Illustrator เป็น PDF|คุณลักษณะ|
|PSDNET-212|เพิ่มความสามารถในการเรนเดอร์สไตล์ต่าง ๆ ในเลเยอร์ข้อความ|คุณลักษณะ|
|PSDNET-144|สนับสนุนเลเยอร์ปรับสีดำและขาว|คุณลักษณะ|
|PSDNET-233|เพิ่มการสนับสนุนการส่งออกรูปแบบ AI (เวอร์ชัน 8) เป็นรูปแบบอื่น|คุณลักษณะ|
|PSDNET-540|สนับสนุนการประมวลผลโหมดผสาน (ใช้สำหรับเลเยอร์กลุ่มเท่านั้น)|คุณลักษณะ|
|PSDNET-539|ข้อยกเว้น: การโหลดรูปภาพล้มเหลวในการโหลดภาพที่มีชื่อ Unicode Alpha Names Resource ว่างเปล่า|ข้อผิดพลาด|
|PSDNET-541|ผลลัพธ์ไม่ถูกต้องหลังจากเปลี่ยนความเป็นมองเลเยอร์กลุ่ม|ข้อผิดพลาด|
|PSDNET-516|ข้อยกเว้นในการโหลดภาพ PSD: ส่วนสี (การทราบเงาแหลม) ต้องมีส่วนประกอบสี 3 ส่วนสำหรับ RGB หรือ 4 ส่วนสำหรับ CMYK|ข้อผิดพลาด|
|PSDNET-536|ข้อยกเว้นหากพยายามวาดบนเลเยอร์ที่สร้างขึ้นใหม่หากใช้รุ่นง่ายของคอนสตรักเตอร์|ข้อผิดพลาด|

## **การเปลี่ยนแปลง API สาธารณะ**
# **เพิ่ม API:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **API ที่ถูกนำออก:**
- ไม่มี

## **ตัวอย่างการใช้:**
**PSDNET-523. แปลงไฟล์ Adobe Illustrator เป็น PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. เพิ่มความสามารถในการเรนเดอร์สไตล์ต่าง ๆ ในเลเยอร์ข้อความ**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // edit text style "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // edit text style "2\r"

    newPortions[2].Style.FauxBold = true; // edit text style "Bold"

    newPortions[3].Style.FauxItalic = true; // edit text style "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // edit text style "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // edit text style "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. เพิ่มการสนับสนุนการส่งออกรูปแบบ AI (เวอร์ชัน 8) เป็นรูปแบบอื่น**

{{< highlight java >}}

 // ตัวอย่างการส่งออกไฟล์ AI ให้อยู่ในรูปแบบ PSD และ PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. สนับสนุนการประมวลผลโหมดผสาน (ใช้สำหรับเลเยอร์กลุ่มเท่านั้น)**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "There is not 23rd layer.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "The 23rd layer is not a layer group.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "The 23rd layer name is not 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "AdjustmentGroup layer should have 'pass through' blend mode.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. การอัปเดตข้อความในเลเยอร์ข้อความทำให้เกิดข้อยกเว้น**

{{< highlight java >}}

 // การอัปเดตข้อความในเลเยอร์ข้อความทำให้เกิดข้อยกเว้น

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. บันทึกภาพ PSD หลังจากการดำเนินการ RotateFlip ทำให้ไฟล์เสียหายซึ่งไม่สามารถเปิดได้**

{{< highlight java >}}
