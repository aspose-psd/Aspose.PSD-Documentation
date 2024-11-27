---
title: فراپس‌ پی‌اِس‌دی برای .نت ۲۲.۴ – یادداشت‌های انتشار
type: مستندات
weight: 90
url: /fa/net/aspose-psd-for-net-22-4-release-notes/
---

{{% alert color="primary" %}}

این صفحه حاوی یادداشت‌های انتشار برای [فراپس پی‌اِس‌دی برای .نت ۲۲.۴](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-261|رندرینگ افکت لایه براق خارجی|ویژگی|
|PSDNET-1123|افزودن پشتیبانی از لایسنس Sha256|بهبود|
|PSDNET-1107|مکان‌گذاری متن چندخطی با نتیجه در فتوشاپ مطابقت ندارد|اشکال|
|PSDNET-1113|مشکل در بارگذاری فایل PSD در تجزیه‌وتحلیل داده منبع متن|اشکال|
|PSDNET-1129|موقعیت نادرست الگوی سفارشی پس از ذخیره به عنوان PSD|اشکال|


## **تغییرات API عمومی**
# **API های اضافه شده:**
- T:Aspose.PSD.FileFormats.Psd.JustificationMode
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Left
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Right
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Center
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddOuterGlow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Intensity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsAntiAliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Noise
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsSoftBlend
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Range
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Jitter


# **API های حذف شده:**
- هیچکدام


## **نمونه‌های استفاده:**

**PSDNET-261. رندرینگ افکت لایه براق خارجی**
{{< highlight csharp >}}
string src = "GreenLayer.psd";
string output = "output261.png";

using (var image = (PsdImage)Image.Load(src))
{
    OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
    effect.Range = 10;
    effect.Spread = 10;
    ((IColorFillSettings)effect.FillColor).Color = Color.Red;
    effect.Opacity = 128;
    effect.BlendMode = BlendMode.Normal;

    image.Save(output, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1107. مکان‌گذاری متن چندخطی با نتیجه در فتوشاپ مطابقت ندارد**

{{< highlight csharp >}}
string src = "source1107.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var image = (PsdImage)Image.Load(src))
{ 
   var txtLayer = image.AddTextLayer("Text line1\rText line2\rText line3", new Rectangle(200, 200, 500, 500));
   var portions = txtLayer.TextData.Items;

   portions[0].Paragraph.Justification = JustificationMode.Left;
   portions[1].Paragraph.Justification = JustificationMode.Right;
   portions[2].Paragraph.Justification = JustificationMode.Center;

   txtLayer.TextData.UpdateLayerData();

   image.Save(outputPsd);
   image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1113. مشکل در بارگذاری فایل PSD در تجزیه‌وتحلیل داده منبع متن**

{{< highlight csharp >}}
string sourceFile = "input.psd";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    // با موفقیت بارگذاری شد.
}
{{< /highlight >}}


**PSDNET-1129. موقعیت نادرست الگوی سفارشی پس از ذخیره به عنوان PSD**

{{< highlight csharp >}}
string sourceFile = "input_1129.psd";
string outputPsd = "out_psdnet1129.psd";
string outputPng = "out_psdnet1129.png";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
