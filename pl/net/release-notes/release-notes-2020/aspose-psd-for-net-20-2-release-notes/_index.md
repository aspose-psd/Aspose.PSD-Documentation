---
title: Aspose.PSD dla .NET 20.2 - Notatki dotyczące wersji
type: docs
weight: 110
url: /pl/net/aspose-psd-dla-net-20-2-notatki-dotyczace-wersji/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki dotyczące wersji [Aspose.PSD dla .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-206|Udoskonalenie możliwości renderowania tekstu o różnych kolorach w warstwie tekstowej|Funkcja|
|PSDNET-369|Wsparcie zasobu clbl (Zasób warstwy zawiera informacje o elementach obcinania mikstury)|Funkcja|
|PSDNET-274 |Wsparcie zasobu blwh (Zasób zawiera Dane warstwy regulacji czerni i bieli)|Funkcja|
|PSDNET-230|Możliwość eksportu grupy warstw do formatów Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Funkcja|
|PSDNET-372|Wsparcie zasobu lspf (Zawiera ustawienia dotyczące ustawień chronionych warstwy)|Funkcja|
|PSDNET-370|Wsparcie zasobu infx (Zawiera dane o mieszaniu elementów wewnętrznych)|Funkcja|
|PSDNET-251|Refaktoryzacja PsdImage i Layer w celu zmiany zachowania transformacji (Poprawne zmiany rozmiaru/obrotu/przycięcia dla masek warstw gdy transformujemy jedną warstwę osobno)|Udoskonalenie|
|PSDNET-276 |W niektórych ustawieniach globalizacji nie można otworzyć obrazu rastrowego AI|Błąd|
|PSDNET-194|Po wykonaniu operacji FlipRotate na warstwie, obraz PSD staje się nieczytelny|Błąd|
|PSDNET-177. |ArgumentException podczas ładowania pliku PSD|Błąd|
|PSDNET-249|Po zastosowaniu metody transformacji tylko dla warstwy, zapisana warstwa ma nieprawidłowe granice lub maskę|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
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
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String,System.Exception)
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
# **Usunięte API:**
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor(System.Int32)
- F:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues

## **Przykłady użycia:**
**PSDNET-206. Udoskonalenie możliwości renderowania tekstu o różnych kolorach w warstwie tekstowej**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("tekst_testowy_rozne_kolory.psd"))

{

    var txtLayer = (TextLayer)psdImage.Layers[1];

    txtLayer.TextData.UpdateLayerData();

    psdImage.Save("output.png", new PngOptions());

}

{{< /highlight >}}

**PSDNET-369. Wsparcie zasobu clbl (Zasób warstwy zawiera informacje o elementach obcinania mikstury)**

{{< highlight java >}}

        void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "ProbowkaZasobow.psd";

        string destinationFileName = "Output" + sourceFileName;

        ClblResource GetClblResource(PsdImage im)

        {

            foreach (var layer in im.Layers)

            {

                foreach (var layerResource in layer.Resources)

                {

                    if (layerResource is ClblResource)

                    {

                        return (ClblResource)layerResource;

                    }

                }

            }

            throw new Exception("Określony zasób ClblResource nie został znaleziony");

        }

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName))

        {

            var resource = GetClblResource(im);

            AssertIsTrue(resource.BlendClippedElements, "ClblResource.BlendClippedElements powinien mieć wartość true");

            // Testowanie edycji i zapisywania

            resource.BlendClippedElements = false;

            im.Save(destinationFileName);

        }

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName))

        {

            var resource = GetClblResource(im);

            AssertIsTrue(!resource.BlendClippedElements, "ClblResource.BlendClippedElements powinien zmienić się na false");

        }

{{< /highlight >}}

