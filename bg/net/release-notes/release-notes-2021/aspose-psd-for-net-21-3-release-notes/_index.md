---
title: Aspose.PSD for .NET 21.3 - Бележки за версията
type: docs
weight: 100
url: /bg/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележки за версията на [Aspose.PSD за .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Обобщение**|**Категория**|
| :- | :- | :- |
|PSDNET-823|Добавяне на SectionDividerLayer за подобряване на опита с групи от слоеве|Подобрение|
|PSDNET-694|При четене на PattResource ширината и височината бяха разменени|Проблем|
|PSDNET-789|Неправилно смесване на повече от един ефект на слой|Проблем|
|PSDNET-805|Неправилно смесване на реда и логиката, когато има повече от един ефект на слой|Проблем|
|PSDNET-842|Свойствата на ефекта на контур не се запазват в PSD файл|Проблем|

## **Промени в общественото API**
# **Добавени API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **Премахнати API:**
- Няма

## **Примери за използване:**

**PSDNET-694. При четене на PattResource ширината и височината бяха разменени**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // invoke pattern rendering

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Неправилно смесване на повече от един ефект на слой**

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
                                    // Търсене на слой за текст
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Най-добър";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // По този начин записваме променения PSD файл
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Неправилно смесване на реда и логиката, когато има повече от един ефект на слой**

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

                // По този начин записваме променения PSD файл
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Добавяне на SectionDividerLayer за подобряване на опита с групи от слоеве**

{{< highlight csharp >}}
            // Следният код демонстрира слоевете SectionDividerLayer и как да се получи свързаният с него LayerGroup.

            // Йерархия на слоевете
            //    [0]: '</Layer group>' SectionDividerLayer за Група 1
            //    [1]: 'Слой 1' Обикновен слой
            //    [2]: '</Layer group>' SectionDividerLayer за Група 2
            //    [3]: '</Layer group>' SectionDividerLayer за Група 3
            //    [4]: 'Група 3' Групов слой
            //    [5]: 'Група 2' Групов слой
            //    [6]: 'Група 1' Групов слой

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Обектите не са равни.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Създаване на йерархия на слоевете
                // Добавяне на LayerGroup 'Група 1'
                LayerGroup group1 = image.AddLayerGroup("Група 1", 0, true);
                // Добавяне на обикновен слой
                Layer layer1 = new Layer();
                layer1.DisplayName = "Слой 1";
                group1.AddLayer(layer1);
                // Добавяне на LayerGroup 'Група 2'
                LayerGroup group2 = group1.AddLayerGroup("Група 2", 1);
                // Добавяне на LayerGroup 'Група 3'
                LayerGroup group3 = group2.AddLayerGroup("Група 3", 0);

                // Получаване на SectionDividerLayer's
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // Използвайки метода SectionDividerLayer.GetRelatedLayerGroup(), се получава свързаният екземпляр на LayerGroup.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // същият LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // същият LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // същият LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Група 1' съдържа 5 слоя
            }
{{< /highlight >}}

**PSDNET-842. Свойствата на ефекта на контур не се запазват в PSD файл**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Обектите не са равни.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Няма да хвърли ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Проверка на запазените стойности
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}
