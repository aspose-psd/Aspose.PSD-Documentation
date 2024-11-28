---
title: Aspose.PSD за .NET 21.1 - Бележки за версията
type: docs
weight: 120
url: /bg/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD за .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Изключение при опит за конвертиране на конкретен Psd файл към png|Проблем|
|PSDNET-792|Изключение при запазване на PSD с умни обекти в PNG|Проблем|

## **Промени в общественото API**
# **Добавени API:**
- Няма

# **Премахнати API:**
- Няма

## **Примери за използване:**
**PSDNET-766. Aspose.PSD 20.10: Изключение при опит за конвертиране на конкретен Psd файл към png**
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

**PSDNET-792. Изключение при запазване на PSD с умни обекти в PNG**
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
                    // Търсене на умен обект
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Зареждаме умен слой от Memory Stream,
                        // Но можем да използваме smart.ExportContents(somePath), за да експортираме умния обект към файл
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Търсене на текстов слой
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Можем да използваме прост UpdateText, но по този начин получаваме възможност за редактиране на текст по части
                                        // Създаване на многоредови текстови слоеве и други функции за стилизиране на текст и абзаци
                                        // Моля, бъдете внимателни. Ако съдържанието на умния обект не е PSD, не можете да използвате този начин за редактиране на текста
                                        // В такъв случай трябва да използвате Graphic API: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Най-добър";

                                        // Трябва да промените размера на текста, ако искате изображението да изглежда добре.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // По-добре е да използвате ReplaceContents. Той автоматично ще пререндира умния обект
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // По този начин запазваме променения PSD файл
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
