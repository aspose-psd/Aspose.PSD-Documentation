---
title: Выпуск Aspose.PSD для .NET 21.3 - Заметки о выпуске
type: docs
weight: 100
url: /ru/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит заметки о выпуске [Aspose.PSD для .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-823|Добавить SectionDividerLayer для улучшения опыта работы с группами слоев|Улучшение|
|PSDNET-694|При чтении PattResource ширина и высота были изменены местами|Ошибка|
|PSDNET-789|Неверное наложение при наличии более одного слоя эффектов|Ошибка|
|PSDNET-805|Неверный порядок и логика наложения при наличии более одного эффекта слоя|Ошибка|
|PSDNET-842|Свойства эффекта обводки не сохраняются в файле PSD|Ошибка|

## **Изменения в публичном API**
# **Добавленные API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **Удаленные API:**
- Нет

## **Примеры использования:**

**PSDNET-694. При чтении PattResource ширина и высота были изменены местами**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // вызвать визуализацию шаблона

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Неверное наложение при наличии более одного слоя эффектов**

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
                                    // Ищем текстовой слой
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Best";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // Таким образом мы сохраняем измененный файл PSD
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Неверный порядок и логика наложения при наличии более одного эффекта слоя**

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

                //Таким образом мы сохраняем измененный файл PSD
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Добавить SectionDividerLayer для улучшения опыта работы с группами слоев**

{{< highlight csharp >}}
            // Следующий код демонстрирует слои SectionDividerLayer и как получить связанный с ним LayerGroup.

            // Иерархия слоев
            //    [0]: '</Layer group>' SectionDividerLayer для Группы 1
            //    [1]: 'Слой 1' Обычный слой
            //    [2]: '</Layer group>' SectionDividerLayer для Группы 2
            //    [3]: '</Layer group>' SectionDividerLayer для Группы 3
            //    [4]: 'Группа 3' GroupLayer
            //    [5]: 'Группа 2' GroupLayer
            //    [6]: 'Группа 1' GroupLayer

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Объекты не равны.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Создание иерархии слоев
                // Добавление LayerGroup 'Группа 1'
                LayerGroup group1 = image.AddLayerGroup("Группа 1", 0, true);
                // Добавление обычного слоя
                Layer layer1 = new Layer();
                layer1.DisplayName = "Слой 1";
                group1.AddLayer(layer1);
                // Добавление LayerGroup 'Группа 2'
                LayerGroup group2 = group1.AddLayerGroup("Группа 2", 1);
                // Добавление LayerGroup 'Группа 3'
                LayerGroup group3 = group2.AddLayerGroup("Группа 3", 0);

                // Получение SectionDividerLayer's
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // используя метод SectionDividerLayer.GetRelatedLayerGroup(), получаем экземпляр связанной LayerGroup.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // та же самая группа
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // та же самая группа
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // та же самая группа

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Группа 1' содержит 5 слоев
            }
{{< /highlight >}}

**PSDNET-842. Свойства эффекта обводки не сохраняются в файле PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Объекты не равны.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Не вызовет исключения ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Проверка сохраненных значений
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}
