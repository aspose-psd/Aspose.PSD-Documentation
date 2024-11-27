---
title: ملاحظات الإصدار Aspose.PSD لـ .NET 23.10
type: docs
weight: 30
url: /ar/net/aspose-psd-for-net-23-10-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 23.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **المفتاح** | **الملخص** | **الفئة** |
|:------------|:------------|:--------|
| PSDNET-692 | دعم اتجاه النص العمودي | ميزة |
| PSDNET-1402 | استخدام إعدادات الحدود من مورد vstk في تقديم الحدود للشكل | ميزة |
| PSDNET-1607 | تنفيذ تقديم المنطقة الداخلية لأشكال الحدود | ميزة |
| PSDNET-1644 | عدم إعادة رسم طبقة الشكل إذا لم تتغير | ميزة |
| PSDNET-1696 | [تنسيق AI] إضافة دعم لقراءة الرأس من ملفات AI مستندة إلى PDF | ميزة |
| PSDNET-1560 | الطرق المختلفة لتعيين دقة ملف Psd لا تعمل | خلل |
| PSDNET-1728 | لا يعمل FontSettings.SetFontsFolders أو يستخدم Aspose.PSD خطًا غير صحيح | خلل |
| PSDNET-1739 | حالة تراجع. إصلاح استثناء الإشارة المرجعية الفارغة عند توفر طبقة Shape | خلل |


## **تغييرات الواجهة العامة**
# **تمت إضافة الواجهات البرمجية:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Stroke
- M:Aspose.PSD.FileFormats.Psd.PsdImage.SetResolution(System.Double,System.Double)
- T:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Stroke
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Fill
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineAlignment


# **تمت إزالة الواجهات البرمجية:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items


## **أمثلة الاستخدام:**

**PSDNET-692. دعم اتجاه النص العمودي**

{{< highlight csharp >}}
string sourceFile = "692_lt1.psd";
string outputFile = "692_output.png";
string fontsFolder = "692_Fonts";

var fontFolders = new List<string>(FontSettings.GetFontsFolders());
fontFolders.Add(fontsFolder);
FontSettings.SetFontsFolders(fontFolders.ToArray(), true);

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    psdImage.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1402. استخدام إعدادات الحدود من مورد vstk في تقديم الحدود للشكل**

{{< highlight csharp >}}
.
.
.
{{< /highlight >}}

**PSDNET-1607. تنفيذ تقديم المنطقة الداخلية لأشكال الحدود**

{{< highlight csharp >}}
.
.
.
{{< /highlight >}}

**PSDNET-1644. عدم إعادة رسم طبقة الشكل إذا لم تتغير**

{{< highlight csharp >}}
.
.
.
{{< /highlight >}}

**PSDNET-1696. [تنسيق AI] إضافة دعم لقراءة الرأس من ملفات AI مستندة إلى PDF**

{{< highlight csharp >}}
.
.
.
{{< /highlight >}}

**PSDNET-1560. الطرق المختلفة لتعيين دقة ملف Psd لا تعمل**

{{< highlight csharp >}}
.
.
.
{{< /highlight >}}

**PSDNET-1728. لا يعمل FontSettings.SetFontsFolders أو يستخدم Aspose.PSD خطًا غير صحيح**

{{< highlight csharp >}}
.
.
.
{{< /highlight >}}

**PSDNET-1739. حالة تراجع. إصلاح استثناء الإشارة المرجعية الفارغة عند توفر طبقة Shape**

{{< highlight csharp >}}
.
.
.
{{< /highlight >}}