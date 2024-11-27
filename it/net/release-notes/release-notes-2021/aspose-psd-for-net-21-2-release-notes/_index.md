---
title: Note sulla versione di rilascio di Aspose.PSD per .NET 21.2
type: docs
weight: 110
url: /it/net/aspose-psd-per-net-21-2-note-sulla-versione-di-rilascio/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 21.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-404|Supporto di vogkResource|Funzionalità|
|PSDNET-809|Confine del livello di oggetto intelligente non corretto quando sostituiamo i contenuti dell'oggetto intelligente con il file che ha dimensioni e risoluzioni diverse|Funzionalità|
|PSDNET-752|Errore nella conversione del livello FillLayer in SmartObjectLayer|Bug|
|PSDNET-778|Gruppo di livelli che aggiunge nuovi livelli in ordine invertito|Bug|
|PSDNET-790|L'importazione dell'immagine nel livello SmartObject porta alla corruzione del PSD|Bug|
|PSDNET-810|Eccezione durante il caricamento dei file|Bug|
|PSDNET-824|risorsa vogk non corretta dopo il caricamento e il salvataggio dell'immagine PSD con livelli di forma e percorsi vettoriali|Bug|
|PSDNET-827|Eccezione durante il caricamento delle strutture ReferenceStructure ed EnumeratedReferenceStructure|Bug|

## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginType
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginResolution
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginShapeBox
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginRadiiRectangle
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidatedPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginIndexPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginTypePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginResolutionPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginRadiiRectanglePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginShapeBBoxPresent
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Left
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Top
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Right
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bottom
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.QuadVersion
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bounds
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.QuadVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.String,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(Aspose.PSD.Image,Aspose.PSD.ResolutionSetting)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(System.String,Aspose.PSD.ResolutionSetting)

# **API rimosse:**
- Nessuna

## **Esempi d'uso:**

**PSDNET-404. Supporto di vogkResource**

{{< highlight csharp >}}
            // Questo esempio dimostra che il caricamento e il salvataggio dell'immagine PSD con livelli di forma e percorsi vettoriali funziona correttamente.
            string dataDir = "PSDNET404_1";
            string sourcePath = Path.Combine(dataDir, "vectorShapes.psd");
            string outputFilePath = Path.Combine(dataDir, "output_vectorShapes.psd");
            using (PsdImage image = (PsdImage)Image.Load(sourcePath))
            {
                var resource = GetVogkResource(image);
                AssertAreEqual(1, resource.ShapeOriginSettings.Length);
                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, setting.OriginIndex);
                var originalSetting = resource.ShapeOriginSettings[0];
                originalSetting.IsShapeInvalidated = true;
                resource.ShapeOriginSettings = new[]
                {
                    originalSetting,
                    new VectorShapeOriginSettings()
                    {
                        OriginIndex = 1,
                        OriginResolution = 144,
                        OriginType = 4,
                        OriginShapeBox = new VectorShapeBoundingBox()
                        {
                            Bounds = Rectangle.FromLeftTopRightBottom(10, 15, 40, 70)
                        }
                    },
                    new VectorShapeOriginSettings()
                    {
                        OriginIndex = 2,
                        OriginResolution = 301,
                        OriginType = 5,
                        OriginRadiiRectangle = new VectorShapeRadiiRectangle()
                        {
                            TopLeft = 2,
                            TopRight = 6,
                            BottomLeft = 23,
                            BottomRight = 42,
                            QuadVersion = 1
                        }
                    }
                };

                image.Save(outputFilePath, new PsdOptions());
            }

            using (PsdImage image = (PsdImage)Image.Load(outputFilePath))
            {
                var resource = GetVogkResource(image);
                AssertAreEqual(3, resource.ShapeOriginSettings.Length);

                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(true, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, setting.OriginIndex);
                AssertAreEqual(true, setting.IsShapeInvalidated);

                setting = resource.ShapeOriginSettings[1];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(1, setting.OriginIndex);
                AssertAreEqual(144.0, setting.OriginResolution);
                AssertAreEqual(4, setting.OriginType);
                AssertAreEqual(Rectangle.FromLeftTopRightBottom(10, 15, 40, 70), setting.OriginShapeBox.Bounds);

                setting = resource.ShapeOriginSettings[2];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(false, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(true, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(2, setting.OriginIndex);
                AssertAreEqual(301.0, setting.OriginResolution);
                AssertAreEqual(5, setting.OriginType);
                AssertAreEqual(2.0, setting.OriginRadiiRectangle.TopLeft);
                AssertAreEqual(6.0, setting.OriginRadiiRectangle.TopRight);
                AssertAreEqual(23.0, setting.OriginRadiiRectangle.BottomLeft);
                AssertAreEqual(42.0, setting.OriginRadiiRectangle.BottomRight);
                AssertAreEqual(1, setting.OriginRadiiRectangle.QuadVersion);
            }

            VogkResource GetVogkResource(PsdImage image)
            {
                var layer = image.Layers[1];

                VogkResource resource = null;
                var resources = layer.Resources;
                for (int i = 0; i < resources.Length; i++)
                {
                    if (resources[i] is VogkResource)
                    {
                        resource = (VogkResource)resources[i];
                        break;
                    }
                }

                if (resource == null)
                {
                    throw new Exception("Risorsa Vogk non trovata.");
                }

                return resource;
            }

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Gli oggetti non sono uguali.");
                }
            }
{{< /highlight >}}