**PSDNET-274. Wsparcie zasobu blwh (Zasób zawiera Dane warstwy regulacji czerni i bieli)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Oczekiwana wartość własności nie jest równa wartości faktycznej";

        void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

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

            int newTintColor)

        {

            string destinationFileName = "Output" + sourceFileName;

            bool isRequiredResourceFound = false;

            using (PsdImage im = (PsdImage)Image.Load(sourceFileName))

            {

                foreach (var layer in im.Layers)

                {

                    foreach (var layerResource in layer.Resources)

                    {

                        if (layerResource is BlwhResource)

                        {

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

                            // Testowanie edycji i zapisywania

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

            AssertIsTrue(isRequiredResourceFound, "Określony zasób BlwhResource nie został znaleziony");

            isRequiredResourceFound = false;

            using (PsdImage im = (PsdImage)Image.Load(destinationFileName))

            {

                foreach (var layer in im.Layers)

                {

                    foreach (var layerResource in layer.Resources)

                    {

                        if (layerResource is BlwhResource)

                        {

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

            AssertIsTrue(isRequiredResourceFound, "Określony zasób BlwhResource nie został znaleziony");

        Console.WriteLine("Aktualizacja zasobu Blwh działa zgodnie z oczekiwaniami. Naciśnij dowolny klawisz.");

{{< /highlight >}}

**PSDNET-230. Możliwość eksportu grupy warstw do formatów Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}


  using (var psdImage = (PsdImage)Image.Load("1.psd"))

            {

                // folder z tłem

                LayerGroup bg_folder = (LayerGroup)psdImage.Layers[0];

                // folder z treścią

                LayerGroup content_folder = (LayerGroup)psdImage.Layers[4];

                bg_folder.Save("tlo.png", new PngOptions());

                content_folder.Save("zawartosc.png", new PngOptions());

            }

{{< /highlight >}}

` `**PSDNET-372. Wsparcie zasobu lspf (Zawiera ustawienia dotyczące ustawień chronionych warstwy)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Oczekiwana wartość własności nie jest równa wartości faktycznej";

        void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "ProbowkaZasobow.psd";

        string destinationFileName = "Output" + sourceFileName;

        bool isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName))

        {

            foreach (var layer in im.Layers)

            {

                foreach (var layerResource in layer.Resources)

                {

                    if (layerResource is LspfResource)

                    {

                        var resource = (LspfResource)layerResource;

                        isRequiredResourceFound = true;

                        AssertIsTrue(false == resource.IsCompositeProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsPositionProtected, ActualPropertyValueIsWrongMessage);

                        AssertIsTrue(false == resource.IsTransparencyProtected, ActualPropertyValueIsWrongMessage);

                        // Testowanie edycji i zapisywania

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

        AssertIsTrue(isRequiredResourceFound, "Określony zasób LspfResource nie został znaleziony");

        isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName))

        {

            foreach (var layer in im.Layers)

            {

                foreach (var layerResource in layer.Resources)

                {

                    if (layerResource is LspfResource)

                    {

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

        AssertIsTrue(isRequiredResourceFound, "Określony zasób LspfResource nie został znaleziony");

        Console.WriteLine("Aktualizacja zasobu Lspf działa zgodnie z oczekiwaniami. Naciśnij dowolny klawisz.");

{{< /highlight >}}

` `**PSDNET-370. Wsparcie zasobu infx (Zawiera dane o mieszaniu elementów wewnętrznych)**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "ProbowkaZasobow.psd";

        string destinationFileName = "Output" + sourceFileName;

        bool isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName))

        {

            foreach (var layer in im.Layers)

            {

                foreach (var layerResource in layer.Resources)

                {

                    if (layerResource is InfxResource)

                    {

                        var resource = (InfxResource)layerResource;

                        isRequiredResourceFound = true;

                        AssertIsTrue(!resource.BlendInteriorElements, "InfxResource.BlendInteriorElements powinien być równy false");

                        // Testowanie edycji i zapisywania

                        resource.BlendInteriorElements = true;

                        im.Save(destinationFileName);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(isRequiredResourceFound, "Określony zasób InfxResource nie został znaleziony");

        isRequiredResourceFound = false;

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName))

        {

            foreach (var layer in im.Layers)

            {

                foreach (var layerResource in layer.Resources)

                {

                    if (layerResource is InfxResource)

                    {

                        var resource = (InfxResource)layerResource;

                        isRequiredResourceFound = true;

                        AssertIsTrue(resource.BlendInteriorElements, "InfxResource.BlendInteriorElements powinien zmienić się na true");

                        break;

                    }

                }

            }

        }

        AssertIsTrue(isRequiredResourceFound, "Określony zasób InfxResource nie został znaleziony");

{{< /highlight >}}

**PSDNET-251. Refaktoryzacja PsdImage i Layer w celu zmiany zachowania transformacji (Poprawne zmiany rozmiaru/obrotu/przycięcia dla masek warstw gdy transformujemy jedną warstwę osobno)**

{{< highlight java >}}

             var enums = (RotateFlipType[])Enum.GetValues(typeof(RotateFlipType));

            var fileNames = new string[]

            {

                "JednaZwyklaIJednaRegulacjaZVectorIWarstwaMaski",

                "JednaZwyklaIJednaRegulacjaZMaskaWarstwy",

                "WarstwaTekstowa",

                "PołączoneKształtyZWZhanglowanymTekstem"

            };

            foreach (string fileName in fileNames)

            {

                foreach (RotateFlipType rotateFlipType in enums)

                {

                    string sourceFileName = fileName + ".psd";

                    string destinationFileName = fileName + "_" + rotateFlipType;

                    var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

                    using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

                    {

                        image.RotateFlip(rotateFlipType);

                        image.Save(destinationFileName);

                    }

                }

            }

{{< /highlight >}}

**PSDNET-276. W niektórych ustawieniach globalizacji nie można otworzyć obrazu rastrowego AI**

{{< highlight java >}}

        string sourceFileName = "obraz_rastrowy_8.ai";

        System.Threading.Thread.CurrentThread.CurrentCulture = new System.Globalization.CultureInfo("pl_PL");

        System.Threading.Thread.CurrentThread.CurrentUICulture = System.Threading.Thread.CurrentThread.CurrentCulture;

        using (AiImage image = (AiImage)Image.Load(sourceFileName))

        {

            // nie powinien być rzucany wyjątek

        }

{{< /highlight >}}

**PSDNET-194. Po wykonaniu operacji FlipRotate na warstwie, obraz PSD staje się nieczytelny**

{{< highlight java >}}


             string sourceFileName = GetFileInCustomFolderRelativeToBase(@"testdata\Problemy\IMAGINGNET-2617\1.psd");

            var flipType = RotateFlipType.Rotate90FlipNone;

            var outFileNamePsd = this.GetFileInOutputFolder("TestObrotu2617.psd");

            try

            {

                using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

                {

                    for (int i = 0; i < image.Layers.Length; i++)

                    {

                        var layer = image.Layers[i];

                        if (!layer.Bounds.IsEmpty)

                        {

                            layer.RotateFlip(flipType);

                        }

                    }

                    string outFileNamePng = this.GetFileInOutputFolder("TestObrotu2617.png");

                    image.Save(outFileNamePsd);

                }

            // Tutaj otrzymujemy wyjątek. Dla programu PhotoShop ten plik również jest nieczytelny,

            using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) // Rzuca wyjątek

            {

                // Nic nie rób

            }

{{< /highlight >}}

**PSDNET-177. ArgumentException podczas ładowania pliku PSD**

{{< highlight java >}}

         string sourcePath = "1.psd";

        string psdPath = "TestObrotu2617.psd";

        RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

        using (var im = (PsdImage)(Image.Load(sourcePath)))

        {

            im.RotateFlip(flipType);

            im.Save(psdPath);

        }

        using (var im = (PsdImage)(Image.Load(psdPath))) // Tutaj nie powinniśmy otrzymać żadnych wyjątków

        {

            // nic nie rób

        }

{{< /highlight >}}

**PSDNET-249. Po zastosowaniu metody transformacji tylko dla warstwy, zapisana warstwa ma nieprawidłowe granice lub maskę**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        const double Tolerance = 1e-6;

        int newWidth = 132;

        int newHeight = 247;

        double xScale = newWidth / 48.0;

        double yScale = newHeight / 19.0;

        string sourceFileName = "WarstwaTekstowa.psd";

        string outputFileName = "WarstwaTekstowaZmianaRozmiaru" + newWidth + "_" + newHeight;

        var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

        using (PsdImage image = (PsdImage) Image.Load(sourceFileName, psdLoadOptions))

        {

            var layer = image.Layers[1] as TextLayer;

            var newLeft = layer.Left - (newWidth - layer.Width) / 2;

            var newTop = layer.Top - (newHeight - layer.Height) / 2;

            layer.Resize(newWidth, newHeight);

            AssertIsTrue(layer.Left == newLeft, "Właściwość Left warstwy powinna wynosić " + newLeft);

            AssertIsTrue(layer.Top == newTop, "Właściwość Top warstwy powinna wynosić " + newTop);

            AssertIsTrue(layer.Width == newWidth, "Właściwość Width warstwy powinna wynosić " + newWidth);

            AssertIsTrue(layer.Height == newHeight, "Właściwość Height warstwy powinna wynosić " + newHeight);

            AssertIsTrue(Math.Abs(layer.TransformMatrix[0] - xScale) <= Tolerance, "TransformMatrix[0] warstwy powinna wynosić " + xScale);

            AssertIsTrue(Math.Abs(layer.TransformMatrix[3] - yScale) <= Tolerance, "TransformMatrix[3] warstwy powinna wynosić " + yScale);

            AssertIsTrue(Math.Abs(layer.TransformMatrix[4] - newLeft) <= Tolerance, "TransformMatrix[4] warstwy powinna wynosić " + newLeft);

            AssertIsTrue(Math.Abs(layer.TransformMatrix[5] - newTop) <= Tolerance, "TransformMatrix[5] warstwy powinna wynosić " + newTop);

            image.Save(outputFileName + ".psd", new PsdOptions());

            image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

        }

{{< /highlight >}}