---
title: Aspose.PSD dla .NET 20.11 - Notatki dotyczące wydania
type: docs
weight: 20
url: /pl/net/aspose-psd-dla-net-20-11-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 20.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-713|Aspose.PSD nie może konwertować plików PSD do innych trybów kolorów/głębi bitowej bez zapisywania ich jako pliki|Funkcja|
|PSDNET-754|Dodaj możliwość kopiowania warstwy Smart Object w obrazie PSD|Funkcja|
|PSDNET-267|Wyjątek podczas ładowania i zapisywania pliku PSD z efektami warstwy|Błąd|
|PSDNET-579|Metoda "Image.LoadRawData" zgłasza wyjątek NullPointer|Błąd|
|PSDNET-741|Rzucany jest wyjątek ImageLoadException podczas próby otwarcia pliku|Błąd|
|PSDNET-744|Aspose.PSD 20.10: Nie można załadować pliku Psd|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.Convert(Aspose.PSD.ImageOptions.PsdOptions)
- F:Aspose.PSD.FileFormats.Psd.ResourceBlock.ResouceBlockMeSaSignature
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.NewSmartObjectViaCopy
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.DuplicateLayer
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.NewSmartObjectViaCopy(Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer)
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(System.Int32[])
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
# **Usunięte API:**
- Brak

