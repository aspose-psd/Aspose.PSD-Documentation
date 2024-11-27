---
title: دفترچه‌ی انتشار Aspose.PSD for .NET 20.9
type: مستندات
weight: 40
url: /fa/net/aspose-psd-for-net-20-9-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی یادداشت‌های انتشار [Aspose.PSD for .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-408|پشتیبانی از SoLEResource (منبع خارجی لایه‌ی شیء هوشمند)|ویژگی|
|PSDNET-614|پشتیبانی از اشیاء هوشمند پیوند شده|ویژگی|
|PSDNET-615|پشتیبانی از اشیاء هوشمند داخلی|ویژگی|
|PSDNET-690|به‌روزرسانی متن در پرونده PSD داده شده و ذخیره آن تغییراتی در لایه‌ها و پارامترهای زیادی متن ایجاد می‌کند|باگ|
|PSDNET-696|لایه‌های FillLayer پس از ایجاد به‌روز نمی‌شوند و نمی‌توانند به درستی تصویری شوند|باگ|
|PSDNET-712|ناهنجاری: نمی‌تواند پرونده مورد نظر را با Aspose.PSD 20.8.0 باز کند|باگ|
|PSDNET-714|در یک پرونده خاص PSD، تغییر اندازه لایه متن مقدار مکان را خراب می‌کند|باگ|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoKerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandardLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.DiscretionaryLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ContextualAlternates
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.LanguageIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.VerticalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HorizontalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Fractions
- T:Aspose.PSD.FileFormats.Psd.AutoKerning
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Manual
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Metric
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Optical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Item(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource.PlacedId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PageNumber
...
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.#ctor

## **مثال‌های استفاده:**
**PSDNET-408. پشتیبانی از SoLEResource (منبع خارجی لایه‌ی شیء هوشمند)**
{{< highlight csharp >}}
            //کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}

**PSDNET-614. پشتیبانی از اشیاء هوشمند پیوند شده**
{{< highlight csharp >}}
            //کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}

**PSDNET-615. پشتیبانی از اشیاء هوشمند داخلی**
{{< highlight csharp >}}
            //کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}

**PSDNET-690. به‌روزرسانی متن در PSD داده شده و ذخیره آن تغییراتی در لایه‌ها و پارامترهای زیادی متن ایجاد می‌کند**
{{< highlight csharp >}}
            //کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}

**PSDNET-696. لایه‌های FillLayer پس از ایجاد به‌روز نمی‌شوند و نمی‌توانند به درستی تصویری شوند**
{{< highlight csharp >}}
            //کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}

**PSDNET-712. ناهنجاری: نمی‌تواند پرونده مورد نظر را با Aspose.PSD 20.8.0 باز کند**
{{< highlight csharp >}}
            //کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}

**PSDNET-714. در یک پرونده خاص PSD، تغییر اندازه لایه متن مقدار مکان را خراب می‌کند**
{{< highlight csharp >}}
            //کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}**PSDNET-690. به‌روزرسانی متن در PSD داده شده و ذخیره آن تغییراتی در لایه‌ها و پارامترهای زیادی متن ایجاد می‌کند**
{{< highlight csharp >}}
            // کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}

**PSDNET-696. لایه‌های FillLayer پس از ایجاد به‌روز نمی‌شوند و نمی‌توانند به درستی تصویری شوند**
{{< highlight csharp >}}
            // کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}

**PSDNET-712. ناهنجاری: نمی‌تواند پرونده مورد نظر را با Aspose.PSD 20.8.0 باز کند**
{{< highlight csharp >}}
            // کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}

**PSDNET-714. در یک پرونده خاص PSD، تغییر اندازه لایه متن مقدار مکان را خراب می‌کند**
{{< highlight csharp >}}
            // کد نمونه اینجا قرار می‌گیرد
{{< /highlight >}}