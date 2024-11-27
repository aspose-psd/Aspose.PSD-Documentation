---
title: עימוד Aspose.PSD עבור Python via .NET 24.1 - הודעות שחרור
type: מסמכים
weight: 10
url: /he/net/aspose-ps-d-לפי-פייתון-דרך-net-24-1-הודעות-שחרור/
---

{{% alert color="primary" %}}

עמוד זה מכיל הודעות שחרור עבור [Aspose.PSD עבור Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **מפתח**    | **סיכום**                                                                                                             | **קטגוריה** |
|:---------------|:---------------------------------------------------------------------------------------------------------------------|:--------------|
|  PSDPYTHON-19  | [פורמט AI] הוספת טיפול בסיסי עבור תמונות AI מרובות הדפים                                                     |   תכונה     |
|  PSDPYTHON-22  | האפקט הרטט של הטקסט אינו חל על הטקסט                                                                           |   באג       |
|  PSDPYTHON-23  | עיבוד לא נכון של מסיכה בקובץ מסוים                                                                              |   באג       |
|  PSDPYTHON-24  | NullReferenceException ב־Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor                    |   באג       |
|  PSDPYTHON-25  | [פורמט AI] תיקון שימוש בזיכרון ב־AiExporterUtils                                                               |   באג       |



## **שינויים ב- API הציבורי**
# **APIs שנוספו:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **APIs שהוסרו:**
- אף אחד


## **דוגמאות שימוש:**

**PSDPYTHON-19. [פורמט AI] הוספת טיפול בסיסי עבור תמונות AI מרובות הדפים**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # טען את תמונת AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # כברירת מחדל, ה־ActivePageIndex היא 0.
            # לכן אם תייצר את תמונת ה־AI בלי לשנות מאפיין זה, תגרור רק את הדף הראשון ותשמור אותו.
            image.save(firstPageOutputPng, PngOptions())

            # שנה את מספר הדף הפעיל לדף השני.
            image.active_page_index = 1

            # שמור את הדף השני של תמונת ה־AI כתמונת PNG.
            image.save(secondPageOutputPng, PngOptions())

            # שנה את מספר הדף הפעיל לדף השלישי.
            image.active_page_index = 2

            # שמור את הדף השלישי של תמונת ה־AI כתמונת PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. האפקט הרטט של הטקסט אינו חל על הטקסט**

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

**PSDPYTHON-23. עיבוד לא נכון של מסיכה בקובץ מסוים**

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

**PSDPYTHON-24. NullReferenceException ב־Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [פורמט AI] תיקון שימוש בזיכרון ב־AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # צריך להיות 220 בשימוש הזכרון ב־C#, אך עבור Python אין לנו גישה ישירה לפעילויות GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # טען את תמונת ה־AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # שמור את הדף הראשון של תמונת ה־AI כתמונת PNG.
            image.save(firstPageOutputPng, pngOpt)

            # שנה את מספר הדף הפעיל לדף השני.
            image.active_page_index = 1

            # שמור את הדף השני של תמונת ה־AI כתמונת PNG.
            image.save(secondPageOutputPng, pngOpt)

            # שנה את מספר הדף הפעיל לדף השלישי.
            image.active_page_index = 2

            # שמור את הדף השלישי של תמונת ה־AI כתמונת PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("שימוש בזיכרון גדול מדי. {} במקום {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}
