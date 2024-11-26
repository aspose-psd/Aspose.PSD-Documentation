---
title: บันทึกการปล่อย Aspose.PSD สำหรับ .NET 23.12
type: คู่มือ
weight: 10
url: /th/net/aspose-psd-for-net-23-12-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการปล่อยของ [Aspose.PSD สำหรับ .NET 23.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **Summary**                                                                                               | **Category** |
|:------------|:----------------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1679 | [AI Format] เพิ่มการสนับสนุนการแสดงภาพเรสเตอร์ในเวอร์ชันใหม่ของ AI                               |   คุณลักษณะ   |
| PSDNET-1454 | จัดการกับประเภทเส้นไส้ประพันธ์ใน GdflResrource                                                |   คุณลักษณะ   |
| PSDNET-1827 | ข้อผิดพลาด "อ้างอิงตัวอ็อบเจกต์ไม่ได้กำหนดให้เป็นตัวอย่างของอ็อบเจกต์" ในขณะบันทึกเลเยอร์ข้อความหลังจากอัพเดต    |     ข้อบกพร่อง     |
| PSDNET-1776 | แก้ไขการโหลดแบบด้วยตนเองของฟอนต์บน MacOS โดยใช้ System.Drawing.Common และ Aspose.Drawing.                        |     ข้อบกพร่อง     |
| PSDNET-1536 | AllowWarpRepaint ใน PsdLoadOptions ส่งผลให้เกิดข้อยกเว้นโดยขึ้น                                   |     ข้อบกพร่อง     |
| PSDNET-1714 | [AI Format] นำการประมวลผลของสตรีมอ้างอิงข้ามกันมาใช้                                           | การปรับปรุง |
| PSDNET-1834 | การควบคุมการอนุญาตสำหรับ VectorPathDataResource ทำงานไม่ถูกต้อง                                     | การปรับปรุง |
| PSDNET-770  | เปิดไฟล์ภาพใด ๆ เป็นอ็อบเจกต์สมาร์ทที่ฝังอยู่ในภาพ PSD                                      | การปรับปรุง |
| PSDNET-1864 | ระบบลิขิศ Aspose.PSD Plugin                                                                             | การปรับปรุง |



## **การเปลี่ยนแปลงใน Public API**
# **APIs เพิ่มเติม:**
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.#ctor(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.RGB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.HSB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.LAB
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientMode
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.#ctor
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.Metered.GetProductName
- M:Aspose.PSD.Metered.IsMeteredLicensed
- T:Aspose.PSD.PluginLicenseException
- M:Aspose.PSD.PluginLicenseException.#ctor
- M:Aspose.PSD.Metered.Equals(System.Object)

# **APIs ที่ถูกนำออก:**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **ตัวอย่างการใช้:**

**PSDNET-1679. [AI Format] เพิ่มการสนับสนุนการแสดงภาพเรสเตอร์ในเวอร์ชันใหม่ของ AI**

{{< highlight csharp >}}
            string sourceFile = Path.Combine(baseFolder, "raster.ai");
            string outputFile = Path.Combine(outputFolder, "raster_output.png");

            using (AiImage image = (AiImage)Image.Load(sourceFile))
            {
                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1454. จัดการกับประเภทเส้นไส้ประพันธ์ใน GdflResrource**

{{< highlight csharp >}}
            string sourceFile = "Gradient-Fill.psd";
            string destFile = "Gradient-Fill-out.psd";

            using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
            {
                Layer layer = image.Layers[1];

                foreach (LayerResource resource in layer.Resources)
                {
                    GdFlResource gdFlResource = resource as GdFlResource;

                    if (gdFlResource != null)
                    {
                        gdFlResource.Scale = 90;
                        gdFlResource.Angle = 30;
                        gdFlResource.Dither = false;
                        gdFlResource.AlignWithLayer = true;
                        gdFlResource.Reverse = false;

                        break;
                    }
                }

                image.Save(destFile, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-1827. ข้อผิดพลาด "อ้างอิงตัวอ็อบเจกต์ไม่ได้กำหนดให้เป็นตัวอย่างของอ็อบเจกต์" ในขณะบันทึกเลเยอร์ข้อความหลังจากอัพเดต**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "input_1827.psd");
string outputFile = Path.Combine(outputFolder, "out_1827.psd");

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer textLayer)
        {
            textLayer.TextData.UpdateLayerData();
        }
    }

    // การนำไปใช้ไม่ควรมีข้อผิดพลาดที่นี่
    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1536. AllowWarpRepaint ใน PsdLoadOptions ส่งผลให้เกิดข้อยกเว้นโดยขึ้น**

{{< highlight csharp >}}
            string sourceFile = @"SizeChart-4 Colors.psd";
            string outputFile = @"SizeChart-4 Colors.png";

            using (var psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true })) 
			{ 
				psdImage.Save(outputFile + "_original.png", new PngOptions()
				{
					ColorType = PngColorType.TruecolorWithAlpha,
					Progressive = true,
					CompressionLevel = 9
				});
			}
{{< /highlight >}}

**PSDNET-1834. การควบคุมการอนุญาตสำหรับ VectorPathDataResource ทำงานไม่ถูกต้อง**

{{< highlight csharp >}}
 using (PsdImage im = (PsdImage)Image.Load(DifferentLayerMasks.psd))
 {
     im.Save(complexFiles[i] + "out" + "output.psd");
     im.Save(complexFiles[i] + "out" + "output.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
 }
{{< /highlight >}}

**PSDNET-770. เปิดไฟล์ภาพใด ๆ เป็นอ็อบเจกต์สมาร์ทที่ฝังอยู่ในภาพ PSD**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "empty.psd");

string addTreeFile = Path.Combine(baseFolder, "tree.psd");
string addFrostFile = Path.Combine(baseFolder, "frost.png");

string outputTreeFile = Path.Combine(outputFolder, "tree_export.psd");
string outputFrostFile = Path.Combine(outputFolder, "frost_export.psd");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream stream = new FileStream(addTreeFile, FileMode.Open))
    {
        using (SmartObjectLayer smartLayer = new SmartObjectLayer(stream))
        {
            psdImage.AddLayer(smartLayer);

            psdImage.Save(outputTreeFile, new PsdOptions());                        
        }
    }
}

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream stream = new FileStream(addFrostFile, FileMode.Open))
    {
        using (SmartObjectLayer smartLayer = new SmartObjectLayer(stream))
        {
            psdImage.AddLayer(smartLayer);

            psdImage.Save(outputFrostFile, new PsdOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1864. ระบบลิขิศ Aspose.PSD Plugin**

{{< highlight csharp >}}            
    var metered = new Metered();
    metered.SetMeteredKey(pluginPublic, pluginPrivate);
			
	// การจัดการเฉพาะเจาะจงของปลั๊กอิน
{{< /highlight >}}