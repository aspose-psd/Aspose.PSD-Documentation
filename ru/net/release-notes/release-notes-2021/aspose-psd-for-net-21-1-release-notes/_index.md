---
title: Aspose.PSD для .NET 21.1 - Примечания к выпуску
type: docs
weight: 120
url: /ru/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}} 

Эта страница содержит примечания к [Aspose.PSD для .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Исключение при попытке преобразовать конкретный файл PSD в PNG|Ошибка|
|PSDNET-792|Исключение при сохранении PSD с умным объектом в PNG|Ошибка|

## **Изменения в публичном API**
# **Добавленные API:**
- Нет

# **Удаленные API:**
- Нет

## **Примеры использования:**
**PSDNET-766. Aspose.PSD 20.10: Исключение при попытке преобразовать конкретный файл PSD в PNG**
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

**PSDNET-792. Исключение при сохранении PSD с умным объектом в PNG**
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
                    // Поиск умного объекта
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Мы загружаем слой умного объекта из MemoryStream,
                        // Но мы также можем использовать smart.ExportContents(somePath) для экспорта умного объекта в файл
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Поиск текстового слоя
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Мы можем использовать простое UpdateText, но такой способ дает нам возможность редактировать текст по частям
                                        // Создание многострочных текстовых слоев и другие функции стилизации текста и абзаца
                                        // Пожалуйста, будьте осторожны. Если содержимое умного объекта не является PSD, вы не можете использовать этот способ редактирования текста
                                        // В таком случае вы должны использовать Graphic API: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Лучший";

                                        // Вы должны изменить размер текста, если хотите, чтобы изображение выглядело хорошо.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // Лучше использовать ReplaceContents. Он автоматически перерисовывает умный объект
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // Таким образом мы сохраняем измененный файл PSD
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
