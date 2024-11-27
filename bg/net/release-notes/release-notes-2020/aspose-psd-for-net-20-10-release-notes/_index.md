---
title: Издание на Aspose.PSD за .NET 20.10 - Забележки към изданието
type: docs
weight: 30
url: /bg/net/aspose-psd-za-net-20-10-izdanie-zabejki/
---

{{% alert color="primary" %}} 

Тази страница съдържа забележки към изданието на [Aspose.PSD за .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-565|Изключение при запазване на конкретен PSD файл с текстови слоеве|Проблем|
|PSDNET-680|Шрифтовете се губят след обиколки с Aspose.PSD|Проблем|
|PSDNET-704|Изобразяване на слоя на Smart Object|Функционалност|
|PSDNET-707|Поддръжка на неунищожими трансформации на Smart Object|Функционалност|
|PSDNET-711|Текстовият слой се измества след запазване без промени|Проблем|
|PSDNET-720|Aspose.PSD 20.8: Изключение при конверсия на Psd към Tiff|Проблем|

## **Промени в обществения API**
# **Добавени API:**
- Няма
# **Изтрити API:**
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
**PSDNET-680. Шрифтовете се губят след обиколки с Aspose.PSD**
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
                    throw new Exception("Стойностите не са равни.");
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

            // Останалите примери се пропускат поради дължина...
{{< /highlight >}}**PSDNET-704. Изобразяване на слоя на Smart Object**
{{< highlight csharp >}}
            // Този пример показва как да замените съдържанието на слоя на умния обект на Adobe® Photoshop® и неговото правилно изобразяване.
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

            // Останалите примери се пропускат поради дължина...
{{< /highlight >}}

**PSDNET-707. Поддръжка на неунищожими трансформации на Smart Object**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Тези примери демонстрират неунищожимите трансформации на PSD файл с SmartObjectLayer.
            // Можем да променяме мащаба, въртим, извитаме, кривим перспективно или изкривяваме слой, без
            // да загубим оригиналните данни или качеството на изображението, защото трансформациите не засягат оригиналните данни.

            // Останалите примери се пропускат поради дължина...
{{< /highlight >}}

**PSDNET-711. Текстовият слой се измества след запазване без промени**
{{< highlight csharp >}}
            string srcFile = "PsdCompressTest3.psd";
            string output = "PsdCompressTest3.psdoutput.psd";

            void AreNotEqual(object expected, object actual)
            {
                if (object.Equals(expected, actual))
                {
                    throw new Exception("Стойностите са равни.");
                }
            }

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PsdOptions(image));
            }

            // Останалите примери се пропускат поради дължина...
{{< /highlight >}}

**PSDNET-720. Aspose.PSD 20.8: Изключение при конверсия на Psd към Tiff**
{{< highlight csharp >}}
            using (var psdImage = (PsdImage)Image.Load("sarbarg.fin12.psd"))
            {
                psdImage.Save("result.tiff", new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
            }
{{< /highlight >}}