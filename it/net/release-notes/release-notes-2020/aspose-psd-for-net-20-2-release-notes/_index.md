---
title: Note sulla versione di rilascio di Aspose.PSD per .NET 20.2
type: docs
weight: 110
url: /it/net/aspose-psd-for-net-20-2-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-206|Miglioramento della capacità di renderizzare testi di diversi colori nel livello di testo|Funzionalità|
|PSDNET-369|Supporto della risorsa clbl (Layer resource contains info about Blend clipping elements)|Funzionalità|
|PSDNET-274 |Supporto della risorsa blwh (La risorsa contiene dati del Livello di Regolazione Bianco e Nero)|Funzionalità|
|PSDNET-230|Possibilità di esportare Gruppo Livelli in Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Funzionalità|
|PSDNET-372|Supporto della risorsa lspf (Contiene impostazioni sulle impostazioni di protezione del livello)|Funzionalità|
|PSDNET-370|Supporto della risorsa infx (Contiene dati relativi al blending degli elementi interni)|Funzionalità|
|PSDNET-251|Refactoring di PsdImage e Layer per modificare il comportamento di trasformazione (Ridimensionamento/cambio di rotazione/ritaglio corretto per i mask dei livelli se trasformiamo un livello separatamente)|Miglioramento|
|PSDNET-276 |In alcune impostazioni di globalizzazione, l'immagine raster AI non può essere aperta|Bug|
|PSDNET-194|Dopo aver eseguito l'operazione FlipRotate su un livello, l'immagine PSD diventa illeggibile|Bug|
|PSDNET-177. |System.ArgumentException durante il caricamento del file PSD|Bug|
|PSDNET-249|Dopo aver usato un metodo di trasformazione solo per un livello, il livello salvato ha limiti o una maschera incorretti|Bug|

## **Modifiche dell'API pubblica**
# **API Aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskRectangle
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Height
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorRed
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorGreen
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorBlue
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TintColor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor
- P:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues
- T:Aspose.PSD.AggregateException
- M:Aspose.PSD.CmykColor.Equals(System.Object)
- T:Aspose.PSD.CompositeException
- T:Aspose.PSD.CoreExceptions.IndexOutOFRangeException
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String)
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException:#ctor(System.String,System.Exception)
- F:Aspose.PSD.FileFormat.Otg
- T:Aspose.PSD.FileFormats.Jpeg2000.Jpeg2000CustomException
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.IsDataStoredDiscretely
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetChannelData(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetActiveManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetCurveManager
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.TypeToolKey
- T:Aspose.PSD.ImageOptions.TiffOptionsUtils
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.#ctor
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.GetValidTagsCount(Aspose.PSD.FileFormats.Tiff.TiffDataType[])
- P:Aspose.PSD.ImageOptionsBase.ProgressEventHandler
- P:Aspose.PSD.LoadOptions.ProgressEventHandler
- M:Aspose.PSD.Matrix.#ctor(Aspose.PSD.Matrix)
- M:Aspose.PSD.Metered.Equals(System.Object)
- T:Aspose.PSD.ProgressEventHandler
- T:Aspose.PSD.ProgressManagement.EventType
- F:Aspose.PSD.ProgressManagement.EventType.RelativeProgress
- F:Aspose.PSD.ProgressManagement.EventType.StageChange
- F:Aspose.PSD.ProgressManagement.EventType.Initialization
- F:Aspose.PSD.ProgressManagement.EventType.PreProcessing
- F:Aspose.PSD.ProgressManagement.EventType.Processing
- F:Aspose.PSD.ProgressManagement.EventType.Finalization
- T:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Description
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.EventType
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.MaxValue
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Value
- M:Aspose.PSD.RasterImage.GetSkewAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle(System.Boolean,Aspose.PSD.Color)

# **API Rimosse:**
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor(System.Int32)
- F:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues

## **Esempi di utilizzo:**
**PSDNET-206. Miglioramento della capacità di renderizzare testi di diversi colori nel livello di testo**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("text_ethalon_different_colors.psd")) {

    var txtLayer = (TextLayer)psdImage.Layers[1];

    txtLayer.TextData.UpdateLayerData();

    psdImage.Save("output.png", new PngOptions());

}

