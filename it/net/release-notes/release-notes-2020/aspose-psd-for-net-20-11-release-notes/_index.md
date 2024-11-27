---
title: Note sulla versione di Aspose.PSD per .NET 20.11
type: docs
weight: 20
url: /it/net/aspose-psd-per-net-20-11-note-sulla-versione/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 20.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-713|Aspose.PSD non può convertire PSD in altri modelli di colore/Profondità di bit senza salvarli come file|Caratteristica|
|PSDNET-754|Aggiunta la capacità di copiare un livello di oggetto Smart nell'immagine PSD|Caratteristica|
|PSDNET-267|Eccezione durante il caricamento e il salvataggio del file PSD con effetti di livello|Errore|
|PSDNET-579|Il metodo "Image.LoadRawData" genera un'eccezione NullPointer|Errore|
|PSDNET-741|Viene generata un'eccezione ImageLoadException quando si tenta di aprire il file|Errore|
|PSDNET-744|Aspose.PSD 20.10: Impossibile caricare Psd|Errore|

## **Modifiche all'API pubblica**
# **API aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.Convert(Aspose.PSD.ImageOptions.PsdOptions)
- F:Aspose.PSD.FileFormats.Psd.ResourceBlock.ResouceBlockMeSaSignature
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.NewSmartObjectViaCopy
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.DuplicateLayer
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.NewSmartObjectViaCopy(Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer)
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(System.Int32[])
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**
**PSDNET-267. Eccezione durante il caricamento e il salvataggio del file PSD con effetti di livello**
{{< highlight csharp >}}
            string dataDir = "PSDNET267_1\\";
            string inputFilePath = dataDir + "LayerEffectsTest.psd";
            string outputFilePath = dataDir + "LayerEffectsTestOutput.psd";
            using (var image = (PsdImage)Image.Load(inputFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                image.Save(outputFilePath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-579. Il metodo "Image.LoadRawData" genera un'eccezione NullPointer**
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
**PSDNET-713. Aspose.PSD non può convertire PSD in altri modelli di colore/Profondità di bit senza salvarli come file**
{{< highlight csharp >}}
            string dataDir = "PSDNET713_1\\";
            string outputDir = dataDir + "output\\";

            // Questi esempi illustrano la conversione del formato immagine PSD in altri modelli di colore/Profondità di bit.
            ConversioneImmagine(ColorModes.Grayscale, 16, 2);
            ConversioneImmagine(ColorModes.Grayscale, 8, 2);
            ConversioneImmagine(ColorModes.Grayscale, 8, 1);
            ConversioneImmagine(ColorModes.Rgb, 8, 4);
            ConversioneImmagine(ColorModes.Rgb, 16, 4);
            ConversioneImmagine(ColorModes.Cmyk, 8, 5);
            ConversioneImmagine(ColorModes.Cmyk, 16, 5);

            void ConversioneImmagine(ColorModes colorMode, short channelBitsCount, short channelsCount)
            {
                var compression = channelBitsCount > 8 ? CompressionMethod.Raw : CompressionMethod.RLE;
                SalvaInPsdPoiCaricaESalvaInPng(
                    "EsempioFoglioColoriEvidenziato",
                    colorMode,
                    channelBitsCount,
                    channelsCount,
                    compression,
                    1);
                SalvaInPsdPoiCaricaESalvaInPng(
                    "EsempioOpacitàRiempimento",
                    colorMode,
                    channelBitsCount,
                    channelsCount,
                    compression,
                    2);
                SalvaInPsdPoiCaricaESalvaInPng(
                    "MascheraRitaglioRegolare",
                    colorMode,
                    channelBitsCount,
                    channelsCount,
                    compression,
                    3);
            }

            // Salva in PSD quindi carica il file salvato e salva in PNG.
            void SalvaInPsdPoiCaricaESalvaInPng(
                string file,
                ColorModes colorMode,
                short channelBitsCount,
                short channelsCount,
                CompressionMethod compression,
                int numeroLivello)
            {
                string srcFile = dataDir + file + ".psd";
                string postfix = colorMode.ToString() + channelBitsCount + "bit" + channelsCount + "canali" +
                                 compression;
                string fileName = file + "_" + postfix + ".psd";
                string exportPath = outputDir + fileName;
                PsdOptions psdOptions = new PsdOptions()
                {
                    ColorMode = colorMode,
                    ChannelBitsCount = channelBitsCount,
                    ChannelsCount = channelsCount,
                    CompressionMethod = compression
                };
                using (var image = (PsdImage)Image.Load(srcFile))
                {
                    image.Convert(psdOptions);

                    RasterCachedImage raster = image.Layers.Length > 0 && numeroLivello >= 0
                        ? (RasterCachedImage)image.Layers[numeroLivello]
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
**PSDNET-741. Viene generata un'eccezione ImageLoadException quando si tenta di aprire il file**
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
                // Nessuna eccezione qui...
            }
{{< /highlight >}}
**PSDNET-744. Aspose.PSD 20.10: Impossibile caricare Psd**
{{< highlight csharp >}}         
            void AreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("I valori non sono uguali.");
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
**PSDNET-754. Aggiunta la capacità di copiare un livello di oggetto Smart nell'immagine PSD**
{{< highlight csharp >}}
            string dataDir = "PSDNET754_1\\";
            string outputDir = dataDir + "output\\";

            // Questi esempi illustrano come copiare i livelli di oggetti Smart in un'immagine PSD.
            EsempioCopiaLivelloOggettoSmart("r-embedded-psd");
            EsempioCopiaLivelloOggettoSmart("r-embedded-png");
            EsempioCopiaLivelloOggettoSmart("r-embedded-transform");
            EsempioCopiaLivelloOggettoSmart("new_panama-papers-8-trans4");

            void EsempioCopiaLivelloOggettoSmart(string fileName)
            {
                int numeroLivello = 0; // Il numero del livello da copiare
                string filePath = dataDir + fileName + ".psd";
                string outputFilePath = outputDir + fileName + "_copy_" + numeroLivello;
                string pngOutputPath = outputFilePath + ".png";
                string psdOutputPath = outputFilePath + ".psd";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = (SmartObjectLayer)image.Layers[numeroLivello];
                    var nuovoLivello = smartObjectLayer.NewSmartObjectViaCopy();
                    nuovoLivello.IsVisible = false;
                    AssertIsTrue(object.ReferenceEquals(nuovoLivello, image.Layers[numeroLivello + 1]));
                    AssertIsTrue(object.ReferenceEquals(smartObjectLayer, image.Layers[numeroLivello]));

                    var livelloDuplicato = smartObjectLayer.DuplicateLayer();
                    livelloDuplicato.DisplayName = smartObjectLayer.DisplayName + " immagine condivisa";
                    AssertIsTrue(object.ReferenceEquals(nuovoLivello, image.Layers[numeroLivello + 2]));
                    AssertIsTrue(object.ReferenceEquals(livelloDuplicato, image.Layers[numeroLivello + 1]));
                    AssertIsTrue(object.ReferenceEquals(smartObjectLayer, image.Layers[numeroLivello]));

                    using (var innerImage = (RasterImage)smartObjectLayer.LoadContents(null))
                    {
                        // Invertiamo l'immagine dell'oggetto inserito (per un'immagine PSD interna invertiamo solo il suo primo livello)
                        InvertiImmagine(innerImage);

                        // Sostituiamo l'immagine dell'oggetto inserito nel livello PSD
                        smartObjectLayer.ReplaceContents(innerImage);
                    }

                    // Il livello duplicato condivide la sua immagine incorporata con l'oggetto smart originale
                    // e dovrebbe essere aggiornato esplicitamente altrimenti la cache di rendering rimane invariata.
                    // Aggiorniamo ogni oggetto smart per assicurarci che il nuovo livello creato da NewSmartObjectViaCopy
                    // non condivida l'immagine incorporata con gli altri.
                    image.SmartObjectProvider.UpdateAllModifiedContent();

                    image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                    image.Save(psdOutputPath, new PsdOptions(image));
                }
            }

            // Inverte l'immagine raster inclusa nell'immagine PSD.
            void InvertiImmagine(RasterImage innerImage)
            {
                var innerPsdImage = innerImage as PsdImage;
                if (innerPsdImage != null)
                {
                    InvertiImmagineRaster(innerPsdImage.Layers[0]);
                }
                else
                {
                    InvertiImmagineRaster(innerImage);
                }
            }

            // Inverte l'immagine raster.
            void InvertiImmagineRaster(RasterImage innerImage)
            {
                var pixels = innerImage.LoadArgb32Pixels(innerImage.Bounds);
                for (int i = 0; i < pixels.Length; i++)
                {
                    var pixel = pixels[i];
                    var alpha = (int)(pixel & 0xff000000);
                    pixels[i] = (~(pixel & 0x00ffffff)) | alpha;
                }

                innerImage.SaveArgb32Pixels(innerImage.Bounds, pixels);
            }

            void AssertIsTrue(bool condition)
            {
                if (!condition)
                {
                    throw new FormatException(string.Format("Previsto vero"));
                }
            }
{{< /highlight >}}