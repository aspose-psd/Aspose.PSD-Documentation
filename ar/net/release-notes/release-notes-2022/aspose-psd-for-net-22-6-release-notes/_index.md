---
title: ملاحظات الإصدار Aspose.PSD لـ .NET 22.6
type: docs
weight: 70
url: /ar/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-940|إنشاء واجهة برمجة تطبيقات API للحصول على تجزئة فريدة للطبقات المتشابهة في ملفات مختلفة|تحسين|
|PSDNET-678|عرض غير صحيح لطبقة الاملاء بنمط النمط في حالة وجود أنماط أكثر من واحد وتغيير ترتيب الطبقات|خلل|
|PSDNET-1125|استثناء عند تحميل ملف PSD مع وضع لون CMYK محدد|خلل|


## **تغييرات واجهة برمجة التطبيقات العامة**
# **تمت إضافة واجهات برمجة التطبيقات:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **تمت إزالة واجهات برمجة التطبيقات:**
- لا شيء


## **أمثلة الاستخدام:**

**PSDNET-678. عرض غير صحيح لطبقة الاملاء بنمط في حالة وجود أنماط أكثر من واحد وتغيير ترتيب الطبقات**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. إنشاء واجهة برمجة تطبيقات API للحصول على تجزئة فريدة للطبقات المتشابهة في ملفات مختلفة**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    // الكود المذكور في التعليقات السابقة
}
{{< /highlight >}}

**PSDNET-1125. استثناء عند تحميل ملف PSD مع وضع لون CMYK محدد**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}