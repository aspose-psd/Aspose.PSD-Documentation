---
title: Aspose.PSD за .NET 20.10 - Бележки към версията
type: docs
weight: 30
url: /bg/net/aspose-psd-za-net-20-10-belezki-kam-versiyata/
---

{{% alert color="primary" %}} 

Тази страница съдържа **бележки към версията** за [Aspose.PSD за .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-565|Изключение при запазване на конкретен PSD файл с текстови слоеве|Проблем|
|PSDNET-680|Шрифтовете се губят след връщания с Aspose.PSD|Проблем|
|PSDNET-704|Изобразяване на слоя за интелигентен обект|Функционалност|
|PSDNET-707|Поддръжка на недеструктивни трансформации на интелигентен обект|Функционалност|
|PSDNET-711|Текстовият слой се измества след запазване без промени|Проблем|
|PSDNET-720|Aspose.PSD 20.8: Изключение при конвертиране на Psd в Tiff|Проблем|

## **Промени в публичния API**
# **Добавени API:**
- Няма
# **Премахнати API:**
- Няма

## **Примери за използване:**
**PSDNET-565. Изключение при запазване на конкретен PSD файл с текстови слоеве**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. Шрифтовете се губят след връщания с Aspose.PSD**
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
                    throw new Exception("Стойностите не са еднакви.");
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
**PSDNET-704. Изобразяване на слоя за интелигентен обект**
{{< highlight csharp >}}
            // Този пример показва как да се замести съдържанието на слоя на Adobe® Photoshop® интерлигентен обект и правилно изобразяване.
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

            // Този пример показва как да се актуализира кеша на изображението на слоя на Adobe® Photoshop® интерлигентни обекти и правилно изобразяване.
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
**PSDNET-707. Поддръжка на недеструктивни трансформации на интерлигентен обект**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Тези примери показват недеструктивни трансформации на PSD файла с SmartObjectLayer.
            // Можем да скалираме, завъртаме, отклоняваме, изкривяваме, перспективно трансформираме или извъртаме слой без
            // да загубим оригиналните данни или качество на изображението, защото трансформациите не засягат оригиналните данни.

            // Този пример показва как да оразмерите изображението на Adobe® Photoshop® с умни обекти:
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбекти("new_panama-papers-8-trans4-linked");
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбекти("picture-frame-4-linked3");
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбекти("gorilla");

            // Този пример показва как да оразмерите PSD файла с умни обекти.
            void ПримерЗаПоддръжкаНаИзображениеСУмнитеОбекти(string fileName)
            {
                const int мащаб = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Оразмери_" + fileName + ".psd";
                string outputPngPath = outputDir + "Оразмери_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int новаШирина = image.Width * мащаб;
                    int новаВисочина = image.Height * мащаб;
                    image.Resize(новаШирина, новаВисочина);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Този пример показва как да оразмерите слоя с умен обект на Adobe® Photoshop®.
            ПримерЗаПоддръжкаНаОразмеряванеНаСлойСУменОбект("new_panama-papers-8-trans4-linked");
            ПримерЗаПоддръжкаНаОразмеряванеНаСлойСУменОбект("gorilla");

            // Този пример показва как да оразмерите слой с умни обекти в PSD файла.
            void ПримерЗаПоддръжкаНаОразмеряванеНаСлойСУменОбект(string fileName)
            {
                const double мащаб = 3.5;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "РазмерПоследно_" + fileName + ".psd";
                string outputPngPath = outputDir + "РазмерПоследно_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    int новаШирина = (int)(smartObjectLayer.Width * мащаб);
                    int новаВисочина = (int)(smartObjectLayer.Height * мащаб);
                    smartObjectLayer.Resize(новаШирина, новаВисочина);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Този пример показва как да изрежете слоя с умен обект на Adobe® Photoshop®.
            ПримерЗаПоддръжкаНаИзрязванеНаСлойСУменОбект("new_panama-papers-8-trans4-linked");
            ПримерЗаПоддръжкаНаИзрязванеНаСлойСУменОбект("gorilla");

            // Този пример показва как да изрежете слой с умни обекти в PSD файла.
            void ПримерЗаПоддръжкаНаИзрязванеНаСлойСУменОбект(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "ИзрежиПоследно_" + fileName + ".psd";
                string outputPngPath = outputDir + "ИзрежиПоследно_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.Crop(25, 15, 30, 10);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Този пример показва как да изрежете слоя с умен обект на Adobe® Photoshop®:
            ПримерЗаПоддръжкаНаИзрязванеНаИзображениеСУмнитеОбекти("new_panama-papers-8-trans4-linked");
            ПримерЗаПоддръжкаНаИзрязванеНаИзображениеСУмнитеОбекти("gorilla");

            // Този пример показва как да изрежете PSD файла с умни обекти.
            void ПримерЗаПоддръжкаНаИзрязванеНаИзображениеСУмнитеОбекти(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Изрежи_" + fileName + ".psd";
                string outputPngPath = outputDir + "Изрежи_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.Crop(25, 10, 30, 5);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Този пример показва как да завъртите и обърнете изображението на Adobe® Photoshop® с умен обекти:
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбектиЗавъртиОбърни("gorilla", RotateFlipType.Rotate90FlipNone);
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбектиЗавъртиОбърни("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбектиЗавъртиОбърни("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбектиЗавъртиОбърни("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбектиЗавъртиОбърни("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбектиЗавъртиОбърни("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбектиЗавъртиОбърни("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            ПримерЗаПоддръжкаНаИзображениеСУмнитеОбектиЗавъртиОбърни("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Този пример показва как да завъртите и обърнете PSD файла с умни обекти.
            void ПримерЗаПоддръжкаНаИзображениеСУмнитеОбектиЗавъртиОбърни(string fileName, RotateFlipType rotateFlipType)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + rotateFlipType + "_" + fileName + ".psd";
                string outputPngPath = outputDir + rotateFlipType + "_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.RotateFlip(rotateFlipType);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Този пример показва как да завъртите и обърнете слоя с умен обект на Adobe® Photoshop®.
            ПримерЗаПоддръжкаНаОбърниЗавъртиСлойСУменОбект("gorilla", RotateFlipType.Rotate90FlipNone);
            ПримерЗаПоддръжкаНаОбърниЗавъртиСлойСУменОбект("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            ПримерЗаПоддръжкаНаОбърниЗавъртиСлойСУменОбект("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            ПримерЗаПоддръжкаНаОбърниЗавъртиСлойСУменОбект("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            ПримерЗаПоддръжкаНаОбърниЗавъртиСлойСУменОбект("r3-