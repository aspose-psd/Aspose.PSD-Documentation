---
title: תמותחות הגשה ב-Aspose.PSD עבור Python via .NET 24.7 - רשימות השחרור
type: מסמכים
weight: 10
url: /he/python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

עמוד זה מכיל רשימות שחרור עבור [Aspose.PSD עבור Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **מפתח**      | **סיכום**                                                                                                       | **קטגוריה** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | חריגת "טעינת תמונה נכשלה" כאשר נפתח מסמך AI                                            | באג      |
| PSDPYTHON-87 | הטקסט נראה באופן שגוי בקבצי PDF המוצאים                                                | באג      |
| PSDPYTHON-88 | תיקון ImageSaveException: ייצא תמונה ניכשל עבור הקובץ הנתון ב-Linux                          | באג      |
| PSDPYTHON-89 | תיקון טעינת גופנים בשימוש ב-Aspose.Drawing                                                    | באג      |
| PSDPYTHON-90 | 'פעולה אריתמטית גרמה להתמוססות' ביצירה של שכבת עצם חכמה בשימוש ב-JPEG גדול | באג      |
| PSDPYTHON-91 | הקובץ AI לא יכול להיות ממומר לקובץ JPG                                                   | באג      |

## **שינויים ב-API הציבוריים**
# **APIs הנוספים:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs ההוסרו:**
- אף אחד

## **דוגמאות שימוש:**

**PSDPYTHON-86. חריגת "טעינת תמונה נכשלה" כאשר נפתח מסמך AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. הטקסט נראה באופן שגוי בקבצי PDF המוצאים**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. תיקון ImageSaveException: ייצא תמונה ניכשל עבור הקובץ הנתון ב-Linux**
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


**PSDPYTHON-89. תיקון טעינת גופנים בשימוש ב-Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- לפני העדכון. מספר הגופנים שהותקנו: " + str(len(installedFonts.families)))
            print("- מרענן את מטמון הגופנים על ידי ניסיון לקבל את שם הגופן של Adobe עבור 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- לאחר העדכון. מספר הגופנים שהותקנו: " + str(len(installedFonts.families))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'פעולה אריתמטית גרמה להתמוססות' ביצירה של שכבת עצם חכמה בשימוש ב-JPEG גדול**
{{< highlight python >}}
        # תיקון הוחל, אך קיימת בעיה נוספת ב-Aspose.PSD עבור Python שמונעת את הבדיקה הזו
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "שכבת בדיקה"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. הקובץ AI לא יכול להיות ממומר לקובץ JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}