## **Przykłady użycia:**
**PSDNET-267. Wyjątek podczas ładowania i zapisywania pliku PSD z efektami warstwy**
{{< highlight csharp >}}
            string dataDir = "PSDNET267_1\\";
            string inputFilePath = dataDir + "LayerEffectsTest.psd";
            string outputFilePath = dataDir + "LayerEffectsTestOutput.psd";
            using (var image = (PsdImage)Image.Load(inputFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                image.Save(outputFilePath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-579. Metoda "Image.LoadRawData" zgłasza wyjątek NullPointer**
{{< highlight csharp >}}
            string dataDir = "PSDNET579_1\\";
            string srcFile = dataDir + "CmykWithAlpha_raw.psd";
            using (RasterImage image = (RasterImage)Image.Load(srcFile))
            {
                Rectangle rect = image.Bounds;
                RawDataRetriever rawDataRetriever = new RawDataRetriever(rect, image.RawDataSettings);
                image.LoadRawData(rect, image.RawDataSettings, rawDataRetriever);
                rawDataRetriever.GetData();
            }

    class RawDataRetriever : Aspose.PSD.IPartialRawDataLoader
    {
        private readonly byte[] rawData;
        private int rawDataIndex;

        public RawDataRetriever(Rectangle rectangle, RawDataSettings rawDataSettings)
        {
            int totalSize = rawDataSettings.LineSize * rectangle.Height;
            if (totalSize == 0)
            {
                totalSize = rectangle.Width * rectangle.Height * 5;
            }

            this.rawData = new byte[totalSize];
        }

        public byte[] GetData()
        {
            return this.rawData;
        }

        public void Process(Rectangle rectangle, byte[] data, Point start, Point end)
        {
            Array.Copy(data, 0, this.rawData, this.rawDataIndex, data.Length);
            this.rawDataIndex += data.Length;
        }

        public void Process(Rectangle rectangle, byte[] data, Point start, Point end, LoadOptions loadOptions)
        {
            throw new NotImplementedException();
        }
    }
{{< /highlight >}}
**PSDNET-713. Aspose.PSD nie może konwertować plików PSD do innych trybów kolorów/głębi bitowej bez zapisywania ich jako pliki**
{{< highlight csharp >}}
            string dataDir = "PSDNET713_1\\";
            string outputDir = dataDir + "output\\";

            // Te przykłady demonstrują konwersję formatu obrazu PSD na inne tryby kolorów/głębi bitowej.
            KonwersjaObrazu(ColorModes.Szary, 16, 2);
            KonwersjaObrazu(ColorModes.Szary, 8, 2);
            KonwersjaObrazu(ColorModes.Szary,  8, 1);
            KonwersjaObrazu(ColorModes.Rgb, 8, 4);
            KonwersjaObrazu(ColorModes.Rgb, 16, 4);
            KonwersjaObrazu(ColorModes.Cmyk, 8, 5);
            KonwersjaObrazu(ColorModes.Cmyk, 16, 5);

            void KonwersjaObrazu(ColorModes trybKoloru, short liczbaBitowKanału, short liczbaKanałów)
            {
                var kompresja = liczbaBitowKanału > 8 ? CompressionMethod.Raw : CompressionMethod.RLE;
                ZapiszDoPsdNastępnieZaładujIZapiszDoPng(
                    "SheetColorHighlightExample",
                    trybKoloru,
                    liczbaBitowKanału,
                    liczbaKanałów,
                    kompresja,
                    1);
                ZapiszDoPsdNastępnieZaładujIZapiszDoPng(
                    "FillOpacitySample",
                    trybKoloru,
                    liczbaBitowKanału,
                    liczbaKanałów,
                    kompresja,
                    2);
                ZapiszDoPsdNastępnieZaładujIZapiszDoPng(
                    "ClippingMaskRegular",
                    trybKoloru,
                    liczbaBitowKanału,
                    liczbaKanałów,
                    kompresja,
                    3);
            }

            // Zapisuje do PSD, a następnie wczytuje zapisany plik i zapisuje do PNG.
            void ZapiszDoPsdNastępnieZaładujIZapiszDoPng(
                string plik,
                ColorModes trybKoloru,
                short liczbaBitowKanału,
                short liczbaKanałów,
                CompressionMethod kompresja,
                int numerWarstwy)
            {
                string srcFile = dataDir + plik + ".psd";
                string postfix = trybKoloru.ToString() + liczbaBitowKanału + "bity" + liczbaKanałów + "kanały" +
                                 kompresja;
                string fileName = plik + "_" + postfix + ".psd";
                string exportPath = outputDir + fileName;
                PsdOptions psdOptions = new PsdOptions()
                {
                    ColorMode = trybKoloru,
                    ChannelBitsCount = liczbaBitowKanału,
                    ChannelsCount = liczbaKanałów,
                    CompressionMethod = kompresja
                };
                using (var image = (PsdImage)Image.Load(srcFile))
                {
                    image.Convert(psdOptions);

                    RasterCachedImage raster = image.Layers.Length > 0 && numerWarstwy >= 0
                        ? (RasterCachedImage)image.Layers[numerWarstwy]
                        : image;
                    Aspose.PSD.Graphics graphics = new Graphics(raster);
                    int width = raster.Width;
                    int height = raster.Height;
                    Rectangle rect = new Rectangle(
                        width / 3,
                        height / 3,
                        width - (2 * (width / 3)) - 1,
                        height - (2 * (height / 3)) - 1);
                    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

                    image.Save(exportPath);
                }

                string pngExportPath = Path.ChangeExtension(exportPath, "png");
                using (PsdImage image = (PsdImage)Image.Load(exportPath))
                {
                    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
**PSDNET-741. Rzucany jest wyjątek ImageLoadException podczas próby otwarcia pliku**
{{< highlight csharp >}}
            string dataDir = "PSDNET741_1\\";
            string inputFile = dataDir + "input.psd";
            string outputFile = dataDir + "output.psd";

            using (var psdImage = (PsdImage)Image.Load(inputFile))
            {
                psdImage.Save(outputFile, new PsdOptions(psdImage));
            }

            using (var psdImage2 = (PsdImage)Image.Load(outputFile))
            {
                // Brak wyjątku tutaj...
            }
{{< /highlight >}}
**PSDNET-744. Aspose.PSD 20.10: Nie można załadować pliku Psd**
{{< highlight csharp >}}         
            void AreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Wartości nie są równe.");
                }
            }

            string srcFile = "GST-CHALLAN(2)1..psd";
            string output = "output.psd";

            using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
            {
                AreEqual(ResourceBlock.ResouceBlockMeSaSignature, psdImage.ImageResources[23].Signature);
                AreEqual(ResourceBlock.ResouceBlockMeSaSignature, psdImage.ImageResources[24].Signature);
                psdImage.Save(output);
            }
{{< /highlight >}}
**PSDNET-754. Dodaj możliwość kopiowania warstwy Smart Object w obrazie PSD**
{{< highlight csharp >}}
            string dataDir = "PSDNET754_1\\";
            string outputDir = dataDir + "output\\";

            // Te przykłady demonstrują, jak kopiować warstwy obiektów Smart w obrazie PSD.
            PrzykładKopiowaniaWarstwySmartObject("r-embedded-psd");
            PrzykładKopiowaniaWarstwySmartObject("r-embedded-png");
            PrzykładKopiowaniaWarstwySmartObject("r-embedded-transform");
            PrzykładKopiowaniaWarstwySmartObject("new_panama-papers-8-trans4");

            void PrzykładKopiowaniaWarstwySmartObject(string nazwaPliku)
            {
                int numerWarstwy = 0; // Numer warstwy do skopiowania
                string filePath = dataDir + nazwaPliku + ".psd";
                string outputFilePath = outputDir + nazwaPliku + "_copy_" + numerWarstwy;
                string pngOutputPath = outputFilePath + ".png";
                string psdOutputPath = outputFilePath + ".psd";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var warstwaSmartObject = (SmartObjectLayer)image.Layers[numerWarstwy];
                    var nowaWarstwa = warstwaSmartObject.NewSmartObjectViaCopy();
                    nowaWarstwa.IsVisible = false;
                    AssertIsTrue(object.ReferenceEquals(nowaWarstwa, image.Layers[numerWarstwy + 1]));
                    AssertIsTrue(object.ReferenceEquals(warstwaSmartObject, image.Layers[numerWarstwy]));

                    var zduplikowanaWarstwa = warstwaSmartObject.DuplicateLayer();
                    zduplikowanaWarstwa.DisplayName = warstwaSmartObject.DisplayName + " wspólny obraz";
                    AssertIsTrue(object.ReferenceEquals(nowaWarstwa, image.Layers[numerWarstwy + 2]));
                    AssertIsTrue(object.ReferenceEquals(zduplikowanaWarstwa, image.Layers[numerWarstwy + 1]));
                    AssertIsTrue(object.ReferenceEquals(warstwaSmartObject, image.Layers[numerWarstwy]));

                    using (var wewnętrznyObraz = (RasterImage)warstwaSmartObject.LoadContents(null))
                    {
                        // Odwracamy osadzony obrazek Smart Object (dla wewnętrznego obrazu PSD odwracamy tylko jego pierwszą warstwę)
                        OdwróćObraz(wewnętrznyObraz);

                        // Zastępujemy osadzony obraz Smart Object w warstwie PSD
                        warstwaSmartObject.ReplaceContents(wewnętrznyObraz);
                    }

                    // Zduplikowana warstwa dzieli swój osadzony obrazem Smart Object
                    // i musi zostać zaktualizowana w sposób jawnie, w przeciwnym razie jej bufor renderowania pozostanie niezmieniony.
                    // Aktualizujemy każdy obiekt Smart Object, aby upewnić się, że nowa warstwa utworzona przez NewSmartObjectViaCopy
                    // nie dzieli obrazka osadzonego z innymi.
                    image.SmartObjectProvider.UpdateAllModifiedContent();

                    image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                    image.Save(psdOutputPath, new PsdOptions(image));
                }
            }

            // Odwraca obraz rastrowy wraz z obrazem PSD.
            void OdwróćObraz(RasterImage wewnętrznyObraz)
            {
                var wewnętrznyPsdObraz = wewnętrznyObraz as PsdImage;
                if (wewnętrznyPsdObraz != null)
                {
                    OdwróćObrazRastrowy(wewnętrznyPsdObraz.Layers[0]);
                }
                else
                {
                    OdwróćObrazRastrowy(wewnętrznyObraz);
                }
            }

            // Odwraca obraz rastrowy.
            void OdwróćObrazRastrowy(RasterImage wewnętrznyObraz)
            {
                var pixele = wewnętrznyObraz.LoadArgb32Pixels(wewnętrznyObraz.Bounds);
                for (int i = 0; i < pixele.Length; i++)
                {
                    var piksel = pixele[i];
                    var alpha = (int)(piksel & 0xff000000);
                    pixele[i] = (~(piksel & 0x00ffffff)) | alpha;
                }

                wewnętrznyObraz.SaveArgb32Pixels(wewnętrznyObraz.Bounds, pixele);
            }

            void AssertIsTrue(bool warunek)
            {
                if (!warunek)
                {
                    throw new FormatException(string.Format("Oczekiwano prawdy"));
                }
            }
{{< /highlight >}}