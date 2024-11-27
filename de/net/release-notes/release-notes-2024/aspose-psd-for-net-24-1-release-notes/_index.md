---
title: Aspose.PSD für .NET 24.1 - Versionshinweise
type: docs
weight: 120
url: /de/net/aspose-psd-fur-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                             | **Kategorie** |
|:--------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1835   | [AI-Format] Grundlegende Behandlung für mehrseitige AI-Bilder                                   | Feature      |
| PSDNET-718    | Der Warp-Texteffekt wird nicht auf Text angewendet                                              | Fehler       |
| PSDNET-1620   | Falsche Anzeige des Maskierung in der spezifischen Datei                                        | Fehler       |
| PSDNET-1855   | NullReferenceException bei Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor | Fehler       |
| PSDNET-1883   | [AI-Format] Beheben des Speicherverbrauchs in AiExporterUtils                                  | Fehler       |



## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Entfernte APIs:**
- Keine


## **Verwendungsbeispiele:**

**PSDNET-718. Der Warp-Texteffekt wird nicht auf Text angewendet**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
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

**PSDNET-1620. Falsche Anzeige des Maskierung in der spezifischen Datei**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
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

**PSDNET-1835. [AI-Format] Grundlegende Behandlung für mehrseitige AI-Bilder**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// Laden Sie das AI-Bild.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Standardmäßig ist der ActivePageIndex 0.
    // Daher wird, wenn Sie das AI-Bild ohne Änderung dieses Eigenschaft speichern, die erste Seite gerendert und gespeichert.
    image.Save(firstPageOutputPng, new PngOptions());

    // Ändern Sie den aktiven Seitenindex auf die zweite Seite.
    image.ActivePageIndex = 1;

    // Speichern Sie die zweite Seite des AI-Bildes als PNG-Bild.
    image.Save(secondPageOutputPng, new PngOptions());

    // Ändern Sie den aktiven Seitenindex auf die dritte Seite.
    image.ActivePageIndex = 2;

    // Speichern Sie die dritte Seite des AI-Bildes als PNG-Bild.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException bei Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [AI-Format] Beheben des Speicherverbrauchs in AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// Laden Sie das AI-Bild.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Speichern Sie die erste Seite des AI-Bildes als PNG-Bild.
    image.Save(firstPageOutputPng, new PngOptions());

    // Ändern Sie den aktiven Seitenindex auf die zweite Seite.
    image.ActivePageIndex = 1;

    // Speichern Sie die zweite Seite des AI-Bildes als PNG-Bild.
    image.Save(secondPageOutputPng, new PngOptions());

    // Ändern Sie den aktiven Seitenindex auf die dritte Seite.
    image.ActivePageIndex = 2;

    // Speichern Sie die dritte Seite des AI-Bildes als PNG-Bild.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("Speicherauslastung ist zu hoch. " + memoryUsed + " anstatt " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
