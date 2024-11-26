---
title: Примітки до версії Aspose.PSD для .NET 20.10
type: docs
weight: 30
url: /uk/net/aspose-psd-dlya-net-20-10-primichki-do-versiyi/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до версії [Aspose.PSD для .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-565|Виняток при збереженні конкретного файлу PSD з текстовими шарами|Помилка|
|PSDNET-680|Шрифти втрачаються після обробок з Aspose.PSD|Помилка|
|PSDNET-704|Відтворення шару Smart Object|Функція|
|PSDNET-707|Підтримка неруйнівних перетворень Smart Object|Функція|
|PSDNET-711|Шар тексту зсунутий після збереження без будь-яких змін|Помилка|
|PSDNET-720|Aspose.PSD 20.8: Виняток під час конвертації Psd у Tiff|Помилка|

## **Зміни в API для загального використання**
# **Додані API:**
- Жодних
# **Видалені API:**
- Жодних

## **Приклади використання:**
**PSDNET-565. Виняток при збереженні конкретного файлу PSD з текстовими шарами**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. Шрифти втрачаються після обробок з Aspose.PSD**
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
                    throw new Exception("Значення не рівні.");
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
**PSDNET-704. Відтворення шару Smart Object**
{{< highlight csharp >}}
            // Цей приклад демонструє, як замінити вміст шару об'єкта Smart Object Adobe® Photoshop® та правильно відтворити його.
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

            // Цей приклад демонструє, як оновити кеш зображення шарів об'єктів Smart Object Adobe® Photoshop® та правильно їх відтворити.
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
**PSDNET-707. Підтримка неруйнівних перетворень Smart Object**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Ці приклади демонструють неруйнівні перетворення файлу PSD з SmartObjectLayer.
            // Ми можемо масштабувати, обертати, нахиляти, деформувати, здійснювати перспективні перетворення або спотворювати шар, не втрачаючи початкових даних або якості зображення, оскільки перетворення не впливають на початкові дані.

            // Цей приклад демонструє, як змінити розмір зображення Adobe® Photoshop® з розумними об'єктними шарами:
            ExampleOfSmartObjectImageResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageResizeSupport("picture-frame-4-linked3");
            ExampleOfSmartObjectImageResizeSupport("gorilla");

            // Цей приклад демонструє, як змінити розмір файлу PSD з розумними об'єктними шарами.
            void ExampleOfSmartObjectImageResizeSupport(string fileName)
            {
                const int scale = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Resize_" + fileName + ".psd";
                string outputPngPath = outputDir + "Resize_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int newWidth = image.Width * scale;
                    int newHeight = image.Height * scale;
                    image.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Цей приклад демонструє, як змінити розмір об'єктного шару Adobe® Photoshop®.
            ExampleOfSmartObjectLayerResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerResizeSupport("gorilla");

            // Цей приклад демонструє, як змінити розмір шара об'єкта в файлі PSD.
            void ExampleOfSmartObjectLayerResizeSupport(string fileName)
            {
                const double scale = 3.5;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "ResizeLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "ResizeLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    int newWidth = (int)(smartObjectLayer.Width * scale);
                    int newHeight = (int)(smartObjectLayer.Height * scale);
                    smartObjectLayer.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Цей приклад демонструє, як обрізати шар об'єкта Adobe® Photoshop®.
            ExampleOfSmartObjectLayerCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerCropSupport("gorilla");

            // Цей приклад демонструє, як обрізати шар об'єкта в файлі PSD.
            void ExampleOfSmartObjectLayerCropSupport(string fileName)
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

            // Цей приклад демонструє, як обрізати шар об'єкта Adobe® Photoshop®.
            ExampleOfSmartObjectImageCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageCropSupport("gorilla");

            // Цей приклад демонструє, як обрізати файл PSD з розумними об'єктними шарами.
            void ExampleOfSmartObjectImageCropSupport(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Crop_" + fileName + ".psd";
                string outputPngPath = outputDir + "Crop_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.Crop(25, 10, 30, 5);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Цей приклад демонструє, як обертати та віддзеркалити зображення Adobe® Photoshop® з розумними об'єктними шарами:
            ExampleOfSmartObjectImageRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Цей приклад демонструє, як обертати та віддзеркалити файл PSD з розумними об'єктними шарами.
            void ExampleOfSmartObjectImageRotateFlipSupport(string fileName, RotateFlipType rotateFlipType)
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

            // Цей приклад демонструє, як обертати та віддзеркалити шар об'єкта Adobe® Photoshop®.
            ExampleOfSmartObjectLayerRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // Цей приклад демонструє, як обертати та віддзеркалити шар об'єкта в файлі PSD.
            void ExampleOfSmartObjectLayerRotateFlipSupport(string fileName, RotateFlipType rotateFlipType)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + rotateFlipType + "Last_" + fileName + ".psd";
                string outputPngPath = outputDir + rotateFlipType + "Last_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.RotateFlip(rotateFlipType);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Цей приклад демонструє, як обертати шар об'єкта Adobe® Photoshop® на будь-який кут:
            const string AngleFormat = "+#;-#;+0";
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, false);
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, true);

            // Цей приклад демонструє, як обертати шар об'єкта в файлі PSD на будь-який кут.
            void ExampleOfSmartObjectLayerRotateSupport(string fileName, float angle, bool resizeProportionally)
            {
                string prefix = "RotateLast" +  angle.ToString(AngleFormat) + (resizeProportion