---
title: دفترچه‌ی انتشار Aspose.PSD برای .NET 21.1
type: مستندات
weight: 120
url: /fa/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}} 

 این صفحه حاوی یادداشت‌های انتشار برای [Aspose.PSD برای .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/) است

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: استثنا هنگام تلاش برای تبدیل فایل خاص Psd به png|خطا|
|PSDNET-792|استثنا در زمان ذخیره PSD با شیوه هوشمند به PNG|خطا|

## **تغییرات API عمومی**
# **API های اضافه شده:**
- هیچ کدام

# **API های حذف‌شده:**
- هیچ کدام

## **نمونه‌های استفاده:**
**PSDNET-766. Aspose.PSD 20.10: استثنا هنگام تلاش برای تبدیل فایل خاص Psd به png**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. استثنا در زمان ذخیره PSD با شیوه هوشمند به PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // به دنبال شیوه هوشمند می‌گردد
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // ما لایه‌ی شیوه هوشمند را از حافظه‌ی جریانی بارگیری می‌کنیم
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // به دنبال لایه‌ی متن می‌گردد
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // می‌توانیم از روش UpdateText ساده استفاده کنیم
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "بهترین";

                                        // اندازه‌ی متن را باید تغییر دهید اگر می‌خواهید تصویر خوب دیده شود.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // استفاده از ReplaceContents بهتر است. این کار منجر به تجدید رسم خودکار شیوه هوشمند می‌شود
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // با این روش فایل PSD تغییریافته را ذخیره می‌کنیم
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
