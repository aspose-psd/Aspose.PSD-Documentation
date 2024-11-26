---
title: Примітки до випуску Aspose.PSD для .NET 21.3
type: docs
weight: 100
url: /uk/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до випуску для [Aspose.PSD для .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-823|Додано SectionDividerLayer для поліпшення роботи з групами шарів|Покращення|
|PSDNET-694|При читанні PattResource ширина та висота були поміняні місцями|Помилка|
|PSDNET-789|Некоректне змішування більш ніж одного ефекту шару|Помилка|
|PSDNET-805|Некоректний порядок та логіка змішування при більш ніж одному ефекті шару|Помилка|
|PSDNET-842|Властивості ефекту обводки не зберігаються у файлі PSD|Помилка|

## **Зміни в публічному API**
# **Додані API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **Вилучені API:**
- Немає

## **Приклади використання:**

**PSDNET-694. При читанні PattResource ширина та висота були поміняні місцями**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // виклик рендерингу шаблону

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Некоректне змішування більш ніж одного ефекту шару**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)

                                {
                                    // Пошук шару тексту
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Найкраще";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // Таким чином ми зберігаємо змінений файл PSD
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Некоректний порядок та логіка змішування при більш ніж одному ефекті шару**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                // Таким чином ми зберігаємо змінений файл PSD
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Додано SectionDividerLayer для поліпшення роботи з групами шарів**

{{< highlight csharp >}}
            // У наступному коді представлено шари SectionDividerLayer та як отримати пов'язану з ним LayerGroup.

            // Ієрархія шарів
            //    [0]: '</Layer group>' SectionDividerLayer для Групи 1
            //    [1]: 'Шар 1' Звичайний Шар
            //    [2]: '</Layer group>' SectionDividerLayer для Групи 2
            //    [3]: '</Layer group>' SectionDividerLayer для Групи 3
            //    [4]: 'Група 3' Груповий Шар
            //    [5]: 'Група 2' Груповий Шар
            //    [6]: 'Група 1' Груповий Шар

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Об'єкти не є рівні.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Створення ієрархії шарів
                // Додати LayerGroup 'Група 1'
                LayerGroup group1 = image.AddLayerGroup("Група 1", 0, true);
                // Додати звичайний шар
                Layer layer1 = new Layer();
                layer1.DisplayName = "Шар 1";
                group1.AddLayer(layer1);
                // Додати LayerGroup 'Група 2'
                LayerGroup group2 = group1.AddLayerGroup("Група 2", 1);
                // Додати LayerGroup 'Група 3'
                LayerGroup group3 = group2.AddLayerGroup("Група 3", 0);

                // Отримати SectionDividerLayer's
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // за допомогою методу SectionDividerLayer.GetRelatedLayerGroup(), отримуємо пов'язаний екземпляр LayerGroup.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // та сама Група
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // та сама Група
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // та сама Група

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Група 1' містить 5 шарів
            }
{{< /highlight >}}

**PSDNET-842. Властивості ефекту обводки не зберігаються у файлі PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Об'єкти не є рівні.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Не викличе ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Перевірка збережених значень
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}
