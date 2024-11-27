---
title: Aspose.PSD pro .NET 24.1 - Poznámky k vydání
type: docs
weight: 120
url: /cs/net/aspose-psd-pro-net-24-1-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**    | **Shrnutí**                                                                                        | **Kategorie** |
|:-----------|:----------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [AI Formát] Přidána základní obsluha pro vícestránkové AI obrázky                                    | Feature      |
| PSDNET-718  | Efekt zkreslení textu se nepoužije na text                                                          | Chyba        |
| PSDNET-1620 | Nesprávné vykreslování masky ve specifickém souboru                                                 | Chyba        |
| PSDNET-1855 | NullReferenceException u Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor       | Chyba        |
| PSDNET-1883 | [AI Formát] Oprava využití paměti v AiExporterUtils                                                  | Chyba        |



## **Změny ve veřejném rozhraní API**
# **Přidaná API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Odstraněná API:**
- Žádná


## **Příklady použití:**

**PSDNET-718. Efekt zkreslení textu se nepoužije na text**

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

**PSDNET-1620. Nesprávné vykreslování masky ve specifickém souboru**

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

**PSDNET-1835. [AI Formát] Přidána základní obsluha pro vícestránkové AI obrázky**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// Načtení AI obrázku.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Výchozí hodnota ActivePageIndex je 0.
    // Pokud tedy uložíte AI obrázek bez změny této vlastnosti, bude vykreslena a uložena první stránka.
    image.Save(firstPageOutputPng, new PngOptions());

    // Změna aktivního indexu stránky na druhou stránku.
    image.ActivePageIndex = 1;

    // Uložení druhé stránky AI obrázku jako obrázek PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Změna aktivního indexu stránky na třetí stránku.
    image.ActivePageIndex = 2;

    // Uložení třetí stránky AI obrázku jako obrázek PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException u Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

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

**PSDNET-1883. [AI Formát] Oprava využití paměti v AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// Načtení AI obrázku.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Uložení první stránky AI obrázku jako obrázek PNG.
    image.Save(firstPageOutputPng, new PngOptions());

    // Změna aktivního indexu stránky na druhou stránku.
    image.ActivePageIndex = 1;

    // Uložení druhé stránky AI obrázku jako obrázek PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Změna aktivního indexu stránky na třetí stránku.
    image.ActivePageIndex = 2;

    // Uložení třetí stránky AI obrázku jako obrázek PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("Využití paměti je příliš velké. " + memoryUsed + " místo " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
