---
title: Notatki wydania Aspose.PSD dla .NET 20.10
type: docs
weight: 30
url: /pl/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-565|Wyjątek podczas zapisywania określonego pliku PSD z warstwami tekstowymi|Błąd|
|PSDNET-680|Czcionki są tracone po rundach z Aspose.PSD|Błąd|
|PSDNET-704|Renderowanie warstwy Smart Object|Funkcja|
|PSDNET-707|Wsparcie dla niestrukturalnych transformacji warstwy Smart Object|Funkcja|
|PSDNET-711|Warstwa tekstowa jest przemieszczona po zapisaniu bez żadnych zmian|Błąd|
|PSDNET-720|Aspose.PSD 20.8: Wyjątek konwersji Psd na Tiff|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- Brak
# **Usunięte API:**
- Brak

## **Przykłady użycia:**
**PSDNET-565. Wyjątek podczas zapisywania określonego pliku PSD z warstwami tekstowymi**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. Czcionki są tracone po rundach z Aspose.PSD**
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
                    throw new Exception("Wartości nie są równe.");
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
**PSDNET-704. Renderowanie warstwy Smart Object**
{{< highlight csharp >}}
            // Ten przykład pokazuje, jak zastąpić zawartość warstwy inteligentnego obiektu Adobe® Photoshop®
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

            // Ten przykład pokazuje, jak zaktualizować pamięć cache obrazów warstw inteligentnych obiektów Adobe® Photoshop® oraz ich poprawne renderowanie
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
**PSDNET-707. Wsparcie dla niestrukturalnych transformacji warstwy Smart Object**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Te przykłady demonstrują niestrukturalne transformacje pliku PSD z warstwami SmartObject.
            // Możemy skalować, obracać, przechylać, zniekształcać, transformować perspektywicznie lub zniekształcać warstwę bez 
            // utraty oryginalnych danych obrazu lub jakości, ponieważ transformacje nie wpływają na dane oryginalne.

            // Ten przykład pokazuje, jak zmienić rozmiar obrazu Adobe® Photoshop® z warstwami inteligentnego obiektu:
            PrzykladObslugiZmianyRozmiaruSmartObjectImage("new_panama-papers-8-trans4-linked");
            PrzykladObslugiZmianyRozmiaruSmartObjectImage("picture-frame-4-linked3");
            PrzykladObslugiZmianyRozmiaruSmartObjectImage("gorilla");

            // Ten przykład pokazuje, jak zmienić rozmiar pliku PSD z warstwami inteligentnego obiektu
            void PrzykladZmianyRozmiaruSmartObjectImage(string fileName)
            {
                const int skala = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Resize_" + fileName + ".psd";
                string outputPngPath = outputDir + "Resize_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int nowaSzerokosc = image.Width * skala;
                    int nowaWysokosc = image.Height * skala;
                    image.Resize(nowaSzerokosc, nowaWysokosc);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Ten przykład pokazuje, jak zmienić rozmiar warstwy inteligentnego obiektu Adobe® Photoshop®.
            PrzykladZmianyRozmiaruSmartObjectLayer("new_panama-papers-8-trans4-linked");
            PrzykladZmianyRozmiaruSmartObjectLayer("gorilla");

            // Ten przykład pokazuje, jak zmienić rozmiar warstwy smart obiektu w pliku PSD.
            void PrzykladZmianyRozmiaruSmartObjectLayer(string fileName)
            {
                const double skala = 3.5;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "ResizeLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "ResizeLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    int nowaSzerokosc = (int)(smartObjectLayer.Width * skala);
                    int nowaWysokosc = (int)(smartObjectLayer.Height * skala);
                    smartObjectLayer.Resize(nowaSzerokosc, nowaWysokosc);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Ten przykład pokazuje, jak przyciąć warstwę inteligentnego obiektu Adobe® Photoshop®.
            PrzykladObslugiPrzycinaniaWarstwySmartObject("new_panama-papers-8-trans4-linked");
            PrzykladObslugiPrzycinaniaWarstwySmartObject("gorilla");

            // Ten przykład pokazuje, jak przyciąć warstwę Smart Object w pliku PSD.
            void PrzykladObslugiPrzycinaniaWarstwySmartObject(string fileName)
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

            // Ten przykład pokazuje, jak przyciąć warstwę inteligentnego obiektu Adobe® Photoshop®:
            PrzykladObslugiPrzycinaniaObrazuSmartObject("new_panama-papers-8-trans4-linked");
            PrzykladObslugiPrzycinaniaObrazuSmartObject("gorilla");

            // Ten przykład pokazuje, jak przyciąć plik PSD z warstwami Smart Object.
            void PrzykladObslugiPrzycinaniaObrazuSmartObject(string fileName)
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

            // Ten przykład pokazuje, jak obrócić i odbić obraz Adobe® Photoshop® z warstwami Smart Object:
            PrzykladObslugiObracaniaIOdbiciaObrazuSmartObject("gorilla", RotateFlipType.Rotate90FlipNone);
            PrzykladObslugiObracaniaIOdbiciaObrazuSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            PrzykladObslugiObracaniaIOdbiciaObrazuSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            PrzykladObslugiObracaniaIOdbiciaObrazuSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            PrzykladObslugiObracaniaIOdbiciaObrazuSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            PrzykladObslugiObracaniaIOdbiciaObrazuSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            PrzykladObslugiObracaniaIOdbiciaObrazuSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            PrzykladObslugiObracaniaIOdbiciaObrazuSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Ten przykład pokazuje, jak obrócić i odbić plik PSD z warstwami Smart Object.
            void PrzykladObslugiObracaniaIOdbiciaObrazuSmartObject(string fileName, RotateFlipType rotateFlipType)
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

            // Ten przykład pokazuje, jak obrócić i odbić warstwę inteligentnego obiektu Adobe® Photoshop®.
            PrzykladObslugiObracaniaIOdbiciaWarstwySmartObject("gorilla", RotateFlipType.Rotate90FlipNone);
            PrzykladObslugiObracaniaIOdbiciaWarstwySmartObject("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            PrzykladObslugiObracaniaIOdbiciaWarstwySmartObject("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            PrzykladObslugiObracaniaIOdbiciaWarstwySmartObject("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            PrzykladObslugiObracaniaIOdbiciaWarstwySmartObject("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            PrzykladObslugiObracaniaIOdbiciaWarstwySmartObject("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            PrzykladObslugiObracaniaIOdbiciaWarstwySmartObject("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            PrzykladObslugiObracaniaIOdbiciaWarstwySmartObject("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // Ten przykład pokazuje, jak obrócić warstwę inteligentnego obiektu Adobe® Photoshop® o dowolny kąt:
            const string FormatKąta = "+#;-#;+0";
            PrzykladObslugiObracaniaWarstwySmartObject("gorilla", 45, false);
            PrzykladObslugiObracaniaWarstwySmartObject("gorilla", 45, true);
            PrzykladObslugiObracaniaWarstwySmartObject("r3-embedded-transform2", -30, true);
            PrzykladObslugiObracaniaWarstwySmartObject("r3-embedded-transform2", -30, false);
            PrzykladObslugiObracaniaWarstwySmartObject("new_panama-papers-8-trans4-linked", 190, false);
            PrzykladObslugiObracaniaWarstwySmartObject("new_panama-papers-8-trans4-linked", 190, true);

            // Ten przykład pokazuje, jak obrócić warstwę smart object w pliku PSD o dowolny kąt.
            void PrzykladObslugiObracaniaWarstwySmartObject(string fileName, float angle, bool naPodstawieProporcji)
            {
                string prefix = "RotateLast" +  angle.ToString(FormatKąta) + (naPodstawieProporcji ? "ResizeProportionally" : "") + "_";
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + prefix + fileName + ".psd";
                string outputPngPath = outputDir + prefix + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.Rotate(angle, naPodstawieProporcji, Color.Empty);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Ten przykład pokazuje, jak obrócić obraz Adobe® Photoshop® z warstwami Smart Object o dowolny kąt
            PrzykladObslugiObracania