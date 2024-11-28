---
title: Aspose.PSD voor .NET 24.7 - Release-opmerkingen
type: docs
weight: 60
url: /nl/net/aspose-psd-voor-net-24-7-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                                | **Categorie** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | Uitzondering "Afbeeldingsladen mislukt." bij openen AI-document                                      | Bug      |
| PSDNET-2022 | Tekst wordt onjuist weergegeven in uitvoer PDF-bestanden                                           | Bug      |
| PSDNET-2061 | Oplossing voor ImageSaveException: Afbeeldingsexport mislukt voor het opgegeven bestand op Linux   | Bug      |
| PSDNET-2080 | Oplossing voor lettertypen laden bij gebruik van Aspose.Drawing                                     | Bug      |
| PSDNET-2085 | 'Arithmetische bewerking resulteerde in een overflow' bij maken van slim objectlaag met grote JPEG | Bug      |
| PSDNET-2100 | Het AI-bestand kan niet worden omgezet naar een JPG-bestand                                         | Bug      |

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-1029. Uitzondering "Afbeeldingsladen mislukt." bij openen AI-document**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Tekst wordt onjuist weergegeven in uitvoer PDF-bestanden**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. Oplossing voor ImageSaveException: Afbeeldingsexport mislukt voor het opgegeven bestand op Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Oplossing voor lettertypen laden bij gebruik van Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Vóór update. Aantal geïnstalleerde lettertypen: " + installedFonts.Families.Length);
    Console.WriteLine("- Platform: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Vernieuw de lettertypecache door te proberen de Adobe lettertype-naam voor 'Arial' te verkrijgen: "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Na update. Aantal geïnstalleerde lettertypen: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'Arithmetische bewerking resulteerde in een overflow' bij maken van slim objectlaag met grote JPEG**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. Het AI-bestand kan niet worden omgezet naar een JPG-bestand**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
