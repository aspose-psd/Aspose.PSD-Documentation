---
title: Aspose.PSD для .NET 21.1 - Примітки до випуску
type: docs
weight: 120
url: /uk/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до випуску для [Aspose.PSD для .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Зміст**|**Категорія**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Виняток при спробі конвертувати певний файл Psd у png|Помилка|
|PSDNET-792|Виняток при збереженні PSD з об'єктом Smart в PNG|Помилка|

## **Зміни у публічному API**
# **Додані API:**
- Немає

# **Вилучені API:**
- Немає

## **Приклади використання:**
**PSDNET-766. Aspose.PSD 20.10: Виняток при спробі конвертування певного файлу Psd у png**
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

**PSDNET-792. Виняток при збереженні PSD з об'єктом Smart в PNG**
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
                    // Пошук об'єкта Smart
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Ми завантажуємо шар об'єкта Smart із пам'яті,
                        // Але ми можемо використовувати smart.ExportContents(somePath) для експорту об'єкта Smart в файл
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Пошук текстового шару
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Ми можемо використовувати просте оновлення тексту, але цей спосіб надає нам можливість редагувати текст частинами
                                        // Створюйте рядки текстових шарів та інші функції стилізації тексту та абзаців
                                        // Будь ласка, будьте обережні. Якщо зміст об'єкта Smart не є PSD, ви не можете використовувати цей спосіб редагування тексту
                                        // У такому випадку вам слід використовувати Графічний API: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Кращий";

                                        // Ви повинні змінити розмір тексту, якщо хочете, щоб зображення виглядало добре.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // Краще використовувати ReplaceContents. Це автоматично перерендерить об'єкт Smart
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // Таким чином ми зберігаємо змінений файл PSD
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
