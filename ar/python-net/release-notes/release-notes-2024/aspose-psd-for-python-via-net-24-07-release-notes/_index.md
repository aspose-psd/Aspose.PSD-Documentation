---
title: ملاحظات الإصدار Aspose.PSD for Python via .NET 24.7
type: docs
weight: 10
url: /ar/python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD for Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **مفتاح**   | **الملخص**                                                                                                       | **الفئة** |
|:-----------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | استثناء "فشل تحميل الصورة" عند فتح مستند AI                                           | خلل   |
| PSDPYTHON-87 | تقديم النص بشكل غير صحيح في ملفات PDF الناتجة                                                | خلل   |
| PSDPYTHON-88 | إصلاح استثناء ImageSaveException: فشل تصدير الصورة للملف المعطى على نظام Linux           | خلل   |
| PSDPYTHON-89 | إصلاح تحميل الخطوط عند استخدام Aspose.Drawing                                             | خلل   |
| PSDPYTHON-90 | 'العملية الحسابية أسفرت عن تجاوز' عند إنشاء طبقة كائن ذكي باستخدام JPEG كبير        | خلل   |
| PSDPYTHON-91 | لا يمكن تحويل ملف AI إلى ملف JPG                                                         | خلل   |

## **تغييرات الواجهة البرمجية العامة**
# **الواجهات البرمجية الجديدة:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **الواجهات البرمجية المزالة:**
- لا شيء

## **أمثلة الاستخدام:**

**PSDPYTHON-86. استثناء "فشل تحميل الصورة" عند فتح مستند AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. تقديم النص بشكل غير صحيح في ملفات PDF الناتجة**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. إصلاح استثناء ImageSaveException: فشل تصدير الصورة للملف المعطى على نظام Linux**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. إصلاح تحميل الخطوط عند استخدام Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- قبل التحديث. عدد الخطوط المثبتة: " + str(len(installedFonts.families)))
            print("- تحديث ذاكرة التخزين المؤقتة للخطوط بمحاولة الحصول على اسم الخط الخاص بـ 'Arial' من Adobe: ")
            FontSettings.get_adobe_font_name("Arial")
            print("- بعد التحديث. عدد الخطوط المثبتة: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'العملية الحسابية أسفرت عن تجاوز' عند إنشاء طبقة كائن ذكي باستخدام JPEG كبير**
{{< highlight python >}}
        # تم إصلاح المشكلة، لكن هناك مشكلة أخرى في Aspose.PSD for Python تمنع هذا الاختبار
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Test Layer"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. لا يمكن تحويل ملف AI إلى ملف JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}