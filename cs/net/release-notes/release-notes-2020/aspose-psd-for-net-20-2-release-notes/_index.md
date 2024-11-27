---
title: Aspose.PSD pro .NET 20.2 - Poznámky k vydání
type: docs
weight: 110
url: /cs/net/aspose-psd-pro-net-20-2-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-206|Zlepšení možnosti zobrazování textu různých barev ve vrstvě textu|Funkce|
|PSDNET-369|Podpora clbl prostředků (Vrstvový prostředek obsahuje informace o prvcích oříznutí míchání)|Funkce|
|PSDNET-274 |Podpora blwh prostředku (Prostředek obsahuje data o vrstvě úpravy černobílé)|Funkce|
|PSDNET-230|Schopnost exportovat skupinu vrstev do formátů Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Funkce|
|PSDNET-372|Podpora lspf Prostředku (Obsahuje nastavení ochrany vrstvy)|Funkce|
|PSDNET-370|Podpora infx prostředku (Obsahuje data o míchání vnitřních prvků)|Funkce|
|PSDNET-251|Refaktoring tříd PsdImage a Layer pro změnu chování transformace (Správné změny velikosti/otočení/řezání pro vrstvy masky, pokud transformujeme pouze jednu vrstvu samostatně)|Vylepšení|
|PSDNET-276 |V některých nastaveních globalizace nemůže být otevřen obraz rastrového obrázku AI|Chyba|
|PSDNET-194|Po provedení operace FlipRotate na vrstvě se stane obrázek PSD nepřečitelný|Chyba|
|PSDNET-177. |System.ArgumentException během načítání souboru PSD|Chyba|
|PSDNET-249|Po použití metody transformace pouze u vrstvy má uložená vrstva nesprávné hranice nebo masku|Chyba|

## **Veřejné změny API**
# **Přidaná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskRectangle
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Šířka
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Výška
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Rods
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Blue
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.PoužitíTint
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorRed
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorGreen
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorBlue
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Uložit(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Délka
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PsdVerze
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Červená
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Žlutá
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Zelená
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Kyan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Modrá
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Fialová
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PoužitíTint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TintColor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor
- P:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinovanéHodnoty
- T:Aspose.PSD.AggregateException
- M:Aspose.PSD.CmykBarva.Equals(System.Object)
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
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Délka
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.PsdVerze
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.JeDataUkládánaDiskrétně
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.ZískatÚdajeKanálu(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetActiveManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Uložit(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetCurveManager
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.TypeToolKey
- T:Aspose.PSD.ImageOptions.TiffOptionsUtils
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.#ctor
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.GetValidTagsCount(Aspose.PSD.FileFormats.Tiff.TiffDataType[])
- P:Aspose.PSD.ImageOptionsBase.PokrokEventHandler
- P:Aspose.PSD.LoadOptions.PokrokEventHandler
- M:Aspose.PSD.Matrix.#ctor(Aspose.PSD.Matrix)
- M:Aspose.PSD.Metered.Equals(System.Object)
- T:Aspose.PSD.PokrokEventHandler
- T:Aspose.PSD.ProgressManagement.Typudálosti
- F:Aspose.PSD.ProgressManagement.Typudálosti.RelativníPokrok
- F:Aspose.PSD.ProgressManagement.Typudálosti.Změnapodmínek
- F:Aspose.PSD.ProgressManagement.Typudálosti.Inicializace
- F:Aspose.PSD.ProgressManagement.Typudálosti.Předzpracování
- F:Aspose.PSD.ProgressManagement.Typudálosti.Zpracování
- F:Aspose.PSD.ProgressManagement.Typudálosti.Závěr
- T:Aspose.PSD.ProgressManagement.PokrokEventHandlerInfo
- P:Aspose.PSD.ProgressManagement.PokrokEventHandlerInfo.Popis
- P:Aspose.PSD.ProgressManagement.PokrokEventHandlerInfo.TypUdálosti
- P:Aspose.PSD.ProgressManagement.PokrokEventHandlerInfo.MaxHodnota
- P:Aspose.PSD.ProgressManagement.PokrokEventHandlerInfo.Hodnota
- M:Aspose.PSD.RasterImage.getZákladníÚhel
- M:Aspose.PSD.RasterImage.NormalizeAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle(System.Boolean,Aspose.PSD.Barva)
# **Odstraněné API:**
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor(System.Int32)
- F:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinovanéHodnoty

## **Příklady použití:**
**PSDNET-206. Zlepšení možnosti zobrazování textu různých barev ve vrstvě textu**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("text_ethalon_different_colors.psd"))

{

    var txtLayer = (TextLayer)psdImage.Layers[1];

    txtLayer.TextData.UpdateLayerData();

    psdImage.Save("output.png", new PngOptions());

}

{{< /highlight >}}

**PSDNET-369. Podpora clbl prostředků (Vrstvový prostředek obsahuje informace o prvcích oříznutí míchání)**

{{< highlight java >}}

        void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "SampleForResource.psd";

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

            throw new Exception("The specified ClblResource not found");

        }

        using (PsdImage im = (PsdImage)Image.Load(sourceFileName))

        {

            var resource = GetClblResource(im);

            AssertIsTrue(resource.BlendClippedElements, "The ClblResource.BlendClippedElements should be true");

            // Test editing and saving

            resource.BlendClippedElements = false;

            im.Save(destinationFileName);

        }

        using (PsdImage im = (PsdImage)Image.Load(destinationFileName))

        {

            var resource = GetClblResource(im);

            AssertIsTrue(!resource.BlendClippedElements, "The ClblResource.BlendClippedElements should change to false");

        }

{{< /highlight >}}

**PSDNET-274. Podpora blwh prostředku (Prostředek obsahuje data o vrstvě úpravy černobílé)**

{{< highlight java >}}

         const string ActualPropertyValueIsWrongMessage = "Očekávaná hodnota vlastnosti se neshoduje s aktuální hodnotou";

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

                            // Test editing and saving

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

            AssertIsTrue(isRequiredResourceFound, "The specified BlwhResource not found");

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

            AssertIsTrue(isRequiredResourceFound, "The specified BlwhResource not found");

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

        Console.WriteLine("Aktualizace BlwhResource funguje jak bylo očekáváno. Stiskněte libovolnou klávesu.");

{{< /highlight >}}

**PSDNET-230. Schopnost exportovat skupinu vrstev do formátů Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("1.psd"))

{

    // složka s pozadím

    LayerGroup bg_folder = (LayerGroup)psdImage.Layers[0];

    // složka s obsahem

    LayerGroup content_folder = (LayerGroup)psdImage.Layers[4];

    bg_folder.Save("background.png", new PngOptions());

    content_folder.Save("content.png", new PngOptions());

}

{{< /highlight >}}