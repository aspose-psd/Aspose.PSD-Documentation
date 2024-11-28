---
title: فراخوانی‌های رها شده از Aspose.PSD برای پایتون از طریق .NET 24.1 - یادداشت‌های انتشار
type: docs
weight: 10
url: /fa/net/aspose-psd-for-python-via-net-24-1-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD برای پایتون از طریق .NET 24.1](https://pypi.org/project/aspose-psd/) می‌باشد.

{{% /alert %}}

| **کلید**     | **خلاصه**                                                                                                | **دسته‌بندی** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [فرمت AI] اضافه کردن کنترل اساسی برای تصاویر AI چندصفحه ای                                               |   ویژگی   |
|  PSDPYTHON-22 | اثر متن انعطاف‌پذیر به متن اعمال نمی‌شود                                                                   |     باگ     |
|  PSDPYTHON-23 | رندر صحیح ماسک در فایل خاص                                                                             |     باگ     |
|  PSDPYTHON-24 | NullReferenceException در Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor               |     باگ     |
|  PSDPYTHON-25 | [فرمت AI] رفع مصرف حافظه در AiExporterUtils                                                            |     باگ     |



## **تغییرات API عمومی**
# **API های اضافه شده:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **API های حذف شده:**
- هیچکدام


## **مثال‌های استفاده:**

**PSDPYTHON-19. [فرمت AI] اضافه کردن کنترل اساسی برای تصاویر AI چندصفحه ای**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # بارگذاری تصویر AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # به صورت پیش‌فرض، ActivePageIndex 0 است.
            # بنابراین اگر تصویر AI را بدون تغییر در این خاصیت ذخیره کنید، صفحه اول رندر خواهد شد و ذخیره می‌شود.
            image.save(firstPageOutputPng, PngOptions())

            # تغییر دهید اندیس صفحه فعال به صفحه دوم.
            image.active_page_index = 1

            # صفحه دوم تصویر AI را به عنوان تصویر PNG ذخیره کنید.
            image.save(secondPageOutputPng, PngOptions())

            # تغییر دهید اندیس صفحه فعال به صفحه سوم.
            image.active_page_index = 2

            # صفحه سوم تصویر AI را به عنوان تصویر PNG ذخیره کنید.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. اثر متن انعطاف‌پذیر به متن اعمال نمی‌شود**

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

**PSDPYTHON-23. رندر نادرست ماسک در فایل خاص**

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

**PSDPYTHON-24. NullReferenceException در Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [فرمت AI] رفع مصرف حافظه در AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # مصرف حافظه در C# 220 است، اما برای پایتون ما به فعالیت‌های GC دسترسی مستقیم نداریم.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # بارگذاری تصویر AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # صفحه اول تصویر AI را به عنوان تصویر PNG ذخیره نمایید.
            image.save(firstPageOutputPng, pngOpt)

            # تغییر دهید اندیس صفحه فعال به صفحه دوم.
            image.active_page_index = 1

            # صفحه دوم تصویر AI را به عنوان تصویر PNG ذخیره کنید.
            image.save(secondPageOutputPng, pngOpt)

            # تغییر دهید اندیس صفحه فعال به صفحه سوم.
            image.active_page_index = 2

            # صفحه سوم تصویر AI را به عنوان تصویر PNG ذخیره کنید.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("استفاده از حافظه بیش از حد است. {} به جای {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}
