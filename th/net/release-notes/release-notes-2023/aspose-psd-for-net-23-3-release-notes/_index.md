---
title: ของออก Aspose.PSD for .NET 23.3 - บันทึกการออกเวอร์ชัน
type: docs
weight: 100
url: /th/net/aspose-psd-for-net-23-3-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการออกเวอร์ชันสำหรับ [Aspose.PSD for .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-146|การสนับสนุนของ Posterize Adjustment Layer|คุณลักษณะ|
|PSDNET-1366|ปรับสนับสนุนของ VscgResource|คุณลักษณะ|
|PSDNET-1437|เพิ่มการสนับสนุนของ PostResource สำหรับข้อมูลของ Posterize Adjustment Layer|คุณลักษณะ|
|PSDNET-931|การส่งออกไม่ถูกต้องไปยังเลเยอร์ PNG ที่มี Curves adjustment และโหมดสี CMYK|ข้อบกพร่อง|
|PSDNET-1403|รูปแบบของ Paragraph หายไปหลังจากการบันทึกไฟล์และการอัปเดตไฟล์โดย PS|ข้อบกพร่อง|
|PSDNET-1453|การแสดงผลที่เสียหายของเอฟเฟกต์ glow และ shadow บนข้อความ|ข้อบกพร่อง|


## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey


# **API ที่ถูกเอาออก:**
- ไม่มี


## **ตัวอย่างการใช้:**

**PSDNET-146. การสนับสนุนของ Posterize Adjustment Layer**

{{< highlight csharp >}}
string sourceFile = "zendeya_posterize.psd";
string outputFile = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    foreach (Layer layer in image.Layers)
    {
        if (layer is PosterizeLayer)
        {
            ((PosterizeLayer)layer).Levels = 10;
            image.Save(outputFile);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. การส่งออกไม่ถูกต้องไปยังเลเยอร์ PNG ที่มี Curves adjustment และโหมดสี CMYK**

{{< highlight csharp >}}
string srcFile = "input_LevelsLayerWithLayerMaskCmyk.psd";
string outputFile = "output_LevelsLayerWithLayerMaskCmykTest.png";
string outputFilePsd = "output.psd";

var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage image = (PsdImage)Image.Load(srcFile, psdLoadOptions))
{
    image.Save(outputFilePsd, new PsdOptions()); // the ', new PsdOptions()' provocating a bug.
    image.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. ปรับปรุงการสนับสนุนของ VscgResource**

{{< highlight csharp >}}
string sourceFile = "StrokeInternalFill_src.psd";
string outputFile = "StrokeInternalFill_res.psd";

void AreEqual(double expected, double current, double tolerance = 0.1)
{
    if (Math.Abs(expected - current) > tolerance)
    {
        throw new Exception(
        $"ค่าไม่เท่ากัน.\nค่าที่คาดหวัง:{expected}\nผลลัพธ์:{current}\nความแตกต่าง:{expected - current}");
    }
}

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(89.8, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);

    ((DoubleStructure)rgbColorStructure.Structures[0]).Value = 255d; // สีแดง
    ((DoubleStructure)rgbColorStructure.Structures[1]).Value = 0d; // สีเขียว
    ((DoubleStructure)rgbColorStructure.Structures[2]).Value = 0d; // สีน้ำเงิน

    image.Save(outputFile);
}

// ตรวจสอบการเปลี่ยนแปลง
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(255, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. รูปแบบของ Paragraph หายไปหลังจากการบันทึกไฟล์และการอัปเดตไฟล์โดย PS**

{{< highlight csharp >}}
string sourceFile = "PSDTest3.psd";
string outputFile = "output.psd";

string[] newText = new string[]
{
    "Tile \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    TextLayer layer2 = image.AddTextLayer("New layer", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var textDataTL = layer2.TextData;

    ITextStyle defaultStyleTL = textDataTL.ProducePortion().Style;

    ITextParagraph defaultParagraphTL = textDataTL.ProducePortion().Paragraph;
    ITextPortion[] newPortionsTL = textDataTL.ProducePortions(newText, defaultStyleTL, defaultParagraphTL);

    newPortionsTL[0].Style.FontSize = 14;
    newPortionsTL[0].Style.FontName = "TwCenMT-Bold";

    newPortionsTL[1].Style.Leading = 20;
    newPortionsTL[1].Style.FontSize = 10;
    newPortionsTL[1].Style.FontName = "TwCenMT-Bold";

    // ลบข้อความเก่า
    textDataTL.RemovePortion(0);

    // เพิ่มข้อความใหม่
    foreach (var newPortion in newPortionsTL)
    {
        textDataTL.AddPortion(newPortion);
    }

    textDataTL.UpdateLayerData();

    image.Save(outputFile);
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(outputFile))
{
    Txt2Resource txt2OutputResource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    byte[] bytes = txt2OutputResource.Data;
    string txt2Data = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        txt2Data += (char)bytes[i];
    }

    string key0 = @" >> /6 0 >> >> /1 "; // คำนำหน้าความยาวของย่อหน้า 0
    string key1 = @" >> /6 1 >> >> /1 "; // คำนำหน้าความยาวของย่อหน้า 1
    int index0 = txt2Data.IndexOf(key0);
    int index1 = txt2Data.IndexOf(key1);

    string lenPar0 = txt2Data.Substring(index0 + key0.Length, 1);
    string lenPar1 = txt2Data.Substring(index1 + key1.Length, 3);

    string expected0 = newText[0].Length.ToString();
    string expected1 = (newText[1].Length + 1).ToString();

    if (lenPar0 != expected0 || lenPar1 != expected1)
    {
        throw new Exception(
            $"ความยาวของย่อหน้าผิดพลาด.\nคาดหวัง: {expected0} และ {expected1}\nผลลัพธ์: {lenPar0} และ {lenPar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. เพิ่มการสนับสนุนของ PostResource สำหรับข้อมูลของ Posterize Adjustment Layer**

{{< highlight csharp >}}
string sourceFile = "zendeya_posterize.psd";
string outputFile = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];

    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is PostResource)
        {
            ((PostResource)resource).Levels = 10;
            image.Save(outputFile);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. การแสดงผลที่เสียหายของเอฟเฟกต์ glow และ shadow บนข้อความ**

{{< highlight csharp >}}
string outputPsd = "effect_bug.psd";
string outputPng = "effect_bug.png";

using (var psdImage = new PsdImage(500, 500))
{
    // เพิ่มชั้นข้อความ
    Aspose.PSD.Rectangle textArea1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle textArea2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle textArea3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer textLayer1 = psdImage.AddTextLayer("Text With Effects", textArea1);
    TextLayer textLayer2 = psdImage.AddTextLayer("Text With Effects", textArea2);
    TextLayer textLayer3 = psdImage.AddTextLayer("Text With Effects", textArea3);

    // แก้ไขชั้นข้อความ
    textLayer1.TextData.Items[0].Style.FontSize = 150;
    textLayer1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer1.TextData.UpdateLayerData();

    textLayer2.TextData.Items[0].Style.FontSize = 150;
    textLayer2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer2.TextData.UpdateLayerData();

    textLayer3.TextData.Items[0].Style.FontSize = 150;
    textLayer3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer3.TextData.UpdateLayerData();

    // เพิ่มเอฟเฟกต์
    OuterGlowEffect glow = textLayer1.BlendingOptions.AddOuterGlow(); // ทำให้เสีย
    glow.Spread = 15;
    ((ColorFillSettings)glow.FillColor).Color = Color.Red;

    var shadow = textLayer2.BlendingOptions.AddDropShadow(); // ปัญหาเมื่อมีข้อความยาว
    shadow.Distance = 25;
    shadow.Color = Color.DarkBlue;

    var innerShadow = textLayer3.BlendingOptions.AddInnerShadow(); // ปัญหาเมื่อมีข้อความยาว
    innerShadow.UseGlobalLight = false;
    innerShadow.Angle = -179;
    innerShadow.Distance = 10;
    innerShadow.Size = 8;
    innerShadow.Color = Color.HotPink;

    // ส่งออก
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}