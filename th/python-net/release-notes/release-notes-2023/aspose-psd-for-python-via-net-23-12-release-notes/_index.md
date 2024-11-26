---
title: Aspose.PSD สำหรับ Python via .NET 23.12 - บันทึกการอัปเดต
type: docs
weight: 10
url: /th/net/aspose-psd-สำหรับ-python-ผ่าน-net-23-12-บันทึกการอัปเดต/
---

{{% alert color="primary" %}}

หน้านี้ประกอบด้วยบันทึกการอัปเดตสำหรับ [Aspose.PSD สำหรับ Python via .NET 23.12](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**     | **สรุป**                                                                                               | **หมวดหมู่** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-7  | [AI Format] เพิ่มการสนับสนุนการแสดงภาพ Raster ในเวอร์ชันใหม่ของ AI                                    |   คุณลักษณะ   |
|  PSDPYTHON-8  | จัดการ Gradient ประเภท Noise ใน GdflResrource                                                               |   คุณลักษณะ   |
|  PSDPYTHON-9  | ข้อผิดพลาด "Object reference not set to an instance of an object." ในขณะบันทึกของ Text Layer หลังจากอัปเดต        |     ข้อบกพร่อง     |
|  PSDPYTHON-10 | แก้ไขการโหลดแบบดีไซน์ของฟอนต์บน MacOS โดยใช้ System.Drawing.Common และ Aspose.Drawing                  |     ข้อบกพร่อง     |
|  PSDPYTHON-11 | AllowWarpRepaint ในตัวเลือกโหลด PsdLoadOptions ทำให้เกิดข้อยกเว้น                                             |     ข้อบกพร่อง     |
|  PSDPYTHON-12 | [AI Format] นำเข้าการประมวลผลของสตรีม cross-reference                                                | การเพิ่มประสิทธิภาพ |
|  PSDPYTHON-13 | ควบคุมใบอนุญาตสำหรับ VectorPathDataResource ทำงานผิดพลาด                                            | การเพิ่มประสิทธิภาพ |


## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
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

# **API ที่ถูกลบออก:**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **ตัวอย่างการใช้:**


**PSDPYTHON-7. [AI Format] เพิ่มการสนับสนุนการแสดงภาพ Raster ในเวอร์ชันใหม่ของ AI**

{{< highlight python >}}
        sourceFile = "raster.ai"
        outputFile = "raster_output.png"

        with Image.load(sourceFile) as image:
            image.save(outputFile, PngOptions())mage.Save(outputFile, new PngOptions());

{{< /highlight >}}

**PSDPYTHON-8. จัดการ Gradient ประเภท Noise ใน GdflResrource**

{{< highlight python >}}
        # ตัวอย่างการใช้งาน GdFlResource นี้โดยใช้ API พื้นฐาน
        sourceFile = "Gradient-Fill.psd"
        destFile = "Gradient-Fill-out.psd"

        with Image.load(sourceFile, PsdLoadOptions()) as image:
            psdImage = cast(PsdImage, image)
            layer = psdImage.layers[1]

            for res in layer.resources:
                resource = as_of(res, GdFlResource)
                if (resource != None):
                    resource.scale = 90
                    resource.angle = 30
                    resource.dither = False
                    resource.align_with_layer = True
                    resource.reverse = False

                    break

            psdImage.save(destFile, PsdOptions())

		# ตัวอย่างการจัดการ solid Gradient
		sourceFile = "ComplexGradientFillLayer.psd"
        outputFile =  "ComplexGradientFillLayer_output.psd"


        # ส่วนคำสั่งการใช้งาน API สามารถดูได้ในโค้ดแบบด้านบน
{{< /highlight >}}

**PSDPYTHON-9. ข้อผิดพลาด "Object reference not set to an instance of an object." ในขณะบันทึกของ Text Layer หลังจากอัปเดต**

{{< highlight python >}}
        sourceFile = "input_1827.psd"
        outputFile = "out_1827.psd"

        with Image.load(sourceFile) as image:
            psdImage = cast(PsdImage, image)
            for layer in psdImage.layers:
                if (is_assignable(layer, TextLayer)):
                    textLayer = cast(TextLayer, layer)
                    textLayer.text_data.update_layer_data()

            # ไม่ควรมีข้อผิดพลาดที่นี่
            psdImage.save(outputFile)
{{< /highlight >}}


**PSDPYTHON-11. AllowWarpRepaint ในตัวเลือกโหลด PsdLoadOptions ทำให้เกิดข้อยกเว้น**

{{< highlight python >}}
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


**PSDPYTHON-13. ควบคุมใบอนุญาตสำหรับ VectorPathDataResource ทำงานผิดพลาด**

{{< highlight python >}}
        sourceFile = "DifferentLayerMasks.psd"
        outputFile = "DifferentLayerMasks_output.psd")=

        with Image.load(sourceFile) as im:
            im.save(outputFile)
{{< /highlight >}}