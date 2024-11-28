---
title: تفاصيل الإصدار 23.12 من Aspose.PSD لـ .NET - ملاحظات الإصدار
type: docs
weight: 10
url: /ar/net/aspose-psd-for-net-23-12-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 23.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **المفتاح** | **الملخص**                                                                                            | **الفئة** |
|:------------|:------------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1679 | [صيغة AI] إضافة دعم لتقديم صورة بكسيلية في إصدار جديد من AI                                       |   ميزة    |
| PSDNET-1454 | التعامل مع تدرج نوع Noise في GdflResrource                                                           |   ميزة    |
| PSDNET-1827 | خطأ "الإشارة إلى كائن لم يتم التعيين لقيمة مثيل لكائن." عند حفظ طبقة النص بعد التحديث         |     خطأ   |
| PSDNET-1776 | إصلاح التحميل اليدوي للخطوط على نظام MacOS باستخدام System.Drawing.Common و Aspose.Drawing. |     خطأ   |
| PSDNET-1536 | تمكين AllowWarpRepaint في خيارات PsdLoadOptions يؤدي إلى استثناء                               |     خطأ   |
| PSDNET-1714 | [صيغة AI] تنفيذ معالجة لسلاسل الإشارة المتبادلة                                                | تعزيز |
| PSDNET-1834 | تحكم الترخيص لـ VectorPathDataResource يعمل بشكل غير صحيح                                         | تعزيز |
| PSDNET-770  | فتح أي ملف صورة ككائن ذكي مضمن في صورة PSD                                                       | تعزيز |
| PSDNET-1864 | نظام ترخيص البرنامج المساعد لـ Aspose.PSD                                                          | تعزيز |



## **تغييرات API العامة**
# **الـ APIs المُضافة:**
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

# **الـ APIs المحذوفة:**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **أمثلة الاستخدام:**

**PSDNET-1679. [صيغة AI] إضافة دعم لتقديم صورة بكسيلية في إصدار جديد من AI**

{{< highlight csharp >}}
            string sourceFile = Path.Combine(baseFolder, "raster.ai");
            string outputFile = Path.Combine(outputFolder, "raster_output.png");

            using (AiImage image = (AiImage)Image.Load(sourceFile))
            {
                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1454. التعامل مع تدرج نوع Noise في GdflResrource**

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

**PSDNET-1827. خطأ "الإشارة إلى كائن لم يتم التعيين لقيمة مثيل لكائن." عند حفظ طبقة النص بعد التحديث**

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

    // لا يجب أن يوجد خطأ هنا
    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1536. AllowWarpRepaint في خيارات PsdLoadOptions يؤدي إلى استثناء**

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

**PSDNET-1834. تحكم الترخيص لـ VectorPathDataResource يعمل بشكل غير صحيح**

{{< highlight csharp >}}
 using (PsdImage im = (PsdImage)Image.Load(DifferentLayerMasks.psd))
 {
     im.Save(complexFiles[i] + "out" + "output.psd");
     im.Save(complexFiles[i] + "out" + "output.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
 }
{{< /highlight >}}

**PSDNET-770. فتح أي ملف صورة ككائن ذكي مضمن في صورة PSD**

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

**PSDNET-1864. نظام ترخيص البرنامج المساعد لـ Aspose.PSD**

{{< highlight csharp >}}            
    var metered = new Metered();
    metered.SetMeteredKey(pluginPublic, pluginPrivate);
    
	// Manipulation محددة للبرنامج المساعد
{{< /highlight >}}