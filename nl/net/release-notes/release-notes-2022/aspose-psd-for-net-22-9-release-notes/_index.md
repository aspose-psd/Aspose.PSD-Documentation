---
title: Aspose.PSD voor .NET 22.9 - Release-opmerkingen
type: docs
weight: 40
url: /nl/net/aspose-psd-voor-net-22-9-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Deze release heeft een regressie in het geval van 16-bits exports, daarom raden we voorzichtigheid aan bij het gebruik van deze functie in deze release. Gelieve Aspose.PSD niet bij te werken naar 22.9 als 16-bits beeldverwerking je primaire functionaliteit is.
- Voor verschillende versies van Photoshop kunnen gebruikers mogelijk een venster tegenkomen met een foutmelding met de tekst 'layer lezen', dit zal de samenwerking met het PSD-bestand niet beïnvloeden.

We werken aan oplossingen voor deze problemen.

{{% /alert %}}

|**Key**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-1237|Maak het interne LayerStyleFX-model dat effecten en gerelateerde gegevens zal bevatten voor het gebruik van het enkele model in effectenbronnen Lfx2, lmfx en mlst|Verbetering|
|PSDNET-1227|Toevoegen van lezen en schrijven van 'Lefx'-structuren met informatie over effecten voor laagstaten in TimeLine-modellen|Functie|
|PSDNET-1230|Toepassen van TimeLine laagstaat op laag in PsdImage|Functie|
|PSDNET-1072|Onjuiste transparantie bij opslaan van PSD-bestand (RGB/16bit) bij export naar 8bit|Fout|
|PSDNET-1140|Uitzondering bij het laden van globale laagresources tijdens het openen van PSB-document|Fout|
|PSDNET-1266|Geheugenlek bij de verwerking van specifieke bestanden|Fout|


## **Wijzigingen in openbare API**

# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **Verwijderde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Gebruik voorbeelden:**

**PSDNET-1072. Onjuiste transparantie bij opslaan van PSD-bestand (RGB/16bit) bij export naar 8bit**

{{< highlight csharp >}}
string inputPsdFile    = "8bitMetTransparantie.psd";
string outputPsdFile   = "16bitMetTransparantie.psd";
string outputImageFile = "UitvoerMetTransparantie.png";

using (var img = Image.Load(inputPsdFile))
{
    // 16-bits opslaan opties
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // Afbeelding opslaan met 16-bits kleuren
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Uitzondering bij het laden van globale laagresources stap bij het openen van PSB-document**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "uitvoer.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // Hier mag geen uitzondering optreden.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Toevoegen van lezen en schrijven van 'Lefx'-structuren met informatie over effecten voor laagstaten in TimeLine-modellen**

{{< highlight csharp >}}
string sourceFile = "4_geanimeerd.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] layerIds = timeLine.LayerIds;

    var layerStateEffects11 = timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects;

    layerStateEffects11.AddDropShadow();
    layerStateEffects11.AddGradientOverlay();

    var layerStateEffects21 = timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects;
    layerStateEffects21.AddStroke(FillType.Color);
    layerStateEffects21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1230. Toepassen van TimeLine laagstaat op laag in PsdImage**

{{< highlight csharp >}}
string sourceFile = "3_geanimeerd.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    var layerState11 = timeLine.Frames[1].LayerStates[layerIds[1]];

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddPatternOverlay();
    layerState11.BlendMode = BlendMode.Multiply;

    // Wijzig het actieve frame van 0 naar 1 om het toepassen van LayerState op Layer te activeren
    timeLine.ActiveFrame = 1;

    // Voer wijzigingen door in PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Geheugenlek bij de verwerking van specifieke bestanden**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Totaal gebruikte bytes voor de test: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // CheckOpenSaving
    using (MemoryStream outputStream = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(outputStream, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(inputNumber, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    max = Math.Max(max, memCount);
}

memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Totaal gebruikte bytes na de test: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "Geheugenlek in basisonderdelen gevonden!");
{{< /highlight >}}
