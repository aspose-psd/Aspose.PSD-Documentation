---
title: Aspose.PSD voor .NET 24.1 - Release-opmerkingen
type: docs
weight: 120
url: /nl/net/aspose-psd-voor-net-24-1-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel** | **Samenvatting**                                                                                   | **Categorie** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [AI-indeling] Basisverwerking toegevoegd voor AI-afbeeldingen met meerdere pagina's               |   Feature   |
| PSDNET-718  | Teksteffect kromming is niet van toepassing op tekst                                               |     Bug     |
| PSDNET-1620 | Onjuiste weergave van masker in het specifieke bestand                                             |     Bug     |
| PSDNET-1855 | NullReferenceException bij Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor   |     Bug     |
| PSDNET-1883 | [AI-indeling] Geheugengebruik opgelost in AiExporterUtils                                           |     Bug     |



## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-718. Teksteffect kromming is niet van toepassing op tekst**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "tekst_kromming.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. Onjuiste weergave van masker in het specifieke bestand**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "masker_probleem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_zachtLicht3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "masker_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [AI-indeling] Basisverwerking toegevoegd voor afbeeldingen met meerdere pagina's**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "driePaginas.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "eerstePaginaUitvoer.png");
string secondPageOutputPng = Path.Combine(outputFolder, "tweedePaginaUitvoer.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "derdePaginaUitvoer.png");

// Laad de AI-afbeelding.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Standaard is de ActivePageIndex 0.
    // Dus als u de AI-afbeelding opslaat zonder deze eigenschap te wijzigen, wordt de eerste pagina gerenderd en opgeslagen.
    image.Save(firstPageOutputPng, new PngOptions());

    // Wijzig de actieve paginaindex naar de tweede pagina.
    image.ActivePageIndex = 1;

    // sla de tweede pagina van de AI-afbeelding op als een PNG-afbeelding.
    image.Save(secondPageOutputPng, new PngOptions());

    // Wijzig de actieve paginaindex naar de derde pagina.
    image.ActivePageIndex = 2;

    // Sla de derde pagina van de AI-afbeelding op als een PNG-afbeelding.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException bij Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Lettertypen");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "uit_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [AI-indeling] Geheugengebruik opgelost in AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "driePaginas.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "eerstePaginaUitvoer.png");
string secondPageOutputPng = Path.Combine(outputFolder, "tweedePaginaUitvoer.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "derdePaginaUitvoer.png");

const double GeheugenLimiet = 220;
double geheugenGebruikt = double.MaxValue;

// Laad de AI-afbeelding.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Sla de eerste pagina van de AI-afbeelding op als een PNG-afbeelding.
    image.Save(firstPageOutputPng, new PngOptions());

    // Wijzig de actieve paginaindex naar de tweede pagina.
    image.ActivePageIndex = 1;

    // Sla de tweede pagina van de AI-afbeelding op als een PNG-afbeelding.
    image.Save(secondPageOutputPng, new PngOptions());

    // Wijzig de actieve paginaindex naar de derde pagina.
    image.ActivePageIndex = 2;

    // Sla de derde pagina van de AI-afbeelding op als een PNG-afbeelding.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

geheugenGebruikt = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (geheugenGebruikt > GeheugenLimiet)
{
    throw new Exception("Het geheugengebruik is te hoog. " + geheugenGebruikt + " in plaats van " + GeheugenLimiet.ToString("F1"));
}
{{< /highlight >}}
