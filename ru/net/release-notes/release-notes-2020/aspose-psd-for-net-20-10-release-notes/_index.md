---
title: Примечания к выпуску Aspose.PSD для .NET 20.10
type: docs
weight: 30
url: /ru/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}} 

На этой странице содержатся примечания к выпуску [Aspose.PSD для .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-565|Исключение при сохранении конкретного файла PSD с текстовыми слоями|Ошибка|
|PSDNET-680|Шрифты потеряны после обхода с помощью Aspose.PSD|Ошибка|
|PSDNET-704|Рендеринг слоя Smart Object|Функция|
|PSDNET-707|Поддержка неразрушающих преобразований Smart Object|Функция|
|PSDNET-711|Слой текста сдвигается после сохранения без изменений|Ошибка|
|PSDNET-720|Aspose.PSD 20.8: Исключение при преобразовании Psd в Tiff|Ошибка|

## **Изменения в общедоступных API**
# **Добавленные API:**
- Нет
# **Удаленные API:**
- Нет

## **Примеры использования:**
**PSDNET-565. Исключение при сохранении конкретного файла PSD с текстовыми слоями**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}

**PSDNET-680. Шрифты потеряны после обхода с помощью Aspose.PSD**
{{< highlight csharp >}}
            string sourceFilePath = "TwoFonts.psd";

            string outputPsd1 = "output1.psd";
            string outputPsd2 = "output2.psd";
            string outputPng1 = "output1.png";
            string outputPng2 = "output2.png";

            void AreEqual(int expected, int actual)
            {
                if (expected != actual)
                {
                    throw new Exception("Значения не совпадают.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd1, new PsdOptions(psdImage));
                psdImage.Save(outputPng1, new PngOptions());
            }

            using (var psdImage = (PsdImage)Image.Load(outputPsd1))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd2, new PsdOptions(psdImage));
                psdImage.Save(outputPng2, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-704. Рендеринг слоя Smart Object**
{{< highlight csharp >}}
            // Этот пример демонстрирует, как заменить содержимое слоя смарт-объекта Adobe® Photoshop® и его правильное рендеринг.
            string dataDir = "PSDNET704_1\\";
            string filePath = dataDir + "new_panama-papers-4-trans4.psd";
            string pngOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.png";
            string psdOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.psd";
            string newContentPath = dataDir + "new_huset.jpg";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                smartObjectLayer.ReplaceContents(newContentPath);
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }

            // Этот пример демонстрирует, как обновить кэш изображения слоя смарт-объектов Adobe® Photoshop® и их корректное рендеринг.
            filePath = dataDir + "LayeredSmartObjects8bit2.psd";
            pngOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.png";
            psdOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.psd";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                image.SmartObjectProvider.UpdateAllModifiedContent();
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }
{{< /highlight >}}

**PSDNET-707. Поддержка неразрушающих преобразований Smart Object**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Эти примеры демонстрируют неразрушающие преобразования файла PSD с SmartObjectLayer.
            // Мы можем масштабировать, вращать, наклонять, искажать, трансформировать перспективно или искажать слой без
            // потери оригинальных данных или качества, поскольку трансформации не влияют на исходные данные.

            // Этот пример демонстрирует, как изменить размер изображения Adobe® Photoshop® со слоями смарт-объекта:
            ПримерМасштабированияСлояСмартОбъектаИзображения("new_panama-papers-8-trans4-linked");
            ПримерМасштабированияСлояСмартОбъектаИзображения("picture-frame-4-linked3");
            ПримерМасштабированияСлояСмартОбъектаИзображения("gorilla");

            // Этот пример демонстрирует, как изменить размер файла PSD со слоями смарт-объекта.
            void ПримерМасштабированияСлояСмартОбъектаИзображения(string fileName)
            {
                const int масштаб = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Resize_" + fileName + ".psd";
                string outputPngPath = outputDir + "Resize_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int новаяШирина = image.Width * масштаб;
                    int новаяВысота = image.Height * масштаб;
                    image.Resize(новаяШирина, новаяВысота);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Этот пример демонстрирует, как изменить размер слоя смарт-объекта Adobe® Photoshop®.
            ПримерМасштабированияСлояСмартОбъекта("new_panama-papers-8-trans4-linked");
            ПримерМасштабированияСлояСмартОбъекта("gorilla");

            // Этот пример демонстрирует, как изменить размер слоя смарт-объекта в файле PSD.
            void ПримерМасштабированияСлояСмартОбъекта(string fileName)
            {
                const double масштаб = 3.5;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "ResizeLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "ResizeLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    int новаяШирина = (int)(smartObjectLayer.Width * масштаб);
                    int новаяВысота = (int)(smartObjectLayer.Height * масштаб);
                    smartObjectLayer.Resize(новаяШирина, новаяВысота);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Этот пример демонстрирует, как обрезать слой смарт-объекта Adobe® Photoshop®.
            ПримерОбрезкиСлояСмартОбъекта("new_panama-papers-8-trans4-linked");
            ПримерОбрезкиСлояСмартОбъекта("gorilla");

            // Этот пример демонстрирует, как обрезать слой смарт-объекта в файле PSD.
            void ПримерОбрезкиСлояСмартОбъекта(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "CropLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "CropLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.Crop(25, 15, 30, 10);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}

**PSDNET-711. Сдвиг слоя текста после сохранения без изменений**
{{< highlight csharp >}}
            string srcFile = "PsdCompressTest3.psd";
            string output = "PsdCompressTest3.psdoutput.psd";

            void AreNotEqual(object expected, object actual)
            {
                if (object.Equals(expected, actual))
                {
                    throw new Exception("Значения совпадают.");
                }
            }

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PsdOptions(image));
            }

            using (PsdImage image = (PsdImage)Image.Load(output))
            {
                TextLayer txtLayer = (TextLayer)image.Layers[2];

                AreNotEqual(txtLayer.Left, txtLayer.TransformMatrix[4]);
                AreNotEqual(txtLayer.Top, txtLayer.TransformMatrix[5]);
            }
{{< /highlight >}}

**PSDNET-720. Aspose.PSD 20.8: Исключение при конвертации Psd в Tiff**
{{< highlight csharp >}}
            using (var psdImage = (PsdImage)Image.Load("sarbarg.fin12.psd"))
            {
                psdImage.Save("result.tiff", new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
            }
{{< /highlight >}}