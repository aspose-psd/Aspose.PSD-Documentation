---
title: أسبوعيات Aspose.PSD لـ Python via .NET 24.1 - ملاحظات الإصدار
type: docs
weight: 10
url: /ar/net/aspose-psd-for-python-via-net-24-1-release-notes/
---

{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [أسبوز.PSD لـ Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **المفتاح**  | **الملخص**                                                                                                | **الفئة**  |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [تنسيق الذكاء الاصطناعي] إضافة معالجة أساسية لصور AI متعددة الصفحات                                      |   ميزة     |
|  PSDPYTHON-22 | تأثير تحريف النص لا ينطبق على النص                                                                        |     خلل     |
|  PSDPYTHON-23 | عرض غير صحيح للقناع في الملف المحدد                                                                       |     خلل     |
|  PSDPYTHON-24 | استثناء NullReferenceException في Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor  |     خلل     |
|  PSDPYTHON-25 | [تنسيق الذكاء الاصطناعي] إصلاح استخدام الذاكرة في AiExporterUtils                                       |     خلل     |



## **تغييرات واجهة برمجة التطبيقات العامة**
# **الواجهات البرمجية المُضافة:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **الواجهات البرمجية المحذوفة:**
- None

## **أمثلة الاستخدام:**

**PSDPYTHON-19. [تنسيق الذكاء الاصطناعي] إضافة معالجة أساسية لصور AI متعددة الصفحات**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # قم بتحميل صورة AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # بشكل افتراضي، ActivePageIndex هو 0.
            # لذلك إذا قمت بحفظ صورة AI دون تغيير هذه الخاصية، سيتم عرض وحفظ الصفحة الأولى.
            image.save(firstPageOutputPng, PngOptions())

            # قم بتغيير فهرس الصفحة النشطة ليكون الصفحة الثانية.
            image.active_page_index = 1

            # احفظ الصفحة الثانية من صورة AI كصورة PNG.
            image.save(secondPageOutputPng, PngOptions())

            # قم بتغيير فهرس الصفحة النشطة ليكون الصفحة الثالثة.
            image.active_page_index = 2

            # احفظ الصفحة الثالثة من صورة AI كصورة PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. تأثير تحريف النص لا ينطبق على النص**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. عرض غير صحيح للقناع في الملف المحدد**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. استثناء NullReferenceException في Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [تنسيق الذكاء الاصطناعي] إصلاح استخدام الذاكرة في AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # استخدام الذاكرة في C# هو 220، لكن بالنسبة للبايثون ليس لدينا وصول مباشر إلى أنشطة GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # قم بتحميل صورة AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # احفظ الصفحة الأولى من صورة AI كصورة PNG.
            image.save(firstPageOutputPng, pngOpt)

            # قم بتغيير فهرس الصفحة النشطة ليكون الصفحة الثانية.
            image.active_page_index = 1

            # احفظ الصفحة الثانية من صورة AI كصورة PNG.
            image.save(secondPageOutputPng, pngOpt)

            # قم بتغيير فهرس الصفحة النشطة ليكون الصفحة الثالثة.
            image.active_page_index = 2

            # احفظ الصفحة الثالثة من صورة AI كصورة PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("استخدام الذاكرة كبير جدًا. {} بدلاً من {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}