{{< /highlight >}}

**PSDNET-369. Supporto della risorsa clbl (Layer resource contains info about Blend clipping elements)**

{{< highlight java >}}

        void AssertIsTrue(bool condition, string message) {

            if (!condition) {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "SampleForResource.psd";

        string destinationFileName = "Output" + sourceFileName;

        ClblResource GetClblResource(PsdImage im) {

            foreach (var layer in im.Layers) {

                foreach (var layerResource in layer.Resources) {

                    if (layerResource is ClblResource) {

                        return (ClblResource)layerResource;

                    }

                }

            }

            throw new Exception("La risorsa Clbl specificata non è stata trovata");

        }

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName)) {

            var resource = GetClblResource(im);

            AssertIsTrue(resource.BlendClippedElements, "La proprietà ClblResource.BlendClippedElements dovrebbe essere true");

            // Test di modifica e salvataggio

            resource.BlendClippedElements = false;

            im.Save(destinationFileName);

        }

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName)) {

            var resource = GetClblResource(im);

            AssertIsTrue(!resource.BlendClippedElements, "La proprietà ClblResource.BlendClippedElements dovrebbe essere diventata false");

        }

{{< /highlight >}}

**PSDNET-274. Supporto della risorsa blwh (La risorsa contiene dati del Livello di Regolazione Bianco e Nero)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Il valore di proprietà atteso non è uguale al valore effettivo";

        void AssertIsTrue(bool condition, string message) {

            if (!condition) {

                throw new FormatException(message);

            }

        }

        void ExampleSupportOfBlwhResource(

            string sourceFileName,

            int reds,

            int yellows,

            int greens,

            int cyans,

            int blues,

            int magentas,

            bool useTint,

            int bwPresetKind,

            string bwPresetFileName,

            double tintColorRed,

            double tintColorGreen,

            double tintColorBlue,

            int tintColor,

            int newTintColor

        ) {

            string destinationFileName = "Output" + sourceFileName;

            bool isRequiredResourceFound = false;

            using (PsdImage im = (PsdImage)Image.Load(sourceFileName)) {

                foreach (var layer in im.Layers) {

                    foreach (var layerResource in layer.Resources) {

                        if (layerResource is BlwhResource) {

                            var blwhResource = (BlwhResource)layerResource;

                            var blwhLayer = (BlackWhiteAdjustmentLayer)layer;

                            isRequiredResourceFound = true;

                            AssertIsTrue(blwhResource.Reds == reds, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Yellows == yellows, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Greens == greens, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Cyans == cyans, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Blues == blues, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Magentas == magentas, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.UseTint == useTint, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.TintColor == tintColor, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.BwPresetKind == bwPresetKind, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.BlackAndWhitePresetFileName == bwPresetFileName, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorRed - tintColorRed) < 1e-6, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorGreen - tintColorGreen) < 1e-6, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorBlue - tintColorBlue) < 1e-6, ActualPropertyValueIsWrongMessage);

                            // Test di modifica e salvataggio

                            blwhResource.Reds = reds - 15;

                            blwhResource.Yellows = yellows - 15;

                            blwhResource.Greens = greens + 15;

                            blwhResource.Cyans = cyans + 15;

                            blwhResource.Blues = blues - 15;

                            blwhResource.Magentas = magentas - 15;

                            blwhResource.UseTint = !useTint;

                            blwhResource.BwPresetKind = 4;

                            blwhResource.BlackAndWhitePresetFileName = "bwPresetFileName";

                            blwhLayer.TintColorRed = tintColorRed - 60;

                            blwhLayer.TintColorGreen = tintColorGreen - 60;

                            blwhLayer.TintColorBlue = tintColorBlue - 60;

                            im.Save(destinationFileName);

                            break;

                        }

                    }

                }

            }

            AssertIsTrue(isRequiredResourceFound, "La risorsa Blwh specificata non è stata trovata");

            isRequiredResourceFound = false;

            using (PsdImage im = (PsdImage)Image.Load(destinationFileName)) {

                foreach (var layer in im.Layers) {

                    foreach (var layerResource in layer.Resources) {

                        if (layerResource is BlwhResource) {

                            var blwhResource = (BlwhResource)layerResource;

                            var blwhLayer = (BlackWhiteAdjustmentLayer)layer;

                            isRequiredResourceFound = true;

                            AssertIsTrue(blwhResource.Reds == reds - 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Yellows == yellows - 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Greens == greens + 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Cyans == cyans + 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Blues == blues - 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.Magentas == magentas - 15, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.UseTint == !useTint, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.TintColor == newTintColor, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.BwPresetKind == 4, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(blwhResource.BlackAndWhitePresetFileName == "bwPresetFileName", ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorRed - tintColorRed + 60) < 1e-6, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorGreen - tintColorGreen + 60) < 1e-6, ActualPropertyValueIsWrongMessage);

                            AssertIsTrue(Math.Abs(blwhLayer.TintColorBlue - tintColorBlue + 60) < 1e-6, ActualPropertyValueIsWrongMessage);

                            break;

                        }

                    }

                }

            }

            AssertIsTrue(isRequiredResourceFound, "La risorsa Blwh specificata non è stata trovata");

        }

        ExampleSupportOfBlwhResource(

            "BlackWhiteAdjustmentLayerStripesMask.psd",

            0x28,

            0x3c,

            0x28,

            0x3c,

            0x14,

            0x50,

            false,

            1,

            "\0",

            225.00045776367188,

            211.00067138671875,

            179.00115966796875,

            -1977421,

            -5925001);

        ExampleSupportOfBlwhResource(

            "BlackWhiteAdjustmentLayerStripesMask2.psd",

            0x80,

            0x40,

            0x20,

            0x10,

            0x08,

            0x04,

            true,

            4,

            "\0",

            239.996337890625,

            127.998046875,

            63.9990234375,

            -1015744,

            -4963324);

        Console.WriteLine("L'aggiornamento di BlwhResource funziona come previsto. Premere un tasto.");

