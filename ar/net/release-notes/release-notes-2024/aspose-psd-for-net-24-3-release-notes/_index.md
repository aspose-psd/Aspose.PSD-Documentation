---
title: تحديثات إصدار Aspose.PSD لـ .NET 24.3
type: docs
weight: 100
url: /ar/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على تحديثات إصدار لـ [Aspose.PSD لـ .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **المفتاح**     | **الملخص**                                                          | **الفئة** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [تنسيق AI] تقليل وقت تحميل الصور الكبيرة المتعددة الصفحات       |     تحسين     |
| PSDNET-1905 | تصبح ملف PSD غير قابل للقراءة بعد التحويل من 8 بت إلى 16 بت |     خطأ     |
| PSDNET-1906 | تصبح ملف PSD غير قابل للقراءة بعد التحويل من 8 بت إلى 32 بت |     خطأ     |
| PSDNET-1921 | [تنسيق AI] إصلاح تقديم المنحنيات القصيرة في ملف AI                 |     خطأ     |

## **التغييرات العامة في واجهة برمجة التطبيقات**
# **الواجهات البرمجية الجديدة:**
- لا شيء

# **الواجهات البرمجية المزالة:**
- لا شيء

## **أمثلة استخدام:**

**PSDNET-1905. تصبح ملف PSD غير قابل للقراءة بعد التحويل من 8 بت إلى 16 بت**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("مورد عالمي خاطئ، يجب أن يكون المورد الأول Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. تصبح ملف PSD غير قابل للقراءة بعد التحويل من 8 بت إلى 32 بت**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("مورد عالمي خاطئ، يجب أن يكون المورد الأول Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [تنسيق AI] إصلاح تقديم المنحنيات القصيرة في ملف AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}