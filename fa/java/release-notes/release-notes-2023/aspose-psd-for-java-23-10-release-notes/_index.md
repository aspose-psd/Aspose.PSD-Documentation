---
title: دفترچه‌های رها سازی Aspose.PSD برای جاوا 23.10
type: اسناد
weight: 40
url: /fa/java/aspose-psd-for-java-23-10-release-notes/
---

{{% alert color="primary" %}} این صفحه شامل دفترچه‌های رها سازی برای [Aspose.PSD برای جاوا 23.10](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.10/) می‌باشد. {{% /alert %}}

| **کلید**       | **خلاصه**                                                                             | **دسته‌بندی** |
|:---------------|:----------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-538    | پشتیبانی از جهت متن عمودی                                                    |    ویژگی   |
| PSDJAVA-542    | استفاده از تنظیمات Stroke از منبع vstk در رندرینگ Stroke شکل                |    ویژگی   |
| PSDJAVA-540    | پیاده‌سازی رندرینگ منطقه داخلی اشکال Stroke                              |    ویژگی   |
| PSDJAVA-541    | رندر نکردن لایه Shape اگر تغییری‌داده نشده است                            |    ویژگی   |
| PSDJAVA-545    | [فرمت AI] اضافه کردن پشتیبانی برای خواندن Header از فایل‌های AI مبتنی بر PDF |    ویژگی   |
| PSDJAVA-546    | روشهای مختلف برای تنظیم رزولوشن فایل Psd کار نمی‌کنند                 |      باگ    |
| PSDJAVA-547    | FontSettings.SetFontsFolders کار نمی‌کند یا Aspose.PSD از قلم نادرست استفاده می‌کند |      باگ    |
| PSDJAVA-548    | دگرگرایی. برطرف کردن استثناء مرجع تهی بر روی PsdImage.Save هنگام حاضر داشتن لایه Shape |      باگ    |

## **تغییرات عمومی API**
# **API های اضافه:**

- M:com.aspose.psd.FontSettings.getGetSystemAlternativeFont
- M:com.aspose.psd.FontSettings.setGetSystemAlternativeFont(boolean)
- M:com.aspose.psd.Graphics.getPaintableImageOptions
- M:com.aspose.psd.Graphics.setPaintableImageOptions(com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.getAutoAdjustPalette
- M:com.aspose.psd.Image.getFileFormat(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.extensions.RegionExtensions.#ctor
- M:com.aspose.psd.fileformats.psd.PsdImage.setResolution(double,double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.getStroke
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.setStroke(com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getEnabled
- ...

# **API های حذف شده:**

- M:com.aspose.psd.Image.isAutoAdjustPalette
- M:com.aspose.psd.ImageOptionsBase.memberwiseClone
- ...

## **مثال های استفاده:**

** PSDJAVA-538. پشتیبانی از جهت متن عمودی **

{{< highlight java >}}
    
    String sourceFile = "src/main/resources/692_lt1.psd";
    String outputFile = "src/main/resources/692_output.png";
    String fontsFolder = "src/main/resources/692_Fonts";

        List<String> fontFolders = new List<>(FontSettings.getFontsFolders());
        fontFolders.add(fontsFolder);
        FontSettings.setFontsFolders(fontFolders.toArray(new String[0]), true);

        try(PsdImage psdImage = (PsdImage)Image.load(sourceFile)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            psdImage.save(outputFile, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-542. استفاده از تنظیمات Stroke از منبع vstk در رندرینگ Stroke شکل **

{{< highlight java >}}

    ...
    
{{< /highlight >}}

...

** PSDJAVA-548. دگرگرایی. برطرف کردن استثناء مرجع تهی بر روی PsdImage.Save هنگام حاضر داشتن لایه Shape **

{{< highlight java >}}

    ...

{{< /highlight >}}