{{< /highlight >}}

**PSDNET-230. Possibilità di esportare Gruppo Livelli in Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("1.psd")) {

                // cartella con sfondo

                LayerGroup bg_folder = (LayerGroup)psdImage.Layers[0];

                // cartella con contenuto

                LayerGroup content_folder = (LayerGroup)psdImage.Layers[4];

                bg_folder.Save("sfondo.png", new PngOptions());

                content_folder.Save("contenuto.png", new PngOptions());

            }

{{< /highlight >}}

**PSDNET-372. Supporto della risorsa lspf (Contiene impostazioni sulle impostazioni di protezione del livello)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Il valore di proprietà atteso non è uguale al valore effettivo";

        void AssertIsTrue(bool condition, string message) {

            if (!condition) {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "CampionePerLaRisorsa.psd";

        string destinationFileName = "Output" + sourceFileName;

        bool isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName)) {

            foreach (var layer in im.Layers) {

                foreach (var layerResource in layer.Resources) {

                    if (layerResource is LspfResource) {

                        var resource = (LspfResource)layerResource;

                        isRequiredResourceFound = true;

                        AssertIsTrue(false == resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        // Test di modifica e salvataggio

                        resource.IsCompositeProtected = true;

                        AssertIsTrue(true == resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        resource.IsCompositeProtected = false;

                        resource.IsPositionProtected = true;

                        AssertIsTrue(false == resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(true == resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        resource.IsPositionProtected = false;

                        resource.IsTransparencyProtected = true;

                        AssertIsTrue(false == resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(true == resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        resource.IsCompositeProtected = true;

                        resource.IsPositionProtected = true;

                        resource.IsTransparencyProtected = true;

                        im.Save(destinationFileName);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(isRequiredResourceFound, "La risorsa Lspf specificata non è stata trovata");

        isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName)) {

            foreach (var layer in im.Layers) {

                foreach (var layerResource in layer.Resources) {

                    if (layerResource is LspfResource) {

                        var resource = (LspfResource)layerResource;

                        isRequiredResourceFound = true;

                        AssertIsTrue(resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(isRequiredResourceFound, "La risorsa Lspf specificata non è stata trovata");

        Console.WriteLine("L'aggiornamento di LspfResource funziona come previsto. Premere un tasto.");

{{< /highlight >}}

**PSDNET-370. Supporto della risorsa infx (Contiene dati relativi al blending degli elementi interni)**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message) {

            if (!condition) {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "EsempioPerLaRisorsa.psd";

        string destinationFileName = "Output" + sourceFileName;

        bool isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName)) {

            foreach (var layer in im.Layers) {

                foreach (var layerResource in layer.Resources) {

                    if (layerResource is InfxResource) {

                        var resource = (InfxResource)layerResource;

                        isRequiredResourceFound = true;

                        AssertIsTrue(!resource.BlendInteriorElements, "La proprietà InfxResource.BlendInteriorElements dovrebbe essere falsa");

                        // Test di modifica e salvataggio

                        resource.BlendInteriorElements = true;

                        im.Save(destinationFileName);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(isRequiredResourceFound, "La risorsa Infx specificata non è stata trovata");

        isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName)) {

            foreach (var layer in im.Layers) {

                foreach (var layerResource in layer.Resources) {

                    if (layerResource is InfxResource) {

                        var resource = (InfxResource)layerResource;

                        isRequiredResourceFound = true;

                        AssertIsTrue(resource.BlendInteriorElements, "La proprietà InfxResource.BlendInteriorElements dovrebbe essere cambiata in vero");

                        break;

                    }

                }

            }

        }

        AssertIsTrue(isRequiredResourceFound, "La risorsa Infx specificata non è stata trovata");

{{< /highlight >}}

**PSDNET-251. Refactoring di PsdImage e Layer per modificare il comportamento di trasformazione (Ridimensionamento/cambio di rotazione/ritaglio corretto per i mask dei livelli se trasformiamo un livello separatamente)**

{{< highlight java >}}

             var enums = (RotateFlipType[])Enum.GetValues(typeof(RotateFlipType));

            var fileNames = new string[] {

                "UnNormaleEUmAdjustrnentConVettoreEUmMaskDelLivello",

                "UnNormaleEUmAdjustrnentConMaskDelLivello", 

                "LivelloDiTesto",

                "FormeCollegateConTesto"

            };

            foreach (string fileName in fileNames) {

                foreach (RotateFlipType rotateFlipType in enums) {

                    string sourceFileName = fileName + ".psd";

                    string destinationFileName = fileName + "_" + rotateFlipType;

                    var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

                    using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions)) {

                        image.RotateFlip(rotateFlipType);

                        image.Save(destinationFileName);

                    }

                }

            }

{{< /highlight >}}

**PSDNET-276. In alcune impostazioni di globalizzazione, l'immagine raster AI non può essere aperta**

{{< highlight java >}}

        string sourceFileName = "raster_form_8.ai";

        System.Threading.Thread.CurrentThread.CurrentCulture = new System.Globalization.CultureInfo("ru_RU");

        System.Threading.Thread.CurrentThread.CurrentUICulture = System.Threading.Thread.CurrentThread.CurrentCulture;

        using (AiImage image = (AiImage)Image.Load(sourceFileName)) {

            // non dovrebbero essere generate eccezioni

        }

{{< /highlight >}}

**PSDNET-194. Dopo aver eseguito l'operazione FlipRotate su un livello, l'immagine PSD diventa illeggibile**

{{< highlight java >}}

             string sourceFileName = OttieniFileNellaCartellaPersonalizzataRelativamenteABase(@"datiTest\Problemi\IMAGINGNET-2617\1.psd");

            var flipType = RotateFlipType.Rotate90FlipNone;

            var outFileNamePsd = this.GetFileInOutputFolder("TestDiRotazioneFlip2617.psd");

            try {

                using (PsdImage image = (PsdImage)Image.Load(sourceFileName)) {

                    for (int i = 0; i < image.Layers.Length; i++) {

                        var layer = image.Layers[i];

                        if (!layer.Bounds.IsEmpty) {

                            layer.RotateFlip(flipType);

                        }

                    }

                    string outFileNamePng = this.GetFileInOutputFolder("TestDiRotalionFlip2617.png");

                    image.Save(outFileNamePsd);

                }

            // Qui otteniamo un'eccezione. Anche per PhotoShop questo file è illeggibile,

            using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) { // Genera un'eccezione

            {

                // Non fare nulla

            }

{{< /highlight >}}

**PSDNET-177. System.ArgumentException durante il caricamento del file PSD**

{{< highlight java >}}

         string sourcePath = "1.psd";

        string psdPath = "TestDiRotazioneFlip2617.psd";

        RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

        using (var im = (PsdImage)(Image.Load(sourcePath))) {

            im.RotateFlip(flipType);

            im.Save(psdPath);

        }

        using (var im =(PsdImage)(Image.Load(psdPath))) { // Qui non dovrebbero verificarsi eccezioni

            // non fare nulla

        }

{{< /highlight >}}

**PSDNET-249. Dopo aver usato un metodo di trasformazione solo per un livello, il livello salvato ha limiti o una maschera incorretti**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message) {

            if (!condition) {

                throw new FormatException(message);

            }

        }

        const double Tolleranza = 1e-6;

        int nuovaLarghezza = 132;

        int nuovaAltezza = 247;

        double xScale = nuovaLarghezza / 48.0;

        double yScale = nuovaAltezza / 19.0;

        string sourceFileName = "LivelloDiTesto.psd";

        string outputFileName = "LivelloDiTestoResize" + nuovaLarghezza + "_" + nuovaAltezza;

        var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

        using (PsdImage image = (PsdImage) Image.Load(sourceFileName, psdLoadOptions)) {

            var layer = image.Layers[1] as TextLayer;

            var nuovoSinistro = layer.Sinistro - (nuovaLarghezza - layer.Larghezza) / 2;

            var nuovoTop = layer.Top - (nuovaAltezza - layer.Altezza) / 2;

            layer.Resize(nuovaLarghezza, nuovaAltezza);

            AssertIsTrue(layer.Sinistro == nuovoSinistro, "La proprietà di Sinistro del livello dovrebbe essere " + nuovoSinistro);

            AssertIsTrue(layer.Top == nuovoTop, "La proprietà Top del livello dovrebbe essere " + nuovoTop);

            AssertIsTrue(layer.Larghezza == nuovaLarghezza, "La proprietà Larghezza del livello dovrebbe essere " + nuovaLarghezza);

            AssertIsTrue(layer.Altezza == nuovaAltezza, "La proprietà Altezza del livello dovrebbe essere " + nuovaAltezza);

            AssertIsTrue(Math.Abs(layer.MatriceTrasformazione[0] - xScale) <= Tolleranza, "La Matrice di Trasformazione[0] della strato dovrebbe essere " + xScale);

            AssertIsTrue(Math.Abs(layer.MatriceTrasformazione[3] - yScale) <= Tolleranza, "La Matrice di Trasformazione[3] del livello dovrebbe essere " + yScale);

            AssertIsTrue(Math.Abs(layer.MatriceTrasformazione[4] - nuovoSinistro) <= Tolleranza, "La Matrice di Trasformazione[4] del livello dovrebbe essere " + nuovoSinistro);

            AssertIsTrue(Math.Abs(layer.MatriceTrasformazione[5] - nuovoTop) <= Tolleranza, "La Matrice di Trasformazione[5] del livello dovrebbe essere " + nuovoTop);

            image.Save(outputFileName + ".psd", new PsdOptions());

            image.Save(outputFileName + ".png", new PngOptions() { TipoColore = PngTipoColore.VeroColoreConAlfa });

        }

{{< /highlight >}}