---
title: Aspose.PSD لـ .NET 21.1 - ملاحظات الإصدار
type: docs
weight: 120
url: /ar/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: استثناء عند محاولة تحويل ملف Psd معين إلى صيغة png|خلل|
|PSDNET-792|استثناء عند حفظ ملف PSD يحتوي على كائن ذكي إلى صيغة PNG|خلل|

## **تغييرات الواجهة البرمجية العامة**
# **تمت إضافة واجهات البرمجة الجديدة:**
- لا شيء

# **تمت إزالة واجهات البرمجة:**
- لا شيء

## **أمثلة الاستخدام:**
**PSDNET-766. Aspose.PSD 20.10: استثناء عند محاولة تحويل ملف Psd معين إلى صيغة png**
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

**PSDNET-792. استثناء عند حفظ ملف PSD يحتوي على كائن ذكي إلى صيغة PNG**
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
                    // البحث عن Smart Object
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // نحن نقوم بتحميل Smart Object Layer من Memory Stream،
                        // ولكن يمكننا استخدام smart.ExportContents(somePath) لتصدير كائن ذكي إلى ملف
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // البحث عن Text Layer
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // يمكننا استخدام UpdateText بسهولة، ولكن هذه الطريقة تمنحنا القدرة على تعديل النص تدريجياً
                                        // إنشاء طبقات نص متعددة الأسطر وميزات تنسيق النص والفقرات الأخرى
                                        // يرجى الحذر. إذا كان محتوى Smart Object ليس PSD، فلا يمكنك استخدام هذه الطريقة لتحرير النص
                                        // في مثل هذه الحالة يجب عليك استخدام واجهة رسومية: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "الأفضل";

                                        // يجب عليك تغيير حجم النص إذا كنت ترغب في جعل الصورة تبدو جيدة.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // الأفضل استخدام ReplaceContents. سيعيد رسم Smart Object تلقائيًا
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // بهذه الطريقة نقوم بحفظ الملف PSD المعدل
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}