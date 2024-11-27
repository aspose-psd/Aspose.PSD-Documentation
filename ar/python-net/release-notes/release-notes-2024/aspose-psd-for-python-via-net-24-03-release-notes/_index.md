---
title: تحديثات إصدار Aspose.PSD لـ Python via .NET 24.3
type: docs
weight: 10
url: /ar/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على تحديثات الإصدار لـ [Aspose.PSD لـ Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}


| **المفتاح**   | **الملخص**                                                          | **الفئة**  |
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [تنسيق AI] تقليل وقت التحميل لصور AI متعددة الصفحات الكبيرة         | تعزيز |
| PSDPYTHON-45 | ملف PSD بعد التحويل من 8 بت إلى 16 بت أصبح غير قابل للقراءة          |     خلل     |
| PSDPYTHON-46 | ملف PSD بعد التحويل من 8 بت إلى 32 بت أصبح غير قابل للقراءة          |     خلل     |
| PSDPYTHON-47 | [تنسيق AI] إصلاح عرض منحنى القصير في ملف AI                       |     خلل     |



## **تغييرات واجهة البرمجة العامة**
# **تمت إضافة APIs:**
- لا شيء

# **تمت إزالة APIs:**
- لا شيء


## **أمثلة الاستخدام:**

**PSDPYTHON-42. [تنسيق AI] تقليل وقت التحميل لصور AI متعددة الصفحات الكبيرة**

{{< highlight python >}}
   # لا توجد نموذج
{{< /highlight >}}

**PSDPYTHON-45. ملف PSD بعد التحويل من 8 بت إلى 16 بت أصبح غير قابل للقراءة**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # صحيح
                pass
            else:
                raise Exception("المورد العالمي خطأ، يجب أن يكون المورد الأول Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. ملف PSD بعد التحويل من 8 بت إلى 32 بت أصبح غير قابل للقراءة**


{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # صحيح
                pass
            else:
                raise Exception("المورد العالمي خطأ، يجب أن يكون المورد الأول Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [تنسيق AI] إصلاح عرض منحنى القصير في ملف AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}