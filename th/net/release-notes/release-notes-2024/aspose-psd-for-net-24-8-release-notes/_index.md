---
title: บันทึกการปล่อย Aspose.PSD สำหรับ .NET 24.8
type: คำแนะนำ
weight: 50
url: /th/net/aspose-psd-for-net-24-8-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการปล่อยสำหรับ [Aspose.PSD สำหรับ .NET 24.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **คีย์**     | **สรุป**                                                                                        | **หมวดหมู่** |
|:------------|:---------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2091 | [รูปแบบ AI] เพิ่มการจัดการสำหรับกลุ่ม XObject                                   | การปรับปรุง  |
| PSDNET-1754 | เพิ่มกันการแปลงร่างความสามารถโดยการเพิ่ม WarpSettings สำหรับ TextLayer และ SmartObjectLayer | คุณลักษณะ      |
| PSDNET-1836 | [รูปแบบ AI] จัดการเรียกใช้ขั้นตอนเครือข่ายของเลเยอร์ในไดร็ฟตัวดำเนินการ               | คุณลักษณะ      |
| PSDNET-2015 | ผลลัพธ์การแสดงผลของไฟล์ AI ต่างกันมากเมื่อเปรียบเทียบกับผลลัพธ์ของ Illustrator      | ข้อผิดพลาด        |
| PSDNET-2093 | การเชื่อมโยง Smart Object ไม่ได้รับการใช้กับ Smart Object ทั้งหมดในไฟล์ PSD              | ข้อผิดพลาด        |

## **การเปลี่ยนแปลงใน API สาธารณะ**
# **API ที่เพิ่ม:** 

- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.WarpSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.WarpSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[],Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Rotate
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.MeshPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Horizontal
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Vertical
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.None
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Custom
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arc
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcUpper
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcLower
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arch
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Bulge
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Flag
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Fish
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Rise
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Wave
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Twist
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Squeeze
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Inflate

# **API ที่ถูกลบ:**
- None

## **ตัวอย่างการใช้งาน:**

**PSDNET-1754. เพิ่มความสามารถในการแปลงร่างโดยการเพิ่ม WarpSettings สำหรับ TextLayer และ SmartObjectLayer**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "smart_without_warp.psd");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

string[] outputImageFile = new string[4];
string[] outputPsdFile = new string[4];

for (int caseIndex = 0; caseIndex < outputImageFile.Length; caseIndex++)
{
    outputImageFile[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".png");
    outputPsdFile[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".psd");

    using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
    {
        foreach (Layer layer in img.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                var smartLayer = (SmartObjectLayer)layer;
                smartLayer.WarpSettings = GetWarpSettingsByIndex(smartLayer.WarpSettings, caseIndex);
            }

            if (layer is TextLayer)
            {
                var textLayer = (TextLayer)layer;

                if (caseIndex != 3)
                {
                    textLayer.WarpSettings = GetWarpSettingsByIndex(textLayer.WarpSettings, caseIndex);
                }
            }
        }

        img.Save(outputPsdFile[caseIndex], new PsdOptions());
    }

    using (PsdImage img = (PsdImage)Image.Load(outputPsdFile[caseIndex], opt))
    {
        img.Save(outputImageFile[caseIndex],
            new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
    }
}

WarpSettings GetWarpSettingsByIndex(WarpSettings warpParams, int caseIndex)
{
    switch (caseIndex)
    {
        case 0:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 20;
            break;
        case 1:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Vertical;
            warpParams.Value = 10;
            break;
        case 2:
            warpParams.Style = WarpStyles.Flag;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 30;
            break;
        case 3:
            warpParams.Style = WarpStyles.Custom;
            warpParams.MeshPoints[2].Y += 70;
            break;
    }

    return warpParams;
}
{{< /highlight >}}

**PSDNET-1836. [รูปแบบ AI] จัดการเลเยอร์ในดำเนินการของเนื้อหา**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Layers-NoPen.ai");
string outputFile = Path.Combine(outputFolder, "Layers-NoPen.output.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}

//// เส้นโค้งจากเลเยอร์ชื่อ "Pen" ควรถูกซ่อน
{{< /highlight >}}

**PSDNET-2015. ผลลัพธ์การแสดงผลของไฟล์ AI แตกต่างมากเมื่อเปรียบเทียบกับผลลัพธ์ของ Illustrator**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "4.ai");
string outputFilePath = Path.Combine(outputFolder, "4.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2093. การเชื่อมโยง Smart Object ไม่ได้รับการใช้กับ Smart Object ทั้งหมดในไฟล์ PSD**

{{< highlight csharp >}}
string[] files = { "simple_test", "w22" };
string changeFile = Path.Combine(baseFolder, "image(19).png");

string[] sourceFile = new string[files.Length];
string[] outputFiles = new string[files.Length];

for (int i = 0; i < files.Length; i++)
{
    sourceFile[i] = Path.Combine(baseFolder, files[i] + ".psd");
    outputFiles[i] = Path.Combine(outputFolder, files[i] + "_output.psd");

    using (var image = (PsdImage)Image.Load(sourceFile[i]))
    {
        foreach (Layer layer in image.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                SmartObjectLayer smart = (SmartObjectLayer)layer;

                // สำหรับเลเยอร์สมาร์ทที่สองที่นี่มีข้อผิดพลาด
                smart.ReplaceContents(changeFile);
            }
        }

        image.Save(outputFiles[i]);
    }
}
{{< /highlight >}}
