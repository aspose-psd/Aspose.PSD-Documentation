---
title: Aspose.PSD voor .NET 24.6 - Release-opmerkingen
type: docs
weight: 70
url: /nl/net/aspose-psd-voor-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **Samenvatting**                                                                         | **Categorie** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | Implementeer ondersteuning voor Gradient-maplaag                                                                               | Functie      |
| PSDNET-1670 | [AI-indeling] Voeg ondersteuning toe voor XPacket Metadata naar AI-indeling                                                                               | Functie      |
| PSDNET-1831 | Implementeer Inflate, Squeeze en Twist warp-types                                                                               | Functie      |
| PSDNET-1653 | Rgb- en Lab-modi kunnen niet minder dan 3 kanalen bevatten en meer dan 4 kanalen in het bestand met ArtBoard-lagen                                                                               | Fout      |
| PSDNET-1775 | Het verwerking gebied top moet positief zijn. (Parameter 'areaToProcess') bij de verwerking van specifiek bestand                                                                               | Fout      |
| PSDNET-2052 | Uitgezette afbeelding over het canvas wordt bijgesneden na het opslaan. Gegevens gaan verloren maar de voorvertoning ziet er correct uit                                                                               | Fout      |

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-1450. Implementeer ondersteuning voor Gradient-maplaag**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // Voeg een Gradient-map aanpassingslaag toe.
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// Controleer opgeslagen wijzigingen
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("Aangepast", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [AI-indeling] Voeg ondersteuning toe voor XPacket Metadata naar AI-indeling**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objecten zijn niet gelijk.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("Testobjecten zijn null.");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string expectedNPages = "1";
string expectedUnit = "Pixels";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Xmp Metadata is toegevoegd.
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // Nu hebben we toegang tot Xmp-pakketten van AI-bestanden.
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    
    var package = xmpMetaData.Packages[4];

    // En we hebben toegang tot de inhoud van deze pakketten.
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}

**PSDNET-1831. Implementeer Inflate, Squeeze en Twist warp-types**

{{< highlight csharp >}}
string[] files = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefix in files)
{
    string sourceFile = Path.Combine(baseFolder, prefix + ".psd");
    string outputFile = Path.Combine(outputFolder, prefix + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. Rgb- en Lab-modi kunnen niet minder dan 3 kanalen bevatten en meer dan 4 kanalen in het bestand met ArtBoard-lagen**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // Hier mag geen uitzondering optreden
    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. Het verwerking gebied top moet positief zijn. (Parameter 'areaToProcess') bij de verwerking van specifiek bestand**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
{
    image.Save(outputFile);
    // Er mag geen uitzondering zijn
}
{{< /highlight >}}

**PSDNET-2052. Uitgezette afbeelding over het canvas wordt bijgesneden na het opslaan. Gegevens gaan verloren maar de voorvertoning ziet er correct uit**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");

string outputFile = Path.Combine(outputFolder, "bigfile_output.psd");
string outputPicture = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // Er mag geen fout optreden
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(outputFile, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // Er mag geen fout optreden
    psdImage.Save(outputPicture, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
