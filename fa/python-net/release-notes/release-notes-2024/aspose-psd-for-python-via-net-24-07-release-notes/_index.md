---
title: اسپوز.پی‌اس‌دی برای پایتون از طریق .نت ۲۴.۷ - یادداشت‌های انتشار
type: مستندات
weight: ۱۰
url: /fa/python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های انتشار برای [اسپوز.پی‌اس‌دی برای پایتون از طریق .نت ۲۴.۷](https://pypi.org/project/aspose-psd/) می‌باشد

{{% /alert %}}

| **کلید**      | **خلاصه**                                                                                                       | **دسته‌بندی** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | استثنای "بارگذاری تصویر ناکام ماند." در هنگام باز کردن سند AI                                          | باگ      |
| PSDPYTHON-87 | متن به طور نادرست در فایل‌های PDF خروجی رندر می‌شود                                                  | باگ      |
| PSDPYTHON-88 | رفع استثنای ImageSaveException: ناتوانی در صادر کردن تصویر برای فایل داده شده در لینوکس          | باگ      |
| PSDPYTHON-89 | رفع بارگذاری فونت‌ها در هنگام استفاده از Aspose.Drawing                                               | باگ      |
| PSDPYTHON-90 | 'عملیات حسابی به سطح بالا رسید.' در هنگام ایجاد لایه smart object با استفاده از JPEG بزرگ       | باگ      |
| PSDPYTHON-91 | فایل AI نمی‌تواند به یک فایل JPG تبدیل شود                                                           | باگ      |

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API‌های حذف شده:**
- هیچکدام

## **مثال‌های استفاده:**

**PSDPYTHON-86. "بارگذاری تصویر ناکام ماند." استثنا در هنگام باز کردن سند AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. متن به طور نادرست در فایل‌های PDF خروجی رندر می‌شود**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. رفع استثنای ImageSaveException: ناتوانی در صادر کردن تصویر برای فایل داده شده در لینوکس**
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


**PSDPYTHON-89. رفع بارگذاری فونت‌ها در هنگام استفاده از Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- قبل از به‌روزرسانی. تعداد فونت‌های نصب شده: " + str(len(installedFonts.families)))
            print("- کش فونت را با تلاش برای گرفتن نام فونت Adobe برای 'Arial' به‌روز کنید: ")
            FontSettings.get_adobe_font_name("Arial")
            print("- پس از به‌روزرسانی. تعداد فونت‌های نصب شده: " + str(len(installedFonts.families))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'عملیات حسابی به سطح بالا رسید.' در هنگام ایجاد لایه smart object با استفاده از JPEG بزرگ**
{{< highlight python >}}
        # رفع شده است، اما مسئله دیگری در Aspose.PSD برای پایتون وجود دارد که این تست را محدود می‌کند
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


**PSDPYTHON-91. فایل AI نمی‌تواند به یک فایل JPG تبدیل شود**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}
