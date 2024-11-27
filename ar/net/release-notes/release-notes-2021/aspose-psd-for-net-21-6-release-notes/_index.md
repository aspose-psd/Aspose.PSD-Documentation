---
title: أسبوز.باسد ل .نت 21.6 - ملاحظات الإصدار
type: docs
weight: 70
url: /ar/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}} 

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [أسبوز.باسد ل .نت 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-546|لا يتم عرض قناع القصاصة للمجموعة بشكل صحيح|خلل|
|PSDNET-547|يتم تجاهل القناع العادي أو القناع البياني لمجموعة الطبقات عند التقديم|خلل|
|PSDNET-647|صورة PSD مع أقنعة الطبقة البيانية المعطلة عند الحفظ تقوم بتمكين الأقنعة البيانية|خلل|
|PSDNET-786|استثناء عند إنشاء طبقة نص بنص يتجاوز طول النص 255 حرفًا|خلل|
|PSDNET-900|لا يمكن عرض نص الطبقة النصية على نظام Linux|تحسين|

## **تغييرات واجهة برمجة التطبيقات العامة**
# **الواجهات البرمجية التي تمت إضافتها:**
- لا شيء

# **الواجهات البرمجية التي تمت إزالتها:**
- لا شيء

## **أمثلة الاستخدام:**

**PSDNET-546. لا يتم عرض قناع القصاصة للمجموعة بشكل صحيح**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. يتم تجاهل القناع العادي أو القناع البياني لمجموعة الطبقات عند التقديم**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. صورة PSD مع أقنعة الطبقة البيانية المعطلة عند الحفظ تقوم بتمكين الأقنعة البيانية**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. استثناء عند إنشاء طبقة نص بنص يتجاوز طول النص 255 حرفًا**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}