**PSDNET-752. Errore nella conversione del livello FillLayer in SmartObjectLayer**

{{< highlight csharp >}}
            string sourceFilePath = "effectlost.psd";
            string outputFilePath = "output.psd";

            using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFilePath))
            {
                SmartObjectLayer smartObject = psdImage.SmartObjectProvider.ConvertToSmartObject(0);

                psdImage.Save(outputFilePath);
            }
{{< /highlight >}}

**PSDNET-778. Gruppo di livelli che aggiunge nuovi livelli in ordine invertito**

{{< highlight csharp >}}
            void AreEqual(string expected, string actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("I valori non sono uguali.");
                }
            }

            string outputFile = "output.psd";

            PsdOptions psdOptions = new PsdOptions();
            psdOptions.Source = new StreamSource(new MemoryStream());
            using (PsdImage psdImage = (PsdImage)Image.Create(psdOptions, 100, 100))
            {
                LayerGroup layerGroup = psdImage.AddLayerGroup("Cartella", 0, true);
                layerGroup.AddLayer(new Layer() { DisplayName = "Livello 1" });
                layerGroup.AddLayer(new Layer() { DisplayName = "Livello 2" });

                AreEqual("Livello 1", layerGroup.Layers[0].DisplayName);
                AreEqual("Livello 2", layerGroup.Layers[1].DisplayName);

                psdImage.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-790. Importazione dell'immagine nel livello SmartObject che porta alla corruzione del PSD**

{{< highlight csharp >}}
            const string cartellaBase = "PSDNET790_1\\";
            const string cartellaOutput = cartellaBase + "output\\";

            // Test che il livello, importato da un'immagine, viene convertito in livello di oggetto intelligente e il file PSD salvato è corretto.
            using (PsdImage image = (PsdImage)Image.Load(cartellaBase + @"testLivello1.psd"))
            {

                string percorsoLivello = cartellaBase + @"immagine.jpg";
                string percorsoFileOutput = cartellaOutput + "testLivello2.psd";
                string percorsoPngOutput = Path.ChangeExtension(percorsoFileOutput, ".png");
                using (var stream = new FileStream(percorsoLivello, FileMode.Open))
                {
                    Layer livello = null;
                    try
                    {
                        livello = new Layer(stream);
                        image.AddLayer(livello);
                    }
                    catch (Exception)
                    {
                        if (livello != null)
                        {
                            livello.Dispose();
                        }

                        throw;
                    }

                    var livello2 = image.Layers[2];
                    var livello3 = image.SmartObjectProvider.ConvertToSmartObject(image.Layers.Length - 1);
                    var confini = livello3.Bounds;
                    livello3.Left = (image.Width - livello3.Width) / 2;
                    livello3.Top = livello2.Top;
                    livello3.Right = livello3.Left + confini.Width;
                    livello3.Bottom = livello3.Top + confini.Height;

                    image.Save(percorsoFileOutput);
                    image.Save(percorsoPngOutput, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}

**PSDNET-809. Confine del livello di oggetto intelligente non corretto quando sostituiamo i contenuti dell'oggetto intelligente con il file che ha dimensioni e risoluzioni diverse**

{{< highlight csharp >}}
            // Questo esempio dimostra che il metodo ReplaceContents funziona correttamente quando il nuovo file di contenuto ha una diversa risoluzione.
            const string cartellaBase = "PSDNET809_1\\";
            const string cartellaOutput = cartellaBase + "output\\";
            const string fileName = "CommonPsb.psd";
            const string filePath = cartellaBase + fileName; // immagine PSD originale
            const string percorsoNuovoContenuto = cartellaBase + "immagine.jpg"; // il nuovo file di contenuto per l'oggetto intelligente
            const string percorsoOutputFile = cartellaOutput + "ChangedPsd";
            const string percorsoPngOutput = percorsoOutputFile + ".png"; // il file di output PNG
            const string percorsoPsdOutput = percorsoOutputFile + ".psd"; // il file di output PSD
            using (PsdImage psd = (PsdImage)Image.Load(filePath))
            {
                for (int i = 0; i < psd.Layers.Length; i++)
                {
                    var livello = psd.Layers[i];
                    SmartObjectLayer livelloOggettoIntelligente = livello as SmartObjectLayer;
                    if (livelloOggettoIntelligente != null)
                    {
                        livelloOggettoIntelligente.ReplaceContents(percorsoNuovoContenuto);

                        psd.Save(percorsoPsdOutput);
                        psd.Save(percorsoPngOutput, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
                    }
                }
            }
{{< /highlight >}}

**PSDNET-810. Eccezione durante il caricamento dei file**

{{< highlight csharp >}}
            string fileTest1 = "volto.psd";
            string fileTest2 = "GrandeFile2.psd";

            using (var immaginePsd = (PsdImage)Image.Load(fileTest1))
            {
                // File caricato correttamente
            }

            using (var immaginePsd = (PsdImage)Image.Load(fileTest2))
            {
                // File caricato correttamente
            }
{{< /highlight >}}

**PSDNET-824. risorsa vogk non corretta dopo il caricamento e il salvataggio dell'immagine PSD con livelli di forma e percorsi vettoriali**

{{< highlight csharp >}}
            // Questo esempio dimostra che il caricamento e il salvataggio dell'immagine PSD con livelli di forma e percorsi vettoriali funziona correttamente e le proprietà Live Shape sono conservate.
            string dataDir = "PSDNET824_1\\";
            string srcFile = dataDir + "vectorShapes.psd";
            string outputFilePath = dataDir + @"\output\vectorShapes.psd";
            using (PsdImage psd = (PsdImage)Image.Load(srcFile))
            {
                psd.Save(outputFilePath);
            }

            // Verifica che le proprietà Live Shape siano presenti nel file PSD di output in Adobe® Photoshop®.
{{< /highlight >}}

**PSDNET-827. Eccezione durante il caricamento delle strutture ReferenceStructure ed EnumeratedReferenceStructure**

{{< highlight csharp >}}
            string srcFile = "fileSorgente.psd";
            string output = "output.psd";

            using (var immaginePsd = (PsdImage)Image.Load(srcFile))
            {
                // File caricato correttamente

                SmartObjectLayer livello = (SmartObjectLayer)immaginePsd.Layers[1];
                SoLdResource risorsa = (SoLdResource)livello.Resources[9];

                DescriptorStructure struttura1 = (DescriptorStructure)risorsa.Items[15];
                ListStructure struttura2 = (ListStructure)struttura1.Structures[5];
                DescriptorStructure struttura3 = (DescriptorStructure)struttura2.Types[1];
                DescriptorStructure struttura4 = (DescriptorStructure)struttura3.Structures[6];
                ListStructure struttura5 = (ListStructure)struttura4.Structures[1];
                DescriptorStructure struttura6 = (DescriptorStructure)struttura5.Types[0];

                // Caricamento delle strutture ReferenceStructure ed EnumeratedReferenceStructure
                ReferenceStructure strutturaDiRiferimento = (ReferenceStructure)struttura6.Structures[0];
                EnumeratedReferenceStructure strutturaDiRiferimentoEnumerata = (EnumeratedReferenceStructure)strutturaDiRiferimento.Items[0];

                // Le strutture ReferenceStructure ed EnumeratedReferenceStructure sono state caricate correttamente

                immagine